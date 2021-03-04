<template>
    <div id="app">
        <KyHeader
            :topics="topics"
            :currentNav="currentNav"
            :about="true"
        ></KyHeader>
        <router-view />
    </div>
</template>

<script>
import KyHeader from "@/components/KyHeader.vue";

export default {
    data() {
        return {
            topics: [
                { title: "首页", link: "/" },
                { title: "时间线", link: "/timeline" }
            ],
            currentNav: 1
        };
    },
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
    text-align: center;
    color: #2c3e50;
}
</style>
