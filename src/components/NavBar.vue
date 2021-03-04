<template>
    <div class="hello">
        <nav class="topnav">
            <router-link
                v-for="(item, index) in this.props.topics"
                :key="index"
                :to="item.link"
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
    name: "NavBar"
    // props: {
    //     topics: [{ title: String, link: String }],
    //     currentNav: Number,
    //     about: Boolean(false)
    // }
};
</script>

<style scoped>
nav.topnav {
    height: 2em;
    background-color: grey;
    overflow: hidden;
}

nav.topnav a {
    height: 2em;
    padding: 0.25em 0.25em 0 0.25em;
    display: block;
    float: left;
    border-right: 1px solid rgb(180, 180, 180);
    color: white;
    text-decoration: none;
}

nav.topnav a:last-child {
    border-right: 0;
}

nav.topnav a.currentNav {
    background-color: steelblue;
}

nav.topnav a:hover {
    background-color: lightsteelblue;
}

nav.topnav a:active {
    background-color: grey;
}
</style>
