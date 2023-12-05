<svelte:head>
    <title>Hakkımızda</title>
</svelte:head>

<script>

</script>

<div id="about">
    <div class="container">
        <div class="box">
            <img src="/images/img.webp" alt="Team_Image">
        </div>

        <div class="box">
            <h1>Hakkımızda</h1>
            <span>Sahne üstü üretimlerimize ek olarak kamera önü üretimlerimizle 2013'ten beri yolumuza devam etmekteyiz.</span>
        </div>
    </div>
</div>

<style>
    #about
    {
        min-height: 75vh;
    }

    #about > .container
    {
        display: grid;
    }

/***** ****/

    #about > .container > .box
    {
        border: .3rem solid #fff;
    }

    #about > .container > .box:nth-child( 2 )
    {
        color: #fff;
        display: flex;
        padding: 2rem 1rem;
        text-align: center;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        background-color: #e21c21;
    }

    #about > .container > .box:nth-child( 2 ) > h1
    {
        margin-bottom: 1rem;
        background-color: #000;
    }

    #about > .container > .box:nth-child( 2 ) > span
    {
        font-size: 1.2rem;
    }

    #about > .container > .box > img
    {
        width: 100%;
        height: 100%;
    }

/*****
      Media
           ****/

    @media ( min-width: 62em )
    {
        #about > .container
        {
            grid-template-columns: repeat( 2, 1fr );
        }
    }
</style>