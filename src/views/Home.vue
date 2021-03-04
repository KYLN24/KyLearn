<template>
    <div class="home">
        <KyHeader :topics="topics" :currentNav="currentNav" about=true></KyHeader>
        <router-view />
    </div>
</template>

<script>
// @ is an alias to /src
import KyHeader from "@/components/KyHeader.vue";

export default {
    name: "Home",
    date() {
        return {
            topics: [
                { title: '首页', link: '/' },
                { title: '首页', link: '/' }
            ],
            currentNav: 1
        };
    },
    components: {
        KyHeader
    }
};
</script>
