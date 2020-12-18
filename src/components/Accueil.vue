<template lang="">
    <div>
        <h1 class="ml-2">Page d'accueil</h1>
        <div class="card mt-5 main-contenu">

            <p>Cette mini application à pour but :</p>
            
            <ul>
                <li>La pratique de VueJS et du routage avec vue-router</li>
                <li>La création d'une todo list</li>
                <li>La création d'un blog (via l'api jsonplaceholder)</li>
            </ul>

        </div>
    </div>
</template>
<script>
export default {
  name: "Accueil",
};
</script>
<style scoped>
.main-contenu {
  padding: 15px;
  margin: 15px;
}
ul{
    margin-left: 25px;
    list-style-type:'- ';
}
</style>