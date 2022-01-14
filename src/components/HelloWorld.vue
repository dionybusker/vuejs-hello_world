<template>
    <h1>{{ msg }}</h1>

    <p>{{ moment(new Date()).format('dddd LL') }}</p>
    
    <div>
        <input v-model="num" type="number" />

        <p>Number: {{ num + counter }}</p>

        <button @click="counter += num">Add</button>
    </div>

</template>

<script>
    import moment from 'moment';

    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        },
        data() {
            return {
                num: 0,
                counter: 0
            }
        },
        created: function () {
            this.moment = moment;
        }
    }
</script>

<style>
    
</style>
