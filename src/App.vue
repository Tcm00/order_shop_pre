<template>
    <div id="app">
        <!--keep-alive 表示页面不会被销毁，即保持页面状态-->
        <keep-alive>
            <router-view v-if="$route.meta.keepalive"></router-view>
        </keep-alive>
        <router-view v-if="!$route.meta.keepalive"></router-view>
    </div>
</template>

<script>
export default {
    name: "App",
};
</script>

<style>
* {
    margin: 0;
    padding: 0;
}
body {
    font-size: 4.1vw;
    overscroll-behavior-y: none;
}
#app {
    width: 100vw;
    height: 100vh;
    overflow-x: hidden;
    overflow-y: auto;
}
</style>
