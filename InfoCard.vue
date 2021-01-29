<template>
    <div>
        <h2>...</h2>
        <button v-on:click="toggleFavorite>
    </div>
</template>

<script>
export default {
    props: [
        'name'
    ],
    emits: ['toggle-method'],
    methods: {
        toggleFavorite(){
            this.$emit('toggle-method');
        }
    }
}
</script>
