<style scoped>
nav {
    list-style-type: none;
    top: 0;
    left: 0;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: rgb(24, 24, 24);
    position: fixed;
    top: 0;
    width: 100%;
}

nav a {
    float: left;
}

nav a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 20px;
    text-decoration: none;
}

nav a:hover:not(.active) {
    background-color: rgb(0, 0, 0);
    padding: 14px 19px;
    border-right: solid 1px;
    border-left: solid 1px;
}
</style>
<template>
    <nav>
        <router-link to="/">MijnCV</router-link>
        <div v-for="Page in Pages">
            <a :href="'#' + Page.name">{{ Page.name }}</a>
        </div>
    </nav>
</template>

<script>
import axios from 'axios';

export default {
    props: {
        ID: null,
        Pages: null,
    },
}
</script>