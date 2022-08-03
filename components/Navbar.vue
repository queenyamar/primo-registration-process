<template>
    <b-navbar class="primo-nav" toggleable="lg" type="light">
        <b-container>
            <b-navbar-brand>
                <NuxtLink to="/">
                    <b-img :src="require(`~/assets/images/primo-logo.png`)" fluid class="primo-nav__logo"></b-img>
                </NuxtLink>
            </b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav class="primo-nav__links">
                    <b-nav-item href="#" class="primo-nav__item">Features</b-nav-item>
                    <b-nav-item href="#" class="primo-nav__item">Why Primo</b-nav-item>
                    <b-nav-item href="#" class="primo-nav__item">Pricing</b-nav-item>
                    <b-nav-item href="#" class="primo-nav__item">Resources</b-nav-item>
                </b-navbar-nav>

                <!-- Right aligned nav items -->
                <b-navbar-nav class="ml-auto">
                    <b-button class="btn-blue">Login</b-button>
                </b-navbar-nav>
            </b-collapse>
        </b-container>
    </b-navbar>
</template>

<script>
export default {
}
</script>
