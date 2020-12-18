<template >
  <div class="header-top">
    <p>{{ titre }}</p>
  </div>
</template>
<script>
export default {
  name: "header-top",
  data() {
    return {
      titre: "To-Do liste",
    };
  },
};
</script>
<style scoped>
.header-top {
  position: fixed;
  top: 0;
  height: 50px;
  color: #f1f1f1;
  width: 100%;
  text-align: center;
  line-height: 50px;
  font-size: 25px;
  background: #333;
  z-index: 1000;
}
</style>