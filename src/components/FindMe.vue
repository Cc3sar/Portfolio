<template>
    <footer class="container find-me">
        <button class="menu-button" @click="toggleMenu">
            <span class="icon-wrapper">
                <img src="@assets/icons/connect-with-me.svg" alt="Hi" class="connect-icon" />
                <!-- <span class="icon-indicator">+</span> -->
                <span class="font-violet back-arrow" v-if="menu">
                    ←
                </span>
            </span>
            <span class="font-white find-me-text" v-if="!menu">
                Discover Me
            </span>
        </button>
        <nav class="find-me-icons row" v-if="menu">
        <a href="https://github.com/Cc3sar" target="_blank">
            <img src="@assets/icons/github.svg" alt="github" class="find-me-icon" />
        </a>
        <a href="https://www.linkedin.com/in/cesar-peren" target="_blank">
            <img src="@assets/icons/linkedin.svg" alt="linkedin" class="find-me-icon" />
        </a>
        </nav>
    </footer>
</template>
  
<style scoped>
    .find-me {
        display: flex;
        align-items: center;
        position: fixed;
        bottom: 10%;
        left: 0;
    }
    
    .menu-button {
        background-color: transparent;
        border: none;
        cursor: pointer;
        padding: 0;
        margin: 0;
        display: flex;
        align-items: center;
    }

    .icon-wrapper {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-right: 0.5em;
    }

    .find-me-text {
        font-size: 1.5em;
        font-weight: 400;
    }

    .back-arrow {
        font-size: 4em;
        font-weight: 400;
    }

    .connect-icon {
        width: 60px;
        height: 60px;
        animation: spin 5s linear infinite;
    }

    @keyframes spin {
        0% {
            transform: rotate(0deg);
        }
        100% {
            transform: rotate(360deg);
        }
    }

    .find-me-icons {
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    .find-me-icons a {
        margin: 0 1em;
        width: 60px;
        height: 60px;
    } 
</style>
  
<script>
    import { ref } from 'vue';

    export default {
    setup() {
            const menu = ref(false);
    
            const toggleMenu = () => {
                menu.value = !menu.value;
            };

            return {
                menu,
                toggleMenu,
            };
        },
    };
</script>