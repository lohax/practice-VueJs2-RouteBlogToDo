<template lang="">
    <div class="article">
        <h1>Le post numero {{ id }}</h1>
        <div>
            <h2>{{ articleUnique.title }}</h2>
            <br>
            <p>
                {{ articleUnique.body }}
            </p>
        </div>

        <div class="btn btn-warning" @click="goDebut">Retour</div>
    </div>
</template>
<script>
import axios from 'axios'
export default {
  name: "Post",
  data(){
      return {
          id: this.$route.params.id,
          articleUnique: []
      }
  },
  methods: {
    goDebut: function () {
      this.$router.push("/Page1");
    },
  },
  mounted() {
    axios
    .get(`https://jsonplaceholder.typicode.com/posts/${this.id}`)
    .then((response) => {
      this.articleUnique = response.data
    });
  },
};
</script>
<style scoped>
.article{
    margin: 20px;
}

</style>