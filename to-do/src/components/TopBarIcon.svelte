<script lang="ts">

    export let imgSource;
    export let extraAtr;

    function onClickHandler(){
        console.log("clicked!")
    }
</script>

<div class="hover:bg-slate-200 rounded-xl p-1 w-[40px] h-[40px]" on:click={onClickHandler} on:keypress>
    <img class="h-[32px] w-[32px] {extraAtr}" alt="img" src={imgSource}/>
</div>
