<template>
    <info-card
        name="Tom"
        phone-number="0912345678"
        email-address="test@gmail.com"
        v-bind:is-favorite="isFavorite"
        v-on:toggle-method="changeStatusMethod()"
    ></info-card>
</template>

<script>
    import InfoCard from './components/UI/InfoCard.vue';
    export default{
        components:{
            InfoCard
        },
        data() {
            return {
                isFavorite: false
            }
        },
        methods: {
            changeStatusMethod(){
                this.isFavorite = !this.isFavorite;
            }
        }
    };
</script>
