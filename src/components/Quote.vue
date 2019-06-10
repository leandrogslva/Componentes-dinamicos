<template>
    <div>
        <div class="title">
        <slot name="title"></slot>
        <span style="color: #ccc"><slot name="subtitle">Subtitle</slot></span>
        </div>
        <hr>
        <div>
            <slot></slot>
        </div>
    <!-- <p>{{quote}}</p>-->
   </div>
</template>

<script>
export default {
 //   props: ['quote']
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

    h2{
        color: red;
    }
    .title{
        font-style: italic;
    }
    p{
        font-size: 25px;
        color: red;
    }
</style>
