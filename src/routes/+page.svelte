<script>
    let projects = ["app","todolist"];
</script>

<h1>Hello world!</h1>
<h3>
    This project contains multiple differnt practice apps, each on their own
    folder
</h3>
{#each projects as p}
    <li>
        <a href="/{p}t">{p}</a>
    </li>
{/each}
