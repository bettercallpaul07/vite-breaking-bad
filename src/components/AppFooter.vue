<script>
export default {
    name: "AppFooter",
    props: {
        charactersCount: {
            type: Number,
            default: 0
        }
    }
}
</script>

<template>
    <footer class="py-4">
        <div class="container">
            <strong>
                Found {{charactersCount}} characters
            </strong>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
</style>