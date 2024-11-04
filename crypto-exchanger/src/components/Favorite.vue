<script>
export default {
    props: {
        favs: {
            type: Array,
            required: true
        },
        getFromFavs: {
            type: Function,
            required: true
        }
    }

}
</script>
<template>
    <div>
    <h2>Избранное</h2>
    <div className="text" @click="getFromFavs(index)" v-for="(el, index) in favs" :key="index">
        <span>{{ el.from }}</span>
        <span>{{ el.to }}</span>
    </div>
</div>
</template>


<style scoped>
h2 {
    color: aliceblue;
}

div.text {
    display: flex;
    justify-content: center;
    column-gap: 20px;
    margin: 0;
}

span {
    padding: 10px 15px;
    background-color: rgb(75, 134, 114);
    color: aliceblue;
}

div.text:hover {
    opacity: 0.7;
    transform: scale(1.1);
    cursor: pointer;
}


</style>