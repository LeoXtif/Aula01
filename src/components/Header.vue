<template>
    <div class="header">
        <h1>
            LeoFood
        </h1>
        <div class="div-input">
            <span class="grupo-label-input">Produto</span>
            <input v-model="produto" class="grupo-input" type="text"/>
        </div>
        <div class="div-input">
            <span class="grupo-label-input">Cliente</span>
            <input v-model="cliente" class="grupo-input" type="text"/>
        </div>
        <div class="div-input">
            <span class="grupo-label-input">Quantidade</span>
            <input v-model="quantidade" class="grupo-input" type="text"/>
        </div>
        <div class="div-input"> 
            <button class="grupo-botao" type="submit" @click="clicou">
                Comprar
             </button> 
            
        </div>

    </div>
</template>

<style>
    .header{
        display: flex;
        flex-direction: column; 
        background-color: gray;
        width: 100%;
        flex: 1;
        margin: 0;
        padding: 0 0 0 10px;

    }

    .div-input {
        display: flex;
        flex-direction: column;
        background-color: blue;
        width: 270px;
        height: 80px;
        padding: 10px;
    }

    .grupo-label-input {
        font-size: 25px;
        color:black;
    }

    .grupo-input {
        flex:1;
    }

    .grupo-botao {
        font-size: 30px;
        
    }
</style>

<script>
    export default {

        data: function () {
            return {
                produto:"",
                cliente:"",
                quantidade:""
            }
        },
        methods: {
            clicou:()=>{
               let texto=this.data.produto
                alert(texto)
            }

        },
        
    }
</script>