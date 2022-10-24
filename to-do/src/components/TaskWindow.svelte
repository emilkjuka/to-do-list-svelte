<script lang="ts">
    import TaskItem from "./TaskItem.svelte";

    let index = 1;
    let items = [index];

    function createNewTask() {
        items = [index, ...items];
    }
</script>

<div class="h-[95%] w-[428px] min-w-[420px] rounded-[30px] border-dashed border-4 border-black flex flex-col justify-start items-center m-6 pt-6">
    <div class="mt-2 w-[95%]  flex justify-between ">
        <div class="bg-gray-200 mr-2 pl-2 pr-2 rounded-lg">To-Do</div>
        <div class="bg-gray-200  ml-2  pl-2 pr-2 rounded-lg">
            <button on:click={createNewTask}>New Task</button>
        </div>
    </div>
    {#each items as item}
        <TaskItem />
    {/each}
</div>
