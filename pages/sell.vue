<template >
<div class="main">
<v-app class="container">
    <h1>Upload your product</h1>
    <form @submit.prevent="submit">
        <v-text-field
        v-model="name"
        :error-messages="errors"
        label="Product name"
        required
        ></v-text-field>
        <v-text-field
        v-model="phoneNumber"
        :counter="10"
        :error-messages="errors"
        label="Phone Number"
        required
        ></v-text-field>
        <v-select
          class="qty"
          :items="items"
          v-model="Quantity"
          label="Quantity"
          outlined
          ></v-select>
        <v-textarea
        color="teal"
        v-model="details"
        >
        <template v-slot:label>
            <div>
            Details 
            </div>
        </template>
        </v-textarea>
        <v-file-input
        v-model="pImage"
        :rules="rules"
        accept="image/png, image/jpeg, image/bmp"
        prepend-icon="mdi-camera"
        label="product"
      ></v-file-input>
    <v-btn
        class="mr-4"
        type="submit"
        :disabled="invalid"
    >
        Sell
    </v-btn>
    <input type="reset" class="reset">
    </form>

</v-app>
</div>
</template>
<style scoped>
.main{
  background-color:#e5e5e5e5;
  padding: 20px;
}
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
.container{
    width: 400px;
    background-color: white;
    border: 2px solid black;
    border-radius: 5px;
    height: auto;
}
</style>
<script>
  export default {
    data (){
      return{
      rules: [
        value => !value || value.size < 2000000 || 'Avatar size should be less than 2 MB!',
      ],
      items:[1,2,3,4,5],
      }
    },
    
    
  }
</script>