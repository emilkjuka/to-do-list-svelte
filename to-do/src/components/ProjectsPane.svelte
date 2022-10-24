<script lang="ts">
    import ProjectContainer from "./ProjectContainer.svelte";


    
</script>

<div class="h-full w-[13%] min-w-[170px] bg-white flex flex-col justify-start">
    <div class="flex justify-between items-center p-4">
        <div class="text-[2em] font-bold">Projects</div>
        <button class=" bg-gray-200 rounded-[90px] hover:bg-yellow-400"><img class="w-[32px] h-[32px]" src="../../assets/plus.png" alt="plus" /></button>
    </div>
    <div class="flex flex-col justify-center items-start p-4">
        <ProjectContainer></ProjectContainer>
    </div>
</div>

<style>
    
</style>