<script>
    export let serviceTitle;
</script>

<article on:click="{() => console.log('Jo')}">
    <h1>{serviceTitle}</h1>
    <button on:click>Add to Cart</button>
    <button>Delete</button>
</article>