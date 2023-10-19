<script>
    import Header from "./lib/Header.svelte";
    import Carousel from "./lib/Carousel.svelte";
    import Hero from "./lib/Hero.svelte";
    import Catalog from "./lib/Catalog.svelte";
    import Icon from "./lib/Icon.svelte";
    import SearchBar from "./lib/SearchBar.svelte"
    
</script>

<main>
    <Header />
    <Icon />
    <SearchBar />
    <Carousel />
    <Hero />
    <Catalog url="https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc"/>
    <Catalog url="https://api.themoviedb.org/3/movie/upcoming?language=en-US&page=1"/>
    <Catalog url="https://api.themoviedb.org/3/movie/top_rated?language=en-US&page=1"/>
    <Catalog url="https://api.themoviedb.org/3/trending/movie/day?language=en-US"/>
    
</main>
