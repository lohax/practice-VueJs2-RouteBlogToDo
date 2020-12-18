<template>
  <div class="main-contenu">
    <h2>{{ titre }}</h2>
    <form>
      <div class="form-group">
        <label for="nouveau">Action</label>
        <input type="text" class="form-control" v-model="formData.tempTodo" />
      </div>
      <button type="submit" class="btn btn-primary" @click.prevent="addTodo">
        Créer la tâche
      </button>
    </form>

    <ul>
      <li v-for="(todo, i) in todolst" :key="i">
        <todo :id="i" :todo="todo" :delTodo="delTodo" />
      </li>
    </ul>

  </div>
</template>
<script>
import Todo from "./Todo";
export default {
  name: "contenu",
  data() {
    return {
      titre: "Rentrer un To-Do",
      formData : {
        tempTodo: "",
      },
      todolst: ["TypeScript", "Symphony", "Jest", "Redux"],
    };
  },
  methods: {
    addTodo: function () {
      this.todolst.push(this.formData.tempTodo);
      this.formData.tempTodo = "";
    },
    delTodo: function (e) {
      this.todolst.splice(e.target.parentNode.id, 1);
    },
  },
  components: {
    'todo': Todo,
  },
};
</script>
<style >
.main-contenu {
  margin-top: 60px;
  padding: 15px;
}
ul {
 list-style-type: none;
 padding: 0;
}
</style>