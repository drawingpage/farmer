<template>
    <v-app class="shopMain">
        <v-row
        class="details">
        <!-- first section -->
        <v-col
        class="firstD">
        <v-img
        :src="img"
        contain
        class="productImg"
        ></v-img>
        </v-col>
        <!-- second section -->
        <v-col
        class="secondD">
        <!-- product details -->
        <div class="productDetails">
                <h1 class="pName">{{pName}}</h1>
                <h2 class="pPrice">1{{mes}} = {{pPrice}}Rs</h2>
                <h3 class="pAvailable">Available Quqntity = {{pAvailable}}</h3>
                <h3 class="pDetails">{{pDetails}}</h3>
                
                    <form @submit.prevent="submit">
                        <v-select
                            class="qty"
                            :items="items"
                            label="Quantity"
                            outlined
                            ></v-select>
                    
                        <v-text-field
                        v-model="name"
                        :counter="10"
                        :error-messages="errors"
                        label="Name"
                        required
                        ></v-text-field>
                        <v-text-field
                        v-model="phoneNumber"
                        :counter="7"
                        :error-messages="errors"
                        label="Phone Number"
                        required
                        ></v-text-field>
                    
                        <v-text-field
                        v-model="email"
                        :error-messages="errors"
                        label="E-mail"
                        required
                        ></v-text-field>
                        <v-textarea
                        color="teal"
                        >
                        <template v-slot:label>
                            <div>
                            Address 
                            </div>
                        </template>
                        </v-textarea>
                    <v-btn
                        class="mr-4"
                        type="submit"
                        :disabled="invalid"
                    >
                        Buy Now
                    </v-btn>
                    <input class="reset" type="reset" >
                    </form>
        </div>
        </v-col>
        </v-row>
    </v-app>
</template>

<style scoped>
.reset{
  background-color: #e5e5e5e5;
  border: 1px solid rgb(180, 177, 177);
  height: 34px;
  padding: 0 16px;
  font-weight: 500;
  letter-spacing: 0.0892;
  border-radius: 5px;
  box-shadow: 0px 3px 1px -2px rgba(0 0 0 /20%),0px 2px 2px 0px rgba(0 0 0 /14%),0px 1px 5px 0px rgba(0 0 0 /12%),;
}
.reset:hover{
  background-color: aliceblue;
}
.qty{
    width: 250px;
    margin-top: 20px;
}
.sli{
    width: 200px;
    height: 300px;
}
.pDetails{
    width: 200px;
    height: auto;
}
.productDetails{
    padding: 60px;
    background-color: rgb(255, 255, 255);
    width: 600px;
    height: auto;
    margin-top: 40px;
    margin-left: 40px;
}
.productImg{
    margin-top: 100px !important;
    width: 600px;
    height: 600px;
    margin: auto;
    background-color: rgb(216, 200, 200);
}
.shopMain{
    background-color: rgb(226, 215, 215);
    width: 100%;
    height: 100vh;
}
.firstD{
    height: auto;
    background-color: aquamarine;
}
.secondD{
    height: auto;
    background-color: rgb(59, 224, 224);
}
</style>
<script>
export default {
    data() {
        return {
            pName:"hello",
            img:"kkkk",
            pPrice:"200",
            mes:"kg",
            pDetails:"helo bcdjgcd hscbsdc scn d gjv djhvdc dcygd sjcg dg udgc dsgc jdsgcudsg cdgcudg vugsduvgdug udgusdg",
            pAvailable:"50",
            min:0,
            max:10,
            items:[1,2,3,4,5],
        }
    }
}
</script>
