<template>
    <div class="menu-overlay" v-if="isVisible" @click="toggleMenu">
        <p class="logo">Susannah Harmon Furr</p>
        <nav @click.stop>
            <ul>
                <li>
                    <nuxt-link to="/author" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>author</p>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/pronk" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>pronk</p>
                    </nuxt-link>
                </li>
                <li>

                    <nuxt-link to="/interiors" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>interiors</p>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/booking" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>booking</p>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/about" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>about</p>
                    </nuxt-link>
                </li>
            </ul>
        </nav>
        <div class="flex-row socials align-center">
            <a href="https://www.linkedin.com/in/susannah-furr-21375b251/?original_referer=https%3A%2F%2Fwww.google.com%2F"><img src="/img/linkedin.png" class="social" alt=""></a>
            <a href="https://www.instagram.com/susannahfurr"><img class="social" src="/img/insta.webp" alt=""></a>    
        </div>
        
    </div>
</template>

<script>
export default {
    props: {
        isVisible: {
            type: Boolean,
            required: true
        }
    },
    methods: {
        toggleMenu() {
            this.$emit('toggle-menu');
        },
        closeMenu() {
            this.$emit('toggle-menu');
        }
    }
}
</script>