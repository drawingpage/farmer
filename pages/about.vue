<template>
    <div class="main">
        <h1 class="Farmer">Farmer</h1>
        <div class="messageBlock">
            <p class="message">{{msg}}</p>
        </div>
        
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
            msg:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim, aliquam eum dolorem atque mollitia cumque at, nemo aut doloremque debitis saepe dicta esse voluptates animi accusamus quos magni quaerat dignissimos."
        }
    }
}
</script>
