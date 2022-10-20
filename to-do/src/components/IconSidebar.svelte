<script lang="ts">
    export let imageSource;
    export let addProps;
</script>

<div class="flex justify-center align-middle mb-2 rounded-md {addProps}">
    <img alt="img mis" src={imageSource}/>
</div>

<style>

</style>