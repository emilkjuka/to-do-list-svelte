<script lang="ts">
    let contentProjects = ">"
    let opValueProjects = 0
    let heightValueProjects = "0"
    
    let contentTasks = ">"
    let opValueTasks = 0
    let heightValueTasks = "0"

    function onClickHideTasks(){
        contentTasks == ">" ? contentTasks="˅" : contentTasks=">"
        opValueTasks == 0 ? opValueTasks=100 : opValueTasks = 0
        heightValueTasks == "0" ? heightValueTasks = "auto" : heightValueTasks="0"
    }
    
    function onClickHideProject(){
        contentProjects == ">" ? contentProjects="˅" : contentProjects=">"
        opValueProjects == 0 ? opValueProjects=100 : opValueProjects = 0
        heightValueProjects == "0" ? heightValueProjects = "auto" : heightValueProjects="0"
    }

</script>

<div class="w-full h-full">
    <div class="flex justify-between text-[1.5rem] font-bold">
        <div>Projects</div>
        <button on:click={onClickHideProject}>{contentProjects}</button>
    </div>
    <div><vr></div>
    <div class="ml-2 pl-4 pt-2 pb-2 font-bold border-l-2 border-gray-200 opacity-{opValueProjects} h-{heightValueProjects}">
        <div class="mt-4">All Projects(3)</div>
        <div class="mt-4">Main Project</div>
        <div class="mt-4">Second Project</div>
        <div class="mt-4">Third Project</div>
    </div>
    <div class="flex justify-between text-[1.5rem] font-bold">
        <div>Tasks</div>
        <button on:click={onClickHideTasks}>{contentTasks}</button>
    </div>
    <div><vr></div>
    <div class="ml-2 pl-4 pt-2 font-bold border-l-2 border-gray-200 opacity-{opValueTasks} h-{heightValueTasks}">
        <div class="mt-4">All Projects(3)</div>
        <div class="mt-4">Main Project</div>
        <div class="mt-4">Second Project</div>
        <div class="mt-4">Third Project</div>
    </div>
    

</div>