<template>
    <div>
        ...
        <button v-on:click="toggleFavorite>
    </div>
</template>

<script>
export default {
    props: [
        ...
    ],
    emits: ['toggle-method'],
    methods: {
        toggleFavorite(){
            this.$emit('toggle-method');
        }
    }
}
</script>
