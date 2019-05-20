<script>
    import { createEventDispatcher } from 'svelte';

    export let serviceTitle;

    const dispatch = createEventDispatcher();

    function addToCart() {
        dispatch('add-to-cart', {id: 's1'}); // can pass context graph ids !!!
    }
</script>

<article>
    <h1>{serviceTitle}</h1>
    <button on:click="{addToCart}">Add to Cart</button>
    <button on:click="{() => {dispatch('delete', 's1')}}">Delete</button>
</article>