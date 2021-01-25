<template>

    <div>
        <h3> {{ name1 }} </h3>
    </div>

    <div>
        <h3> {{ aPasswordMethod('abc123') }} </h3>
    </div>

    <div>
        <h3> {{ myBoolean }} </h3>
        <button v-on:click="toggleMethod()"> 
          切換 </button>
    </div>

    <div>
        <h3> {{ aPlusMethod() }} </h3>
    </div>

    <div>
        <h3> {{ allData }} </h3>
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
