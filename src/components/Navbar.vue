<!-- Navbar -->

<template>
    <div class="navbar-container">
        <div class="container">
            <nav class="row">    
                <router-link exact-active-class="active" to="/" class="column navbar-item font-white">Home</router-link>
                <router-link exact-active-class="active" to="/about" class="column navbar-item font-white">About&nbsp;me</router-link>
                <router-link exact-active-class="active" to="/experience" class="column navbar-item font-white">Experience</router-link>
                <router-link exact-active-class="active" to="/projects" class="column navbar-item font-white">Projects</router-link>
                <router-link exact-active-class="active" to="/contact" class="column navbar-item font-white">Contact</router-link>
            </nav>
        </div>
    </div>
</template>
 
<style scoped>
    .navbar-container {
        width: fit-content;
        margin-left: auto;
    }
    .navbar-item {
        font-size: 20px;
        line-height: 23px;
        font-weight: 400;
    }
    .active {
        color: #AD47FF;
    }
</style>