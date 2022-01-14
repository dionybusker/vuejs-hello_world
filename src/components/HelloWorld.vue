<template>
    <h1>{{ msg }}</h1>

    <p>{{ moment(new Date()).format('dddd LL') }}</p>
    
    <div>
        <input v-model="num" />

        <p>Number: {{ num }}</p>
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
                num: ''
            }
        },
        created: function () {
            this.moment = moment;
        }
    }
</script>

<style>
    
</style>
