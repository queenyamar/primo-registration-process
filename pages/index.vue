<template>
    <div class="main-body">
        <header>
            <navbar></navbar>
        </header>
        <main class="main-content">
            <hero-banner></hero-banner>
        </main>
        <footer>

        </footer>
    </div>
</template>

<script>
import Navbar from '../components/Navbar.vue'
    export default {
  components: { Navbar },
        name: 'IndexPage'
    }
</script>
