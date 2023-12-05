<script>

</script>

<div id="intro">
    <div class="box image_box">
        <img src="/images/scene3.webp" alt="">
    </div>

    <div class="box first_box">
        <div class="item">
            <span>Santral Kumpanya'nın</span>
            <span>Aynı Aşkın Laciverdi</span>
        </div>

        <div class="item">
            <ul>
                <li>KOMEDİ</li>
                <li>2 PERDE</li>
                <li>6 SKEÇ</li>
                <li>90 DK.</li>
            </ul>
        </div>
    </div>

    <div class="box image_box">
        <img src="/images/scene3.webp" alt="">
    </div>

    <div class="box second_box">
        <span>"Tüm merasimler, ortaya çıkmaya fırsat kollayan bir gülünçlük barındırırlar."</span>
        <span>Henri Bergson</span>
    </div>
</div>

<style>
    #intro
    {
        display: grid;
        border-top: .3rem solid #fff;
        border-bottom: .3rem solid #fff;
    }

/***** ****/

    #intro > .box
    {
        height: 40rem;
    }

/***** ****/

    #intro > .image_box > img
    {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

/***** ****/

    #intro > .first_box,
    #intro > .second_box
    {
        display: flex;
        padding: 0 1rem;
        text-align: center;
        align-items: center;
        flex-direction: column;
    }

/***** ****/

    #intro > .first_box
    {
        color: #fff;
        background-color: #000;
        justify-content: space-evenly;
    }

/***** ****/

    #intro > .first_box > .item > span:nth-child( 1 )
    {
        font-size: 1.5rem;
    }

    #intro > .first_box > .item > span:nth-child( 2 )
    {
        line-height: .9;
        margin-top: 1rem;
        font-size: 3.5rem;
    }

/***** ****/

    #intro > .first_box > .item > ul > li
    {
        font-size: 1.3rem;
    }

/***** ****/

    #intro > .second_box
    {
        justify-content: center;
        background-color: #f7fade;
    }

    #intro > .second_box > span:nth-child( 1 )
    {
        font-size: 2rem;
        line-height: 1.2;
    }

    #intro > .second_box > span:nth-child( 2 )
    {
        margin-top: 2rem;
        font-size: 1.5rem;
        border-bottom: .2rem solid #e21c21;
    }

/*****
      Media
           ****/

    @media ( min-width: 48em )
    {
        #intro
        {
            grid-template-columns: repeat( 2, 1fr );
        }

    /***** ****/

        #intro > .first_box > .item > span:nth-child( 2 )
        {
            font-size: 4.5rem;
        }
    }

    @media ( min-width: 62em )
    {
        #intro
        {
            grid-template-columns: repeat( 4, 1fr );
        }
    }
</style>