<template>
    <div class="hello">
        <nav class="topnav">
            <router-link
                v-for="(item, index) in this.props.topics"
                :key="index"
                to="item.link"
                >{{ item.title }}</router-link
            >
            <router-link
                v-if="this.props.about"
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
    name: "NavBar",
    props: {
        topics: [],
        currentNav: Number,
        about: Boolean(false)
    }
};
</script>

<style scoped>
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
