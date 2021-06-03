<script>

</script>

<div class = "container">
    <div class = "opacity">
        <div class="content">
            <h1>Terence Dumas</h1>
            <a href = "#contact"><button class = "buttonContact">Contact Me</button></a>
        </div>
    </div>
</div>

<style>
    .container{
        background-image: url("/Images/Home.png");
    }

    .buttonContact{
        z-index: 1;
        font-size: 1.3em;
        position: relative;
        width: 400px;
        padding: 0.5em;
        outline: none;
        border: none;
        background-color: white;
        transition: 300ms ease-in-out;
        transform-origin: left;
    }

    .buttonContact::before{
        content: "";
        z-index: -1;
        position: absolute;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        background-color: var(--redTwo);
        transition: transform 300ms ease-in-out;
        transform: scaleX(0);
        transform-origin: left;
    }

    .buttonContact:hover::before, .buttonContact:focus::before {
        transform: scaleX(1);
    }

    .buttonContact:hover{
        color: white;
    }
</style>