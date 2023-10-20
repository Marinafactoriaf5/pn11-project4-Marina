<script>
    import Header from "./lib/Header.svelte";
    import Hero from "./lib/Hero.svelte";
    import Title from "./lib/Title.svelte"
    import Catalog from "./lib/Catalog.svelte";
</script>

<main>
    <Header />
    <Hero />
    <Title text="Novetats a la cartellera" />
    <Catalog
        url="https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc"
    />
    <Title text="Pròximament" />
    <Catalog
        url="https://api.themoviedb.org/3/movie/upcoming?language=en-US&page=1"
    />
    <Title text="Top 20" />
    <Catalog
        url="https://api.themoviedb.org/3/movie/top_rated?language=en-US&page=1"
    />
    <Title text="Populars" />
    <Catalog
        url="https://api.themoviedb.org/3/trending/movie/day?language=en-US"
    />
</main>
