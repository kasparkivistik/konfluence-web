<template>
  <div class="wrapper">
    <slot name="content">
      <div class="text-padding">
        <h1 class="title">
          {{ title }}
        </h1>
        <p>{{ text }}</p>
      </div>
    </slot>
  </div>
</template>

<script>

export default {
  name: "Wrapper",
  components: {

  },
  props: {
    title: String,
    text: String
  }
}
</script>

<style scoped>
    .wrapper {
      background-color: #FFFFFF;
      border-radius: 1.5rem;
      overflow: hidden;
      padding: 0;
      margin: 10rem 0;
      text-align: justify;
      z-index: 10;
      position: relative;
    }

   .text-padding {
     padding: 2rem;
   }

  @media (max-width: 900px) {
    .wrapper {
      margin: 3.5rem 0.8rem 0 0.8rem;
    }
  }
</style>
