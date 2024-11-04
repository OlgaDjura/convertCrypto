<script>
export default {
    props: {
        changeAmount: {
            type: Function,
            required: true
        },
        convert: {
            type: Function,
            required: true
        },
        favorite: {
            type: Function,
            required: true
        }
    }
}
</script>
<template> <div>
<input min="0" type="number" @input="changeAmount($event.target.value)" placeholder="Введите число"> <br>
<button @click="convert()">Конвертировать</button>
<button @click="favorite()" className="favorite">Добавить в избранное</button>
</div>
</template>


<style scoped>
input {
    outline: none;
    border-radius: 10px;
    border: none;
    padding: 10px 15px;
    background-color: rgb(55, 99, 55);
    color: rgb(252, 250, 250);
    font-size: 30px;
}

button {
    margin-top: 20px;
    border-radius: 20px;
    background-color: rgb(91, 133, 91) ;
    height: 50px;
    color: aliceblue;
    cursor: pointer;
}

.favorite {
    margin-left: 20px;
}

</style>