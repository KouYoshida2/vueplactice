<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div class="cards">
    <div v-for="(item, index) in items" :key="index">
      <CardComponent
        :id="item.id"
        :image="item.image"
        :title="item.title"
        :description="item.description"
      />
    </div>
  </div>
  <HelloWorld @parent="parent" msg="propsで書き換えました。"></HelloWorld>
</template>

<script>
import HelloWorld from "@/components/HelloWorld.vue";
import CardComponent from "@/components/CardComponent";

export default {
  name: "App",
  components: {
    HelloWorld,
    CardComponent,
  },
  methods: {
    parent: function (e) {
      console.log(e);
    },
  },
  data() {
    return {
      items: [
        {
          id: 1,
          title: "タイトル1",
          image: "img1.jpg",
          description: "詳細1",
        },
        {
          id: 2,
          title: "タイトル2",
          image: "img2.jpg",
          description: "詳細2",
        },
        {
          id: 3,
          title: "タイトル3",
          image: "img3.jpg",
          description: "詳細3",
        },
      ],
    };
  },
};
</script>

<style>
.cards {
  display: flex;
  justify-content: space-around;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
