<svelte:head>
    <title>Sahne Üstü</title>
</svelte:head>

<script>

</script>

<div id="scene">
    <div class="box">
        <div class="text">
            <span>Skeç Kafası</span>
            <span>2018</span>
        </div>

        <div class="about">
            <a href="/scene/s">Oyun Hakkında</a>
        </div>

        <img src="/images/sahne.webp" alt="Sahne">
    </div>

    <div class="box">
        <div class="text">
            <span>Skeç Kafası</span>
            <span>2018</span>
        </div>

        <div class="about">
            <a href="/scene/s">Oyun Hakkında</a>
        </div>

        <img src="/images/sahne2.webp" alt="Sahne">
    </div>
</div>

<style>
    #scene
    {
        gap: 1rem;
        display: grid;
        padding: 0 1rem 3rem;
        justify-content: center;
        grid-template-columns: 1fr;
    }

/***** ****/

    #scene > .box
    {
        width: 100%;
        height: 26rem;
        display: flex;
        padding: 1rem;
        position: relative;
        flex-direction: column;
        border: .3rem solid #fff;
        justify-content: space-between;
    }

    #scene > .box > img
    {
        top: 0;
        left: 0;
        width: 100%;
        z-index: -1;
        height: 100%;
        object-fit: cover;
        position: absolute;
    }

/***** ****/

    #scene > .box > .text > span,
    #scene > .box > .about > a
    {
        color: #fff;
    }

    #scene > .box > .text > span:nth-child( 1 )
    {
        font-size: 2rem;
        font-weight: bold;
    }

    #scene > .box > .text > span:nth-child( 2 )
    {
        font-size: 1.5rem;
    }

    #scene > .box > .about > a
    {
        font-size: 1.2rem;
        font-weight: bold;
        width: fit-content;
        padding: .5rem 1rem;
        background-color: #000;
        border: .1rem solid #fff;
        text-decoration: underline;
    }

/*****
      Media
           ****/

    @media ( min-width: 36em )
    {
        #scene > .box
        {
            flex-direction: row;
        }
    }

    @media ( min-width: 62em )
    {
        #scene
        {
            grid-template-columns: 60rem;
        }
    }
</style>