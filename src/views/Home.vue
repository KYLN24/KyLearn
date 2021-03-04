<template>
    <div class="home">
        <NavBar
            topics="[
                { title: '首页', link: 'home' }
            ]"
            currentNav="1"
        ></NavBar>
    </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/NavBar.vue";

export default {
    name: "Home",
    components: {
        NavBar
    }
};
</script>
