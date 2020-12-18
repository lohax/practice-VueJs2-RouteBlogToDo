<template >
  <div class="card my-2 item-todo">
      <p>{{ todo }}</p>
      <button class="deltodo btn btn-danger" @click="delTodo">X</button>
  </div>
</template>
<script>
export default {
  name: "todo",
  props: ["todo", "delTodo"],
};
</script>
<style scoped>
.item-todo {
  position: relative;
  padding: 20px 60px 20px 30px;
  font-size: 20px;
  height: 80px;
}
.deltodo {
  position: absolute;
  top: 18px;
  right: 10px;
}
.item-todo p {
  margin-bottom: 0 !important;
}
</style>