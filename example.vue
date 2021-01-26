<template>
    <info-card
        name="Tom"
        phone-number="0912345678"
        email-address="test@gmail.com"
        :is-favorite="false"
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
                name1: 'value1',
                name2: 'value2',
                myBoolean: true,
                myNumber: 1
            }
        },
        methods: {
            aPasswordMethod(someText){
                if (someText === 'abc123'){
                  return 'success';
                }else{
                  return 'failed';
                }
            },
            toggleMethod() {
                this.myBoolean = !this.myBoolean;
            }
        },
        computed: {
            allData() {
                console.log('allData had been triggered!');
                return this.name1 + this.name2;
            }
        },
        watch: {
            myBoolean(){
                alert('myBoolean had been changed!');
            }
        }
    };
</script>
