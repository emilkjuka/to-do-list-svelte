<script lang="ts">
    import TaskItem from "./TaskItem.svelte";

    let index = 1;
    let items = [index];
</script>

<div
    class="h-[95%] w-[428px] rounded-[30px] border-dashed border-4 border-black flex flex-col justify-start items-center m-6 pt-6"
>
    <div class="m-1 flex justify-center items-between">
        <div class="bg-white ml-2 mr-2 pl-2 pr-2">Title</div>
        <div class="bg-white  ml-2 mr-2 pl-2 pr-2">
            <button>New Task</button>
        </div>
    </div>
    {#each items as item}
        <TaskItem />
    {/each}
</div>
