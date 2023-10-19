<script>
</script>

<header>
    <img src="src/assets/logo.png" alt="logo filmin" class="logoFilmin" />

    <ul>
        <li>
            <a href="enlace1.html"><strong>Inici</strong></a>
        </li>
        <li>
            <a href="enlace2.html"><strong>Pel·lícules</strong></a>
        </li>
        <li>
            <a href="enlace2.html"><strong>Sèries</strong></a>
        </li>
        <li>
            <a href="enlace3.html"><strong>Col·leccions</strong></a>
        </li>
        <li>
            <a href="enlace2.html"><strong>Festivals</strong></a>
        </li>
        <li>
            <a href="enlace2.html"><strong>Kids</strong></a>
        </li>
        <li>
            <a href="enlace2.html"><strong>Més</strong></a>
        </li>
    </ul>
    <div class="topButtons">
        <button class="greenButton"><strong>SUBSCRIU-T'HI</strong> </button>
        <button class="transparentButton"
            ><strong>INICIAR SESSIÓ</strong>
        </button>
    </div>
    <article>
        <img src="src/assets/glass.png" alt="magnifying glass" class="glass" />
    </article>
</header>

<style>
    .logoFilmin {
        height: 37px;
        width: 136;
        display: flex;
        margin-top: 10px;
        margin-left: 40px;
    }

    header {
        background-image: url("src/assets/rectangle.png");
        width: 1440px;
        height: 60px;
        display: flex;
        margin-top: -30px;
        margin-left: -80px;
    }

    ul {
        display: flex;
        flex-direction: row;
        list-style: none;
        padding: 0;
    }

    li {
        font-family: Helvetica, Arial, sans-serif;
        color: white;
        margin-left: 40px;
    }

    .greenButton {
        background-color: #02ffa1;
        width: 120px;
        height: 32px;
        border-radius: 5px;
        border: none;
        margin-top: 15px;
        margin-left: 200px;
    }
    .transparentButton {
        background-color: transparent;
        width: 120px;
        height: 32px;
        border-radius: 5px;
        border: 3;
        border-color: white;
        margin-top: 15px;
        margin-left: 20px;
        margin-right: 20px;
        color: white;
    }

    .topButtons {
        display: flex;
    }

    .glass {
        height: 44px;
        width: 50px;
        margin-top: 8px;
    }
</style>
