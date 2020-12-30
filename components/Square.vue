<template>
  <div
    class="box"
    :style="{ 'background-color': displayColor }"
    @click="toggleColor"
  ></div>
</template>

<script>
export default {
  props: {
    primaryColor: String,
    secondaryColor: String,
  },
  data() {
    return {
      displayColor: this.primaryColor,
      first: this.primaryColor,
      second: this.secondaryColor,
    }
  },
  methods: {
    toggleColor() {
      console.log('primary_color' + this.primaryColor)
      console.log('secondary_color' + this.secondaryColor)
      console.log('display_color' + this.displayColor)
      if (this.displayColor === this.first) {
        this.displayColor = this.second
      } else {
        this.displayColor = this.first
      }
    },
  },
}
</script>

<style scoped>
.box {
  width: 200px;
  height: 200px;
}
</style>
