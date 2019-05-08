<template>


    <div>
        <div class="card" v-for="(item, index) in elements" :key="index" :offset="index > 0 ? 2 : 0">
            <img src="https://shadow.elemecdn.com/app/element/hamburger.9cf7b091-55e9-11e9-a976-7f4d0b07eef6.png" alt="Avatar" class="image">
            <div class="container">
                <h4><b>{{item.name}}</b></h4>
                <p>{{info}}</p>
            </div>
        </div>
    </div>

    
</template>

<script>
    import axios from 'axios';

    export default {
        name: "ProductCard",
        data() {
             let info = null;
                 const elements = [
                     { "name": "shoe1"}
                 ];

            return {
                elements, info
            }

        },
        mounted () {
            axios
                .get('https://api.coindesk.com/v1/bpi/currentprice.json')
                .then(response => (this.info = response))
        }
    }
</script>

<style scoped>

    .card {
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
        border-radius: 5px; /* 5px rounded corners */
        width: 150px;
    }

    /* Add rounded corners to the top left and the top right corner of the image */
    img {
        border-radius: 5px 5px 0 0;
        width: 150px;
    }
</style>