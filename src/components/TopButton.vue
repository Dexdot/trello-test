<template>
  <button type="button" v-on:click="moveOnTop"></button>
</template>

<script>
export default {
  methods: {
    moveOnTop() {
      this.$emit("top");
    },
  },
};
</script>

<style scoped>
button {
  position: fixed;
  bottom: 5px;
  right: 2px;
  border: none;
  outline: none;
  cursor: pointer;
  background-repeat: no-repeat;
  background-position: 50% 50%;
  height: 50px;
  width: 50px;
  transform: rotateY(0deg) rotate(-90deg);
  opacity: 0.9;
  background-color: #f09440;
  border-radius: 4px;
  z-index: 60;
  transition: 0.3s linear;
  background-image: url("../img/button.svg");
}

button:hover {
  opacity: 1;
}
</style>
