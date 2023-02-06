<script>
import SearchForm from "./SearchForm.vue"

export default {
    name: "AppHeader",
    components: {
        SearchForm
    }
}
</script>

<template>
    <header class="my-5">

        <div class="container text-center">

            <h1>
                Yu-Gi-Oh App
            </h1>

            <SearchForm />

        </div>
    </header>



</template>

<style lang="scss" scoped>

</style>