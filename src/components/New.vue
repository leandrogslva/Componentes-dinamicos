<template>
    <div>
        <h3>New quote</h3>
        <button @click="counter++">Increase</button>
        <p>{{counter}}</p>
        <hr>
        <div>
            <!-- esse slot, no caso, é o componente "component" que está registrado na minha instância pai -->
            <slot></slot>
        </div>
   </div>
</template>

<script>
export default {
    data: function() {
       return{
        counter: 0
       }; 
    },
    created() {
        console.log("Foi criado");
    },
    destroyed() {
        console.log('Destroyed');
    },
    deactivated() {
        console.log('Deactivated');
    },
    activated() {
        console.log('Activated');
    }
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
        color: green;
    }
    .title{
        font-style: italic;
    }
    p{
        font-size: 25px;
    }
</style>
