<template>
    <div class="ky-header">
        <a id="bigTitle" href="/"><h1>KYLN 的学习路径</h1></a>
        <nav class="topnav">
            <router-link
                v-for="(item, index) in topics"
                :class="{ currentNav: currentNav == index }"
                :key="index"
                :to="item.link"
                @click.left.native="navTo(index)"
                >{{ item.title }}</router-link
            >
            <div id="rightNav">
                <div id="globalSearch">
                    <input type="text" />
                    <input type="button" value="搜索" />
                </div>
                <router-link
                    v-if="about"
                    :class="{ currentNav: currentNav == -1 }"
                    id="about"
                    to="/about"
                    @click.left.native="navTo(-1)"
                    >关于</router-link
                >
            </div>
        </nav>
    </div>
</template>

<script>
export default {
    name: "KyHeader",
    data() {
        return {
            currentNav: 0,
            topics: [
                { title: "首页", link: "/" },
                { title: "时间线", link: "/timeline" }
            ],
            about: true
        };
    },
    methods: {
        navTo(index) {
            this.currentNav = index;
        }
    }
};
</script>

<style scoped>
#bigTitle {
    margin-left: 2em;
    margin-right: auto;
    color: black;
    text-decoration: none;
}

#rightNav {
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

#rightNav a {
    border-left: 1px solid rgb(180, 180, 180);
    margin-right: 0;
}

#globalSearch {
    border: 0;
    padding: 0;
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
    background-color: rgb(211, 211, 211);
}
</style>
