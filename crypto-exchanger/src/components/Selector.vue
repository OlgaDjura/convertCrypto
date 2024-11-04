<script>
export default {
    props: {
        setCrypto: {
            type: Function,
            required: true
        }
    },
    data() {
        return {
        current: ''
        }
    },
    methods: {
        selectItem(val) {
            this.setCrypto(val);
            this.current = val;
        }
    },

}
</script>
<template>
<ul>
    <li @click="selectItem('BTC')" :className="current == 'BTC' ? 'active' : ''">Bitcoin</li>
    <li @click="selectItem('ETH')" :className="current == 'ETH' ? 'active' : ''">ETH</li>
    <li @click="selectItem('USDT')" :className="current == 'USDT' ? 'active' : ''">USDT</li>
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