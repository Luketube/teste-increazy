<template>

<aside>
    <div class="aside_top">
        <button><img class="icons icons_top" src="../assets/icone-busca.svg" alt="Icone de bússola"></button>
        <button><img class="icons icons_top" src="../assets/icone-folder2.svg" alt="Icone de pasta"></button>    
    </div>
    <button><img class="icons aside_bottom" src="../assets/icone-ajuste.svg" alt="">
</button>
</aside>


</template>

<script>

export default {
    name: 'BarraLateral',
}

</script>

<style scoped>
aside{
    align-items: center;
    background-color: #F6F6F6;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    max-width: 5.5rem;
    height: calc(100vh - 5rem);
    padding: 0rem 1rem;
}

.aside_top{
    
    display: flex;
    justify-content: space-around;
    flex-direction: column;
}


button{
    border: none;
    background-color: #F6F6F6;
}
button:hover{
    cursor: pointer;
}

.icons_top{
    margin: 2rem 0;
}

.icons{
    max-width: 32px;
}

.aside_bottom{
    background-color: #20272C;
    padding: 1rem;
    border-radius: 8px;
    margin-bottom: 1rem;
}

</style>