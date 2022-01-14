<template>
    <h1>{{ msg }}</h1>

    <p>{{ moment(new Date()).format('dddd LL') }}</p>
    <!-- <p>{{ new Date() }}</p> -->

</template>

<script>
    import moment from 'moment';

    export default {
        name: 'HelloWorld',
        props: {
            msg: String
        },
        created: function () {
            this.moment = moment;
        }
    }
</script>

<style>
    
</style>
