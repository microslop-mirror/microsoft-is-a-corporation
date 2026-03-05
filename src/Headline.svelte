<script>
    const { title, links } = $props();
</script>

<div class="headline">
    <div class="title">{title}</div>
    {#each links as link}
        <a target="_blank" href="{link}">{link}</a>
    {/each}
</div>

<style>
    .headline {
        display: block;
        border: 2px solid gray;
        margin: 20px;
        padding: 10px;
        padding-bottom: 0px;
        font-family: sans-serif;
    }

    .headline a {
        display: block;
        margin-bottom: 10px;
    }

    .title {
        color: black;
        font-size: xx-large;
        font-weight: bold;
        margin-bottom: 10px;
    }
</style>