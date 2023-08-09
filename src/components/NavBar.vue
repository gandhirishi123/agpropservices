<template>
    <v-app-bar app class="custom-header" flat  >
        <v-toolbar-title>
            <router-link to="/">
                <v-img
                    src="https://raw.githubusercontent.com/agprop-india/agprop-data/81b26e4b4b66d6028ea8c36cded435f5a7260d67/images/agprop%20logo.svg"
                    alt="Vuetify Name" contain max-height="30" />
            </router-link>
        </v-toolbar-title>
        <v-btn style="color: blue;" text class="mr-2" v-for="item in menuItems" :key="item.link" :to="item.link" link>{{ item.label }}</v-btn>
        <v-spacer/>
        <v-spacer/>
        <v-spacer/>
        <v-btn @click="login" rounded style="background-color: blue; color: white; font-weight: 900;" >
            <p>Login</p>
        </v-btn>
   
       
    </v-app-bar>
</template>
  
<style >
.custom-header {
  height: 56px;
  margin-left: auto ;
  margin-right: auto;
  margin-top: 12px !important;
  max-width: 1024px;
  border-radius: 16px !important;
  backdrop-filter: saturate(100%) blur(10px);
}
</style>

<script>
export default {
    data() {
        return {
            drawer: false,
            menuItems: [
                { label: 'Properties', link: '/properties' },
                { label: 'Products', link: '/products' },
                { label: 'Brand Requirements', link: '/brand-requirements' },
                { label: 'About', link: '/about' },
                { label: 'Contact', link: '/contact' },
            ],
        };
    },
    methods: {
        login() {}
    },
};
</script>
  
  

  