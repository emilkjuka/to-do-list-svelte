<script lang="ts">
    import TopBarIcon from "./TopBarIcon.svelte";
    let name = "Emil"
    let now = new Date().toLocaleDateString()


</script>


<div class="w-[100%] h-[6%] flex justify-between items-center bg-white min-h-[50px]">
    <div class=" font-bold ml-4 p-2 text-[1.5rem]">Welcome back, {name}! 👋</div>
    <div class="flex justify-evenly p-2 ml-2 mr-2 text-[1.5rem] w-[500px] items-center">
        <TopBarIcon imgSource={"../../assets/folder.png"} extraAtr={""}></TopBarIcon>
        <TopBarIcon imgSource={"../../assets/folder.png"} extraAtr={""}></TopBarIcon>
        <TopBarIcon imgSource={"../../assets/folder.png"} extraAtr={""}></TopBarIcon>
        <div class="ml-2 mr-2 text-gray-400">{now}</div>
        <TopBarIcon imgSource={"../../assets/pp.png"} extraAtr={"rounded-xl"}></TopBarIcon>
    </div>
</div>