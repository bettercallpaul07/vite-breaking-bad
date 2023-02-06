<script>


export default {
    name: "AppMain"
}
</script>

<template>
    <main class="py-3">
        <div class="container">

            <div class="row row-cols-1 row-cols-sm-2 row-cols-md-3 row-cols-lg-4 g-4">
                <div class="col text-center" v-for="character in charactersList">
                    <div>
                        <img src="https://via.placeholder.com/300" class="img-fluid" alt="">
                    </div>
                    <div>
                        <h3 class="mb-4">Character Name</h3>
                        <h5>Character Status</h5>
                        <h5>Character Specs</h5>

                    </div>
                </div>


            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>

</style>