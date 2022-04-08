<template>
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
</template>
<style scoped>
.Contact{
    color: orange;
    text-align: center;
    margin-top: 30px;
}
.image{
    width: 100px;
    height: 100px;
}
</style>    
<script>

export default{
    data(){
        return {
            name:"Farmer",
            contactDetails:"farmer@gmail.com",
            src:'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        }
    }
}
</script>
