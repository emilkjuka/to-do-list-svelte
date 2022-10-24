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

    function deleteTaskWindow(){
        console.log(windows)
    }
</script>

<div class="h-full w-full overflow-hidden">
    <div class="h-[5%] min-h-[30px] flex justify-between items-center">
        <button class="rounded-xl bg-white w-[96px] m-4" on:click={createNewTaskWindow}>
            + Add view
        </button>
        <button class="rounded-xl bg-white w-[96px] m-4" on:click={deleteTaskWindow}>
            - Delete view
        </button>
    </div>
    <div class="h-[95%] max-w-inherit flex items-center justify-start bg-slate-300 pl-8 overflow-x-auto overflow-y-hidden">
        {#each windows as window}
        <TaskWindow></TaskWindow>
        {/each}
    </div>
</div>
