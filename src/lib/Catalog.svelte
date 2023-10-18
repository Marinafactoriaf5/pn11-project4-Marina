<script>
    const options = {
        method: "GET",
        headers: {
            accept: "application/json",
            Authorization:
                "Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJlOWU0ZGUyZTllMTg0N2NhMGM2OTEzODUwNjhhZTM0MSIsInN1YiI6IjY1MmU1OTViZWE4NGM3MDBhZWY0NDEwYSIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.-SP3uSRZ-FN8xfCFzDN9DUo0ner_m8z7TjZd74gVSkk",
        },
    };

    let movies = [];

    fetch(
        "https://api.themoviedb.org/3/discover/movie?include_adult=false&include_video=false&language=en-US&page=1&sort_by=popularity.desc",
        options
    )
        .then((response) => response.json())
        .then((data) => (movies = data.results))
        .catch((err) => console.error(err));

</script>

<div>
    {#each movies as movie}
        <img
            src={`https://image.tmdb.org/t/p/w500${movie.poster_path}`}
            alt={movie.title}
        />
        <img
            src={`https://image.tmdb.org/t/p/w500${movie.poster_path}`}
            alt={movie.title}
        />
        <img
            src={`https://image.tmdb.org/t/p/w500${movie.poster_path}`}
            alt={movie.title}
        />
    {/each}
</div>

<style>
    img {
        height: 300px;
    }

    div {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 15px;
    }
</style>
