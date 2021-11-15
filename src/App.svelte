<script>
    import Library from "./library/library.svelte";
    import Detail from "./Detail.svelte";

    let page = 'library'
    let pageArgs = {}

    function handleBookSelect(event) {
        page = 'detail'
        pageArgs = event.detail
    }
</script>

<main>
    {#if (page === 'detail')}
		<Detail {...pageArgs}/>
    {:else }
        <Library on:book-select={handleBookSelect}/>
    {/if}
</main>

<style>
</style>