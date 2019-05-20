<script>
    import { createEventDispatcher } from 'svelte';

    export let title;
    export let price;
    export let bestseller = false;  // a default value means the prop is optional

    const dispatch = createEventDispatcher();

    function addToCart() {
        dispatch('add-to-cart', {id: 's1'}); // can pass context graph ids !!!
    }
</script>

<article>
    <h1>{title}</h1>
    <h2>${price}</h2>
    {#if bestseller}
        <h3>BESTSELLER</h3>
    {/if}
    <button on:click="{addToCart}">Add to Cart</button>
    <button on:click="{() => {dispatch('delete', 's1')}}">Delete</button>
</article>