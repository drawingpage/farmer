<template>
<v-row class="main">
  <v-col 
  cols="3"
  class="leftCon">
  <!-- logp -->
    <v-img
      src="https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg"
      aspect-ratio="1.7"
      contain
      max-height="150" 
      class="logo"
    ></v-img>
    <!-- company name -->
    <h2 class="Farmer">Farmer</h2>
    <!-- buttons -->
    
    <NuxtLink
      class="links"
      v-for="(button,i) in navbar"
      :key="i"
      :to="button.to"
      >
      <div class="buttons">{{button.value}}</div>
      </NuxtLink>
      
  </v-col>
  <v-col class="rightCon">
    <!-- product List -->
    <v-card
      v-for="(card , i) in cards"
      :key="i"
      class="mx-auto productCard"
    >
      <v-img
        class="white--text align-end"
        :src="card.src"
      >
      </v-img>
      <v-card-title class="pb-0">
        {{card.name}}
      </v-card-title>
      <v-card-text class="text--primary">
        <div>1 KG Price = {{card.price}}Rs</div>
        <div>{{card.place}}</div>
      </v-card-text>
      <v-card-actions>
        <v-btn
          class="shopBtn"
          text
        >
          Shop
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-col>
</v-row>
</template>
<style scoped>
.shopBtn{
  background-color: orange;
  color: white;
}
.productCard{
width: 500px;
margin: auto;
margin-top: 20px;

}
.Farmer{
  color: orange;
  text-align: center;
  margin-bottom: 20px;
}
.links{
  text-decoration: none;
  color: #000;
}
.buttons{
  text-align: center;
  width: 100%;
  padding: 10px;
  margin-top: 10px;
  background-color: #c5c5c5;
  height: 50px;
  
}
.buttons:hover{
  background-color: #e1e4e4;
}
.leftCon{
  height: 100vh;
  background-color: #e5e5e5;
  padding: auto;
}
.logo{
  margin: 10px;
}
.rightCon{
  height: 100vh;
  background-color: white;
}
</style>
<script>


export default {
  
  data() {
    return {
      navbar: [
        {
          value: 'Home', 
          to: 'https://nuxtjs.org/docs/features/nuxt-components#the-nuxtlink-component'
          },
        {
          value: 'About',
           to: '/about'
           },
        {
          value: 'Contact',
           to: '/contact'
           },
        {
          value: 'SignIn/SignOut', 
          to: '/contact'
          },
      ],
      cards: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
            name:"Carrot",
            place:"Malappuram ",
            price:"200",
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
            name:"Tomato",
            place:"Kozhikode",
            price:"200",
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
            name:"Beans",
            place:"Thrissur",
            price:"200",
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
            name:"Chilli",
            place:"Kannur",
            price:"200",
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
            name:"Bitroot",
            place:"Wayanad",
            price:"200",
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
            name:"Potato",
            place:"Kozhikode",
            price:"200",
          },
        ],
        dialog: false,
    }
  },
}
</script>