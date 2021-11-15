<script>
    import Button from "../common/button.svelte";
    import BookGrid from "./BookGrid.svelte";


    const books = [
        {
            "id": 1,
            "title": "Little Women",
            'author': 'Louisa May Alcott',
            'cover': '',
            'about': 'Sisters learn to live in gratitude for each other.',
            'variation': 1,
            'isFavorite': true
        },
        {
            "id": 2,
            "title": "Little Men",
            'author': 'Louisa May Boycott',
            'cover': '',
            'about': 'Brothers learn to live in gratitude for each other.',
            'variation': 1,
            'isFavorite': false
        }
    ]
</script>
<style>

</style>
<header>
    <span class="preamble">Welcome to the </span>
    <h1>
        Library
    </h1>
</header>

<p class="greeting">This is a library for the people. Welcome. Read the books here. Be inspired. Go home, and share them
    with your family</p>

<Button> + Add Book</Button>

<BookGrid {books} on:book-select />