<script>
    import {createEventDispatcher} from 'svelte'
    export let books = [];

    const dispatch = createEventDispatcher();

</script>
<ul>
    {#each books as book}
        <li on:click={() => dispatch('book-select', {id: book.id})}>{book.title}</li>
        <li>{book.author}</li>
        <li>{book.about}</li>
        {#if (book.isFavorite)}
            <div>&lt;3</div>
        {/if}
    {/each}
</ul>