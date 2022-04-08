<template>
    <div>
        <h1 class="Farmer">Farmer</h1>
        <div class="messageBlock">
            <p class="message">{{msg}}</p>
        </div>
         <v-app class="main">
        <h1 class="Contact">Contact</h1>
         <v-card
            class="mx-auto"
            max-width="600"
            outlined
        >
            <v-list-item three-line>
            <v-list-item-content>
                <div class="text-overline mb-4">
                Farmer
                </div>
                <v-list-item-title class="text-h5 mb-1">
                {{name}}
                </v-list-item-title>
                <v-list-item-subtitle>{{contactDetails}}</v-list-item-subtitle>
            </v-list-item-content>
            <v-img
            class="image"
            :src=src>

            </v-img>
            </v-list-item>

            <v-card-actions>
            </v-card-actions>
        </v-card>
    </v-app>
    </div>
</template>
<style scoped>
.Farmer{
  color: orange;
  text-align: center;
  margin-top: 30px;
}
.message{
    font-family: 'Courier New', Courier, monospace;
    font-size: 16px;
    font-weight: 500;
    padding: 20px;
    letter-spacing: 0.5;
    

}
.Contact{
    color: orange;
    text-align: center;
    margin-top: 30px;
}
.image{
    width: 100px;
    height: 100px;
}

.messageBlock{
    padding:15px;
    width: 800px;
    height: auto;
    margin: auto;
    background-color: aqua;
    margin-top: 50px !important;
    border-radius: 10px;
    border: 2px solid black;
}
</style>
<script>
export default{
    data (){
        return {
            msg:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim, aliquam eum dolorem atque mollitia cumque at, nemo aut doloremque debitis saepe dicta esse voluptates animi accusamus quos magni quaerat dignissimos.",
            name:"Farmer",
            contactDetails:"farmer@gmail.com",
            src:'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        }
        }
    }

</script>
