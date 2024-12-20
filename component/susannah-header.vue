<template>
    <div class="header-cont borderbox align-center">
        <div class="flex-row space-between block align-center">
            <!--Logo-->
            <div class="logo">
                <nuxt-link to="/" class="menu-item">Susannah Harmon Furr</nuxt-link>
            </div>
            <div class="block flex-row ">
                <div class="block borderbox">
                    <!--Main Menu-->
                    <div class="header-nav-list flex-row">
                        <div class="block">
                            <nuxt-link to="/booking" class="menu-item" exact-active-class="active">booking</nuxt-link>
                        </div>
                        <div class="block">
                            <nuxt-link to="/uncertainty" class="menu-item" exact-active-class="active">uncertainty</nuxt-link>
                        </div>
                        <div class="block">
                            <nuxt-link to="/pronk" class="menu-item" exact-active-class="active">pronk</nuxt-link>
                        </div>
                        <div class="block">
                            <nuxt-link to="/interiors" class="menu-item" exact-active-class="active">interiors</nuxt-link>
                        </div>
                        <div class="block">
                            <nuxt-link to="/manifesto" class="menu-item" exact-active-class="active">manifesto</nuxt-link>
                        </div>
                    </div>
                    <!--Mobile Menu-->
                    <div class="mobile-menu">
                        <menu-icon :isOpen="isMenuVisible" @toggle-menu="toggleMenu" />
                        <mobile-menu :isVisible="isMenuVisible" @toggle-menu="toggleMenu" />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import mobileMenu from './mobile-menu.vue';
import menuIcon from './menu-icon.vue';
export default {
  components: { mobileMenu, menuIcon },
    data() {
        return {
            isMenuVisible: false
        }
    },
    methods: {
        toggleMenu() {
            this.isMenuVisible = !this.isMenuVisible;
        }
    }
}
</script>