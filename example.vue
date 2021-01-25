<template>
    <div>
        <h3> {{ myBoolean }} </h3>
        <button v-on:click="toggleMethod()"> 切換 </button>
    </div>
</template>

<script>
    export default{
        data() {
            return {
                name1: 'value1',
                name2: 'value2',
                myBoolean: true,
                myNumber: 1
            }
        },
        methods: {
            toggleMethod() {
                this.myboolean = !this.myboolean
            },
            aPlusMethod(a, b){
                return{
                    a+b;
                }
            }
        },
        computed: {
            variable1(a, b) {
                return {
                    a+b;
                }
            }
        },
        watch: {
            myBoolean(){
                alert('myBoolean has been changed!');
            },
            aPlusMethod(){
                alert('aPlusMethod has been triggered!');
            }
        }
    }
</script>


