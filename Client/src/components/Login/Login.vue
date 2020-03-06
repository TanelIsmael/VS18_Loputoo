<template>
    <section>
        <h1 class="heading">IKT-osakonna praktika</h1>
        <LoginForm />
    </section>
</template>

<script>
import LoginForm from '@/components/Login/Loginform.vue'



export default {
    components: {
        LoginForm
    }
};

</script>

<style lang="scss" scoped>
    section {
        text-align: center;
        padding: 20px;
        margin-bottom: 202px;

        .heading {
            color:#404040;
            font-family: 'Source Sans Pro', sans-serif;
            font-size: 2.8rem;
            margin-bottom: 90px;
        }
    }
</style>