<template>
    <div>
        <div>
            <form id="burger-form">

                <div class="input-container">
                    <label for="name">Nome do Cliente: </label>
                    <input type="text" id="name" name="name" v-model="name" placeholder="Digite o seu nome" required>
                </div>

                <div class="input-container">
                    <label for="pao">Escolha o pão: </label>
                    <select name="pao" id="pao" v-model="pao" required>
                        <option value="">Selecione o seu pão</option>
                        <option value="integral">Integral</option>
                    </select>
                </div>

                <div class="input-container">
                    <label for="carne">Escolha a carne: </label>
                    <select name="carne" id="carne" v-model="carne" required>
                        <option value="">Selecione a carne</option>
                        <option value="bovina">Bovina</option>
                    </select>
                </div>

                <div id="opcionais-container" class="input-container">
                    <label id="opcionais-title" for="opcionais">Escolha os opcionais: </label>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="salame">
                        <span>Salame</span>
                    </div>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="salame">
                        <span>Salame</span>
                    </div>
                </div>

                <div class="input-container">
                    <input class="submit-btn" type="submit" name="submit-btn" value="Criar meu Burger!" id="">
                </div>

            </form>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'BurgerForm',
        data() {
            return {
                name: ''
            }
        }
    }
</script>

<style scoped>

div{
    font-family: Arial, Helvetica, sans-serif;
}

#burger-form{
    max-width: 450px;
    margin: 40px auto;
    padding: 30px;
    background: #ffffff;
    border-radius: 12px;
    box-shadow: 0 8px 25px rgba(0,0,0,0.12);
    transition: 0.3s;
}

#burger-form:hover{
    box-shadow: 0 10px 30px rgba(0,0,0,0.18);
}

.input-container{
    display: flex;
    flex-direction: column;
    margin-bottom: 20px;
}

label{
    margin-bottom: 6px;
    font-weight: bold;
    color: #444;
    font-size: 14px;
}

input, select{
    padding: 12px;
    width: 100%;
    border: 1px solid #ddd;
    border-radius: 8px;
    font-size: 14px;
    background-color: #fafafa;
    transition: all 0.25s ease;
}

input:focus, select:focus{
    outline: none;
    border-color: #fcba26;
    background-color: #fff;
    box-shadow: 0 0 6px rgba(252,186,38,0.4);
}

#opcionais-container{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;
}

#opcionais-title{
    grid-column: span 2;
    margin-bottom: 5px;
}

.checkbox-container{
    display: flex;
    align-items: center;
    background: #f5f5f5;
    padding: 10px;
    border-radius: 6px;
    transition: 0.2s;
    cursor: pointer;
}

.checkbox-container:hover{
    background: #ffe8a6;
}

.checkbox-container input{
    margin-right: 8px;
}

.checkbox-container span{
    font-weight: 500;
}

.submit-btn{
    width: 100%;
    background: linear-gradient(135deg,#fcba26,#f39c12);
    color: #222;
    font-weight: bold;
    border: none;
    padding: 14px;
    border-radius: 8px;
    cursor: pointer;
    font-size: 16px;
    transition: all 0.25s ease;
}

.submit-btn:hover{
    transform: translateY(-2px);
    box-shadow: 0 6px 14px rgba(0,0,0,0.2);
}

@media (max-width: 500px){
    #burger-form{
        padding: 20px;
        margin: 20px;
    }

    .checkbox-container{
        width: 100%;
    }
}

</style>