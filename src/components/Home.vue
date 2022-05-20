<template>
    <h1> Hello from home component </h1>
    <p> Written by {{ MyName }}</p>
    <input v-model="text" >
    <p> You have written {{ text }}</p>
    <span v-for="word in listofwords.entries()" :key="word" style="width:100%">
        <span :id="color[word[0] % 5]">
            {{ word[1] + " " }}
        </span>
    </span>
</template>

<script>

export default {
  name: 'MyHome',
  data()
  {
    return{
    MyName: "Tanvish",
    text: "",
    index: 0,
    color: ["red","blue","orange","green","yellow"]
    }
  },
  computed:{
    listofwords(){
        return this.text.split(" ");
    },
  }
}
</script>

<style>
#red{
    color: red
}
#yellow{
    color: yellow
}
#green{
    color:green
}
#blue{
    color:blue
}
#orange{
    color:orange
}
</style>
