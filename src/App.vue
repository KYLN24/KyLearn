<template>
    <div id="app">
        <KyHeader />
        <router-view />
    </div>
</template>

<script>
import KyHeader from "@/components/KyHeader.vue";

export default {
    components: {
        KyHeader
    }
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
}
</style>
