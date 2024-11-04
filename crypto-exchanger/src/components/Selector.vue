<script>
export default {
    props: {
        setCrypto: {
            type: Function,
            required: true
        },
        cryptoNow: {
            type: String,
            required: true
        }
    },

}
</script>
<template>
<ul>
    <li @click="setCrypto('ETH')" :className="cryptoNow == 'ETH' ? 'active' : ''">ETH</li>
    <li @click="setCrypto('BTC')" :className="cryptoNow == 'BTC' ? 'active' : ''">Bitcoin</li>
    <li @click="setCrypto('USDT')" :className="cryptoNow == 'USDT' ? 'active' : ''">USDT</li>
</ul>
</template>


<style scoped>
ul {
    list-style: none;
    width: 200px;
    padding: 3px;
    border: 3px solid rgb(39, 84, 39);
    border-radius: 15px;
}

li {
    display: block;
    background-color: rgb(24, 56, 26);
    color: aliceblue;
    padding: 20px 0;
}
li:hover, li.active {
    background-color: rgb(2, 54, 37);
    cursor: pointer;
}


</style>