<template>
    <div>
        <h3>The Author</h3>
        <hr>
        <div>
            <!-- esse slot, no caso, é o componente "component" que está registrado na minha instância pai -->
            <slot></slot>
        </div>
   </div>
</template>

<script>
export default {
}

</script>

<style scoped>
    div{
        border: 1px solid #ccc;
        box-shadow: 1px 1px 2px black;
        padding: 30px;
        margin: 30px auto;
        text-align: center
    }

    h3{
        color: blue;
    }
    .title{
        font-style: italic;
    }
    p{
        font-size: 25px;
    }
</style>
