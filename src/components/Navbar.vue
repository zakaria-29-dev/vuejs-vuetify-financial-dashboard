<template>
   <nav>
      <v-navigation-drawer  v-model="drawer" dark app class="blue accent-2">
          <v-layout column align-center>
               <v-flex class="mt-10 mb-8"> 
                    <v-avatar >
                    <v-icon large>fas fa-store</v-icon>
                    </v-avatar>
               </v-flex>
          </v-layout>
           <v-list >
              <v-list-item v-for="link in links"  :key="link.text" router :to="link.route" active-class="border">
                  <v-list-item-action>
                     <v-icon >{{link.icon}}</v-icon>
                  </v-list-item-action>
                  <v-list-item-content >
                      <v-list-item-title >{{link.text}}</v-list-item-title>
                  </v-list-item-content>
              </v-list-item>
          </v-list>
         <v-flex class="ma-2"> 
 <template>
  <v-carousel
    cycle
    dark
    height="230"
    hide-delimiter-background
    show-arrows-on-hover
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
      <v-sheet
        color="white"
        height="80%"
        align="center"
        tile
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
          
        >
          <div class="grey--text" >
              <h4>Traffic fines</h4>
              <p class="ma-2">{{ slide }}</p>
              <v-btn outlined color="indigo">Read more</v-btn>
              </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>
         </v-flex>
      </v-navigation-drawer>
   </nav>
</template>
<script>
export default {
   data: () => ({
      drawer: true,
      links :[
          {icon: 'fas fa-home', text:'Home', route: '/'},
          {icon: 'far fa-credit-card', text:'Balance', route: '/balance'},
          {icon: 'fas fa-chart-line', text:'Investments', route: '/investments'},
          {icon: 'fas fa-balance-scale-right', text:'Insurance', route: '/insurance'},
          {icon: 'fas fa-briefcase', text:'Busines', route: '/busines'},
      ],
      colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
        ],
        slides: [
          'Online check and payment of official debts',
          'Online check and payment of official debts',
          'Online check and payment of official debts',
          'Online check and payment of official debts',
        ],
     
    }),
    components: {
   
  },

   
}
</script>
<style scoped>
.border {
  border-left: 4px solid #2c3e50;
}
</style>
