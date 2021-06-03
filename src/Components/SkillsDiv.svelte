<script>
    import * as Skills from '../Json/Skills.json';
</script>

<div class = "row">
    <div class = "inside">

        {#each [1, 2, 3, 4, 5, 6] as num}
            {#each Skills.default as skill}
                <a href = {skill.link} target = "_blank"><img class = "app" src = "/Logos/{skill.name}.svg" alt={skill.name}/></a>
            {/each}
        {/each}
    </div>
</div>

<style>
    .row{
        border-top: solid white 3px;
        border-bottom: solid white 3px;
        overflow-x: hidden;
        width: 100vw;
        height: 20vh;
        background-color: #261111;
    }

    .inside{
        display: flex;
        height: 100%;
        position: relative;
        align-items: center;
        -webkit-animation-name: move;
        -webkit-animation-duration: 20s;
        -webkit-animation-iteration-count: infinite;
        -webkit-animation-direction: right;
        -webkit-animation-timing-function: linear;
    }
    @-webkit-keyframes move {
        0% {
            margin-left: 0px;
        }
        100% {
            margin-left: calc(270*-9px);
        }
}
    .inside:hover {
        -webkit-animation-play-state: paused;
    }

    .app{
        margin-left: 60px;
        margin-right: 60px;
        display: inline;
        width: 150px;
        transition: 0.2s;
    }

    .app:hover{
        transform: scale(1.1);
    }

</style>