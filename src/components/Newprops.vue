<template>
    <div>
        <!-- <p>{{firstname}}</p>
        <p>{{secondname}}</p>
        <p>{{age}}</p>
        <button @click="update()">click</button> -->
        <p>{{firstname}}</p>
        <p>{{secondname}}</p>
        <p>{{age}}</p>
        <button @click="update()">click</button>
        <button @click="updateName()">name change</button>
    </div>
</template>
<script>
    export default{
        // props: {
        //    firstname: String,
        //    secondname: String,
        //    age: Number
        // },
        // methods: {
        //     update(){
        //         // this.firstname = 'md';
        //         this.$emit('updateValue','Mohammad');
        //     }
        // }
        props: {
            firstname: String,
            secondname: String,
            age: Number
        },
        methods: {
            update(){
                this.$emit('updateValue',26);
            },
            updateName(){
                this.$emit('updateNamevalue','Mohammad');
            }
        }
    }
</script>
<style scoped>

</style>
