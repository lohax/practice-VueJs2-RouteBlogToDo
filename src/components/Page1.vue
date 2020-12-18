<template lang="">
    <div>
        <h1>Les articles de blog</h1>
        <hr>

        <ul>
            <li v-for="(article, index) in allArticles" :key="index">
                
                <router-link :to="`blogpost/${index+1}`">
                    <div class="card m-2 postTitle">
                        <h3>{{ article.title }}</h3>
                    </div>
                </router-link>

            </li>
        </ul>

        <div class="btn btn-warning" @click="goDebut">Retour au debut</div>
    </div>
</template>
<script>
import axios from "axios";

export default {
  name: "page1",
  data() {
    return {
      allArticles: [],
    };
  },
  methods: {
    goDebut: function () {
      this.$router.push("/");
    },
  },
  created() {
    axios.get("https://jsonplaceholder.typicode.com/posts").then((response) => {
      for (const blogPost of response.data) {
        this.allArticles.push(blogPost);
      }
    });
  },
};
</script>
<style scoped>
ul{
    list-style-type:decimal-leading-zero
}
.postTitle{
    padding: 10px;
}
</style>