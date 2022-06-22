<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <div v-for="item in items" :key="item.name">
    <span>{{item.name}}</span> : <span>{{item.age}}</span>
    </div>
    <!-- <button @click="btnClick">click me!</button> -->
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <h1>this is voting page</h1>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
  },
  data () {
    return {
      items: [
      {name: "john", age: 31},
      {name: "tom", age: 12},
      {name: "danny", age: 22},
      {name: "lydia", age: 30},
      {name: "elenca", age: 31},
    ]
    }

  }
  // methods: {
  //   btnClick() {
  //     alert("button clicked");
  //   }
  // }
};
</script>
