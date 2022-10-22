<script lang="ts">
import MainBody from "./components/MainBody.svelte";
import ProjectsPane from "./components/ProjectsPane.svelte";
import Sidebar from "./components/Sidebar.svelte";
import TopBar from "./components/TopBar.svelte";
</script>

<main>
  <div class="absolute h-full w-full flex bg-pink-300">
    <Sidebar></Sidebar>
    <ProjectsPane></ProjectsPane>
    <div class="h-full w-[83%] flex flex-col bg-green-300">
      <TopBar></TopBar>
      <MainBody></MainBody>
    </div>
  </div>
</main>

<style></style>
