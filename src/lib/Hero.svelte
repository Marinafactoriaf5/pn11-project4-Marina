<div class="hero">
    <img
        src="src/assets/cover1.jpeg"
        alt="a man in a bed with a woman"
        class="heroImg"
    />
    <h1>Aquí venen les millors produccions de l’any</h1>
    <h3>
        Parla de les nostres pelis a les festes per anar de guay. Realment sino
        mires Filmin, no tens ni idea de cinema.
    </h3>
    <h6>Per ser el més chachi posa aquí el teu correuet. No ho dubtis!</h6>
    <section>
        <input placeholder="El teu super correu" />
        <button><strong>COMENÇAR</strong></button>
    </section>
</div>

<style>
    .heroImg {
        height: auto;
        width: 1440px;
        position: absolute;
        margin-left: 0px;
        margin-top: -50px;
        z-index: -5;
        opacity: 0.3;
        display: flex;
    }

    input {
        border-radius: 8px;
        width: 430px;
        height: 48px;
        stroke: 3px;
        border-color: #6f7082;
        background-color: #060612;
        color: #6f7082;
        font-weight: bold;
        padding-left: 20px;
    }

    button {
        background-color: #02ffa1;
        width: 140px;
        height: 48px;
        border-radius: 5px;
        border: none;
        margin-top: 15px;
        margin-left: 10px;
    }

    h1,
    h6 {
        max-width: 1100px;
        margin: 20px;
    }

    h1 {
        font-size: 64px;
        margin-top: 60px;
    }

    h3 {
        font-size: 24px;
        max-width: 800px;
        margin: 0px;
    }

    h6 {
        font-size: 18px;
    }

    .hero {
        display: flex;
        align-items: center;
        flex-direction: column;
        margin-bottom: 100px;
    }
</style>
