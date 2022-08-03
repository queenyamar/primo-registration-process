<template>
    <div class="main-body">
        <header>
            <logo-header></logo-header>
        </header>
        <main class="main-content">
            <register></register>
        </main>
        <footer>

        </footer>
    </div>
</template>

<script>
import LogoHeader from '../components/LogoHeader.vue'

export default {
    components: { LogoHeader },
    name: 'RegisterPage',
}
</script>