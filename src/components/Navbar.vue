<!-- Navbar -->

<template>
    <header class="navbar-container">
        <button class="menu-button" @click="showMenu = !showMenu">
            <span class="menu-icon"></span>
        </button>
        <nav class="row row-sidebar" v-if="showMenu" @click="showMenu = false">    
            <router-link exact-active-class="active" to="/" class="column navbar-item font-white">Home</router-link>
            <router-link exact-active-class="active" to="/about-me" class="column navbar-item font-white">About&nbsp;me</router-link>
            <router-link exact-active-class="active" to="/experience" class="column navbar-item font-white">Experience</router-link>
            <router-link exact-active-class="active" to="/projects" class="column navbar-item font-white">Projects</router-link>
            <router-link exact-active-class="active" to="/contact" class="column navbar-item font-white">Contact</router-link>
        </nav>
    </header>
</template>
 
<style scoped>
    .navbar-container {
        display: flex;
        justify-content: space-between;
        width: 100%;
        left: 0;
        right: 0;
    }
    .navbar-item {
        font-size: 20px;
        line-height: 23px;
        font-weight: 400;
    }
    .active {
        color: #AD47FF;
    }
    .menu-button {
        width: 20px;
        display: none;
        background: none;
        border: none;
        cursor: pointer;
    }
    .menu-icon {
        display: block;
        width: 20px;
        height: 2px;
        background-color: #F8F8F8;
        border-radius: 2px;
        margin: 4px 0;
    }

    .menu-icon::before,
    .menu-icon::after {
        content: "";
        display: block;
        width: 20px;
        height: 2px;
        background-color: #F8F8F8;
        border-radius: 2px;
        margin: 4px 0;
    }

    .menu-icon::before {
        transform: translateY(-6px);
    }

    .menu-icon::after {
        transform: translateY(1px);
    }

    .row-sidebar {
        position: absolute;
        top: 0;
        left: 0;
        width: fit-content;
        background: #1F272F;
        box-shadow: 13px 12px 23px 2px rgba(99, 99, 99, 0.10);
        z-index: 1;
        padding: 20px;
        /* border: 1px solid #F8F8F8; */
        border-radius: 0 0 0 10px;
    }

    .navbar-container {
        flex-direction: row-reverse;
    }
    .menu-button {
        display: block;
    }
    .navbar-item {
        display: block;
        margin: 10px 0;
    }
</style>

<script>
export default {
    data() {
        return {
            showMenu: false
        }
    }
}
</script>