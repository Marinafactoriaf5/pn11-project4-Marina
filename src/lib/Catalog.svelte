<script>
    export let url;

    const options = {
        method: "GET",
        headers: {
            accept: "application/json",
            Authorization:
                "Bearer eyJhbGciOiJIUzI1NiJ9.eyJhdWQiOiJlOWU0ZGUyZTllMTg0N2NhMGM2OTEzODUwNjhhZTM0MSIsInN1YiI6IjY1MmU1OTViZWE4NGM3MDBhZWY0NDEwYSIsInNjb3BlcyI6WyJhcGlfcmVhZCJdLCJ2ZXJzaW9uIjoxfQ.-SP3uSRZ-FN8xfCFzDN9DUo0ner_m8z7TjZd74gVSkk",
        },
    };

    let movies = [];

    fetch(url, options)
        .then((response) => response.json())
        .then((data) => (movies = data.results))
        .catch((err) => console.error(err));

    const rotateLeft = (e) => {
        const transitioningImage = movies[movies.length - 1];
        movies = [
            movies[movies.length - 1],
            ...movies.slice(0, movies.length - 1),
        ];
    };

    const rotateRight = (e) => {
        const transitioningImage = movies[0];
        movies = [...movies.slice(1, movies.length), movies[0]];
    };
</script>

<div>
    {#each movies as movie}
        <img
            src={`https://image.tmdb.org/t/p/w500${movie.poster_path}`}
            alt={movie.title}
        />
    {/each}
    <button id="left" on:click={rotateLeft}> ◀
        <slot name="leftControl">
        </slot>
    </button>
    <button id="right" on:click={rotateRight}> ▶
        <slot name="rightControl">
        </slot>
    </button>
</div>

<style>
    img {
        height: 300px;
        object-fit: cover;
        border-radius: 3px;
    }

    div {
        display: flex;
        justify-content: center;
        gap: 15px;
        margin-top: 30px;
        margin-bottom: 50px;
        flex-direction: row;
        max-width: 100%;
        overflow-x:visible;
        overflow-y: hidden;
    }

    #left{
        left:35px;
        position: absolute;
        display:flex ;
        height: 300px;
        width:40px;
        background-color: grey;
        opacity: 40%;
        padding-top: 140px;
        color: white;
        font-size: 20px;
    }

    #right{
        right: 35px;
        position: absolute;
        display:flex ;
        height: 300px;
        width:40px;
        background-color: grey;
        opacity: 40%;
        padding-top: 140px;
        color: white;
        font-size: 20px;
    }

</style>
