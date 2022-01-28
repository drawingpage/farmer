<template>
  <div class="main">
    <div class="leftSideContainer container">
      <!-- logo -->
      <div class="image"></div>
      <!-- heading -->
      <h2 class="farm">Farmer</h2>
      <!-- buttons -->
      <v-btn
        class="navBtn"
        v-for="(button,i) in navbar"
        :key="i"
        >{{button.value}}
      </v-btn>
      <signUpPopUp />
    </div>
    <div class="rightSideContainer container">
      <!-- product list -->
      <div>
        <v-card
          v-for="(card , i) in cards"
          :key="i"
          class="mx-auto productCard"
        >
          <v-img
            class="white--text align-end"
            height="500px"
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
      </div>
    </div>
  </div>
</template>
<style scoped>
.shopBtn{
  background-color: #ff8800;
  color: rgb(255, 255, 255);
}
.productCard{
  width: 80%;
  margin: auto;
  margin-top: 30px;
}
.farm{
  text-align: center;
  color: rgb(255, 92, 51);
}
.navBtn{
  background-color: tomato;
  width: 100%;
  margin-top: 10px;
}
.image{
  background-image: url('https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg');
  background-size: contain;
  background-repeat: no-repeat;
  width: 100%;
  height: 200px;
}

.main{
  display: table;
  width: 100%;
  height: 100vh;
}
.leftSideContainer{
  position: fixed;
  height: 100vh;
  width: 20%;
  background-color: #e5e5e5;
}
.container{
  display: table-cell;
  }
.rightSideContainer{
  justify-content: center;
  justify-items: center;
  width: 80%;
  background-color: rgb(255, 255, 255);
}
</style>
<script>
import SignUpPopUp from '/home/ck/project/Linsa/farmer/farmers/components/signUpPopUp.vue'


export default {
  coponents: {
    SignUpPopUp,
  },
  data() {
    return {
      navbar: [
        {value: 'Home', path: '/'},
        {value: 'About', path: '/about'},
        {value: 'Contact', path: '/contact'},
        {value: 'SignIn/SignOut', path: '/contact'},
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