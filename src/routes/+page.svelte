<script>
    let projects = ["app","todolist","icad"];
</script>

<h1>Hello world!</h1>
<h3>
    This project contains multiple differnt practice apps, each on their own
    folder
</h3>
<button on:click={
    document.getElementsByTagName("iframe").requestFullscreen()
}>fullscreen</button>
{#each projects as p}
    <li>
        <a href="/{p}">{p}</a>
    </li>
{/each}
