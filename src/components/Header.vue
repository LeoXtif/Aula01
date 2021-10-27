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
            <button class="grupo-botao" type="submit"  @click="clicou">
                Agendar
             </button> 
        </div>
        <div class="div-input">
            <label class="grupo-label-input">Produtos Agendados</label>
            <div class="lista-produtos">
                <div class="lista-linha">
                    <label>Bolo de Chocolate | Myllena</label>
                     <button>
                       Pronto
                     </button> 
                </div>
            </div>
        </div>

    </div>
</template>

<script>
    export default {

        data () {
            return {
                produto:"",
                cliente:"",
                quantidade:"",
                produtosAgendados:[
                    "Pão \n",
                    "bolo"
                ]
            }
        },
        methods: { 

            clicou : function (){
               let texto=this.quantidade
                alert(texto)
            }

        },
        
    }
</script>

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

    .lista-produtos {
        display: flex;
        background-color: green;

         
    }
</style>