<script lang="ts">
    export let text:string;
    export let gHeight:number=0;
</script>

<!-- <div class="graph" height={gHeight}>
    hello I am graph {text}
</div> -->

<div class="graph" style="height:{gHeight}px">
    <p>{text}</p>
</div>

<style lang="scss">
    .graph {
        background-color: cornflowerblue;
        width: 50px;
        height : var(gHeight);
    }
    .graph p{
        width:inherit;
        display: static;
        position: absolute;
        top:500px;
        text-align: center;
        margin-top: 5px;
    }
</style>