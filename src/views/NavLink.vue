<template>
    <nav class="nav">
        <div>
            <router-link to="/" exact active-class = "active"> Accueil </router-link>
            <router-link to="ajout" exact active-class = "active"> Ajout </router-link>
            <router-link to="about" exact active-class = "active"> A propos </router-link>
        </div>
    </nav>
</template>

<script>
    export default {
        name: "NavLink",
        props: {
            url:String,
            text: String
        }
    }
</script>

<style lang="scss" scoped>
   .nav {
        box-shadow: 0px 1px 10px rgba(5,5,5,0.3);
        padding: 1rem;
        div {
            width: 50%;
            display: flex;
            justify-content: space-around;
        }
   }
   .active {
       color: green;
   }
</style>