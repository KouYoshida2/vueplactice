<template>
  <div>
    id:{{ id }}<br />
    title:{{ title }}<br />
    iamge:{{ image }}<br />
    description:{{ description }}
  </div>
</template>

<script>
export default {
  // name: "CardComponent",
  props: {
    id: Number,
    title: String,
    image: String,
    description: String,
  },
};
</script>

<style></style>
