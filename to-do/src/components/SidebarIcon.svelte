<script lang="ts">
    export let imageSource;
    export let addProps;

    function onClickHandler(){
        console.log("sidebar icon clicked!")
    }
</script>

<div class="flex justify-center align-middle rounded-md h-[50px] w-[50px]  hover:bg-gray-200 {addProps}" on:click={onClickHandler} on:keypress>
    <img alt="img" class=" m-2 h-[32px] w-[32px] hover:invert" src={imageSource}/>
</div>
