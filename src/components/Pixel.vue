<template>
  <div @click="changeColor(color)" :class="['pixel', color, current ? 'current' : '']" ></div>
</template>
<script>
export default {
  name: "Pixel",
  props: {
    color: String,
    current: Boolean
  },
  methods: {
    changeColor: function(color) {
      this.$root.$emit('updatecolor', color)
    }
  }
};
</script>
<style scoped>
.pixel {
  border: 1px solid lightgray;
  width: 30px;
  height: 30px;
  box-sizing: border-box;
}
.white {
  background-color: white;
}
.lightblue {
  background-color: rgb(0, 188, 212);
}
.blue {
  background-color: rgb(3, 169, 244);
}
.darkblue {
  background-color: rgb(33, 150, 243);
}
.pixel.current {
  border: 4px solid brown;
}

</style>
