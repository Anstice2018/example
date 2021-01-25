<template>
    <div>
        <h3> {{ variable1(1,1) }} </h3>
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


