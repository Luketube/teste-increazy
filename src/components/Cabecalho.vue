<template>
    <nav>
        <div class="logo">
            <img src="../assets/logo.svg" alt="Logo da empresa">
        </div>
        <div class="info">
            <div class="cidade">
                    <p class="cidade_principal">Surreal São Paulo</p>
                    <p class="cidade_secundario">VTEX</p>
            </div>
            <div>
                <button><img src="../assets/icone-bell.svg" alt="Icone de sino"></button>
            </div>
        </div>
        <div class="usuario">
            <p class="usuario_nome">Olá, Lucas</p>
            <img src="../assets/usuario.svg" alt="Foto do usuário">
        </div>
    </nav>
</template>

<script>
export default {
    name: 'CabecalhoNotificacao',

}
</script>

<style scoped>
nav{
    display: flex;
    background-color: #9206E9;
    align-items: center;
    height: 5rem;
}

img{
    margin: 0.5rem 1rem;
}

p{
    color: #FFFFFF;
}

.logo{
    width: auto;
}

.info{
    align-items: center;
    display: flex;
    justify-content: space-between;
    width: 100%;
}

.cidade{
    border: 1px solid #FFFFFF;
    border-radius: 8px;
    padding: 0.5rem 6rem 0.5rem 0.5rem;
    font-weight: 700;
}

.cidade_secundario{
    margin-top: 0.5rem;
    font-size: 0.75rem;
    font-weight: 100;
}

button{
    border: none;
    background-color: #9206E9;
}
button:hover{
    cursor: pointer;
}

.usuario{
    align-items: center;
    border-left: 1px solid #FFFFFF;
    display: flex;
    margin-right: 1rem;
    width: auto;
}

.usuario_nome{
    padding: 0 1rem 0 1.5rem;
    white-space: nowrap
}

@media only screen and (max-width: 768px) {
    .logo{
        display: none;
    }
    .cidade{
        border: none;
    }
    .info{
        margin-left: 1rem;
    }
    .usuario_nome{
        display: none;
    }
}
@media only screen and (max-width: 375px){
    .usuario{
        display: none;
    }
}
</style>
