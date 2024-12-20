<template>
    <div class="menu-overlay" v-if="isVisible" @click="toggleMenu">
        <nav @click.stop>
            <ul>
                <li>
                    <nuxt-link to="/booking" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>booking</p>
                    </nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/uncertainty" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>uncertainty</p>
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
                    <nuxt-link to="/manifesto" class="menu-item" @click="closeMenu" exact-active-class="active">
                        <p>manifesto</p>
                    </nuxt-link>
                </li>
            </ul>
        </nav>
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