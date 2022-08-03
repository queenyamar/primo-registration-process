<template>
    <div class="main-body">
        <header>
            <logo-header></logo-header>
        </header>
        <main class="main-content">
            <organization-info></organization-info>
        </main>
        <footer>

        </footer>
    </div>
</template>

<script>
import LogoHeader from '../components/LogoHeader.vue'

export default {
    components: { LogoHeader },
    name: 'OrganizationInfoPage',
}
</script>