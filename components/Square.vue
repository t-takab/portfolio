<template>
  <div
    class="box"
    :class="{ 'toggle-color': isToggle }"
    @click="toggleColor"
  ></div>
</template>

<script>
export default {
  data() {
    return {
      isToggle: false,
    }
  },
  methods: {
    toggleColor() {
      this.isToggle = !this.isToggle
    },
  },
}
</script>

<style scoped>
.box {
  width: 200px;
  height: 200px;
  background-color: #0ff;
}

.toggle-color {
  background-color: orange;
}
</style>
