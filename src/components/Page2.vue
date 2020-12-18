<template lang="">
    <div>
        <h1>Page 2</h1>
        <div class="btn btn-warning" @click="goDebut">Retour au debut</div>
    </div>
</template>
<script>
export default {
  name: "page2",
  methods: {
    goDebut: function () {
      this.$router.push("/");
    },
  },
};
</script>
<style lang="">
</style>