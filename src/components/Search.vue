<template>
    <div class="Search">
        <input type="text" class="Search__input" v-model="query" @input="search">
        <button class="Search__button" @click="search">Найти</button>
    </div>
</template>

<script>
    export default {
        name: "Search",
        data() {
            return {
                query: ''
            }
        },
        methods: {
            search () {
                this.$store.dispatch('search', this.query)
            }
        }
    }
</script>

<style scoped>

</style>