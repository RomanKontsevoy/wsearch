<template>
    <div class="Results">
        <div class="Item" v-for="item in results" :key="item.title.substr(0,10)">
            <a :href="item.url" class="Item__title">{{item.title}}</a>
            <a :href="item.url" class="Item__url">{{item.url}}</a>
            <a :href="item.url" class="Item__snippet" v-html="item.snippet"></a>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Results",
        computed: {
            results() {
                return this.$store.getters.results
            }
        }
    }
</script>

<style scoped>

</style>