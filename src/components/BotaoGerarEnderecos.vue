<template>
    <div>
        <button>Gerar Endereços</button>
        <hr>
    </div>
    

</template>

<script>
export default{
    name: 'BotaoGerarEnderecos'
}

</script>

<style scoped>
div{
    align-items: flex-end;
    display: flex;
    flex-direction: column;
}

button{
    background-color: #B600EE;
    border: none;
    border-radius: 8px;
    color: #FFFFFF;
    font-size: 16px;
    font-weight: 700;
    margin: 3rem 0;
    padding: 1rem;
    width: 300px;
}

hr{
    width: 100%;
}
</style>