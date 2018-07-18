<link rel="stylesheet" href="../css/dater.css">
<template>
    <div class="dater">
        <ul class="dater-col">
            <li :click="onYear" v-for="item in [2016,2017,2018,2019,2020]">{{item}}</li>
        </ul>
        <ul class="dater-col"></ul>
        <ul class="dater-col"></ul>

    </div>
</template>
<script>
    export default {
        name: 'dater-el',
        props:["year"],
        data () {
            return {
               year:this.year
            }
        },
        methods:{
            onYear:function (e) {
                this.year = e.target.innerText;
                this.$emit("input",this.year);
            }
        }
    }
</script>