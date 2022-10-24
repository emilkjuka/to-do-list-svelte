<script lang="ts">
    import TaskItem from "./TaskItem.svelte";

    let index = 1;
    let items = [index];

    function createNewTask() {
        items = [index, ...items];
    }
</script>

<div
    class="h-[95%] w-[428px] min-w-[420px] rounded-[30px] border-dashed border-2 border-gray-400 flex flex-col justify-start items-center m-6 pt-6"
>
    <div class="mt-2 w-[95%]  mb-4 flex justify-between ">
        <input
            class="pl-2 pr-2 h-[30px] rounded-md  bg-gray-200"
            placeholder="New View"
        />
        <button
            class="bg-gray-200  ml-2  pl-2 pr-2 rounded-lg hover:bg-yellow-400"
            on:click={createNewTask}>New Task</button
        >
    </div>
    <div
        class="w-full h-[90%] rounded-b-[45px] flex flex-col items-center overflow-y-auto scrollbar-hide"
    >
        {#each items as item}
            <TaskItem />
        {/each}
    </div>
    <div class="mb-2 mt-2 w-full flex justify-end pr-4 pb-2">
        <button
            class="bg-white w-16 h-6 rounded-xl text-centerS hover:bg-red-400">X</button>
    </div>
</div>
