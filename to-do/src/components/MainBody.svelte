<script lang="ts">
    import TaskWindow from "./TaskWindow.svelte";

    let max = screen.height;
    max = max - 64;
    console.log(max);

    let index = 1
    let windows = [index]

    function createNewTaskWindow(){
        index+=1
        windows = [index, ... windows]
        console.log(windows)
    }

</script>

<div class="h-full w-full overflow-hidden bg-gray-100">
    <div class="h-[5%] min-h-[30px] flex justify-start items-center pt-4">
        <button class="rounded-md bg-white w-[112px] m-4 h-8 min-h-[30px] hover:bg-green-200" on:click={createNewTaskWindow}>
            + Add view
        </button>
    </div>
    <div class="h-[95%] max-w-inherit flex items-center justify-start pl-8 overflow-x-auto overflow-y-hidden">
        {#each windows as window}
        <TaskWindow></TaskWindow>
        {/each}
    </div>
</div>
