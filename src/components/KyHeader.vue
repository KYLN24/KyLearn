<template>
    <div class="ky-header">
        <h1><a id="bigTitle" href="/">KYLN 的学习路径</a></h1>
        <nav class="topnav">
            <router-link
                v-for="(item, index) in topics"
                :key="index"
                :to="item.link"
                >{{ item.title }}</router-link
            >
            <router-link
                v-if="about"
                id="about"
                style="float: right; border-left: 1px solid rgb(180, 180, 180)"
                to="/about"
                >关于</router-link
            >
        </nav>
    </div>
</template>

<script>
export default {
    name: "KyHeader",
    props: {
        topics: Array,
        currentNav: Number,
        about: Boolean(false)
    }
};
</script>

<style scoped>
#bigTitle {
    color: black;
    text-decoration: none;
}

.topnav {
    height: 2em;
    background-color: grey;
    overflow: hidden;
}

.topnav a {
    height: 2em;
    padding: 0.25em 0.25em 0 0.25em;
    display: block;
    float: left;
    border-right: 1px solid rgb(180, 180, 180);
    color: white;
    text-decoration: none;
}

.topnav a:last-child {
    border-right: 0;
}

.topnav a.currentNav {
    background-color: steelblue;
}

.topnav a:hover {
    background-color: lightsteelblue;
}

.topnav a:active {
    background-color: grey;
}
</style>
