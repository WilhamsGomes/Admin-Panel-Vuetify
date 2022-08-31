<template>

    <v-navigation-drawer v-model="drawer" app>
        <v-img src="https://preview.pixlr.com/images/800wm/1439/2/1439104804.jpg" class="pa-4">
            <div class="text-center mt-4">
                <v-avatar class="mb-4" color="grey darken-1" size="64">
                    <v-img aspect-ratio="30" src="https://randomuser.me/api/portraits/women/81.jpg"/>
                </v-avatar>
                <h2 class="white--text">Vuetify Admin Panel</h2>
            </div>
        </v-img>

      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="[icon, text] in links"
          :key="icon"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  
</template>

<script>
    export default {
        props: ['drawer'],
        name:"Sidebar",
        data(){
            return{
                links: [
                    ["mdi-microsoft-windows", "Dashboard"],
                    ["mdi-account", "Profile"],
                    ["mdi-clipboard-list-outline", "Product"],
                    ["mdi-clipboard-list", "Order"],
                    ["mdi-cog-outline", "System Settings"],
                ],
            }
        }
    }
</script>

<style>

</style>