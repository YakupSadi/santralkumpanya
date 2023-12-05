<script>

</script>

<div id="outro">
    <div class="box">
        <div class="title">
            <span>Ekip</span>
        </div>

        <div class="text">
            <ul>
                <li>OYUNCULAR</li>
                <li>YÖNETEN</li>
                <li>DANIŞMAN</li>
                <li>DRAMATURG</li>
                <li>METİN</li>
            </ul>
        </div>

        <div class="image">
            <img src="/images/scene4.webp" alt="">
        </div>
    </div>

    <div class="box">
        <div class="title">
            <span>Hakkında</span>
        </div>

        <div class="text">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas eget dolor tellus. Vestibulum aliquam ligula tellus.
            Vestibulum aliquet metus ac nisl mollis, a suscipit mi blandit. Vivamus in euismod tellus, id porta nulla. Praesent
            elit erat, sollicitudin ac lorem nec, egestas suscipit arcu. Morbi eget ullamcorper dolor. Class aptent taciti sociosqu
            ad litora torquent per conubia nostra, per inceptos himenaeos. Maecenas a blandit massa. Integer semper, leo ut lobortis
            ultrices, dui risus sodales diam, quis euismod nisl massa sit amet ex. Etiam eleifend porttitor est. Sed ullamcorper
            finibus congue.
        </div>

        <div class="image">
            <img src="/images/scene4.webp" alt="">
        </div>
    </div>

    <div class="box">
        <div class="title">
            <span>Kısa Özet</span>
        </div>

        <div class="text">
            <span>
                Cras malesuada mi quis bibendum scelerisque. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque
                rutrum, felis vitae varius consequat, orci dolor tristique lacus, nec commodo mi nisl vel odio. Sed varius, erat id
                efficitur tincidunt, arcu orci hendrerit est, sit amet pharetra urna felis ut risus.
            </span>
        </div>

        <div class="image">
            <img src="/images/scene4.webp" alt="">
        </div>
    </div>
</div>

<style>
    #outro
    {
        gap: 1rem;
        display: grid;
        margin-top: 5rem;
        justify-content: center;
    }

/***** ****/

    #outro > .box
    {
        display: grid;
        border: .3rem solid #fff;
    }

    #outro > .box:nth-child( 1 )
    {
        background-color: #00cf83;
    }

    #outro > .box:nth-child( 2 )
    {
        background-color: #e21c21;
    }

    #outro > .box:nth-child( 3 )
    {
        background-color: #3d9be9;
    }

/***** ****/

    #outro > .box > .title
    {
        text-align: center;
    }

    #outro > .box:first-child > .title > span
    {
        width: 10rem;
        font-size: 2rem;
        margin: 2rem 0 0 -1rem;
    }

    #outro > .box:not( :first-child ) > .title > span
    {
        width: 10rem;
        font-size: 2rem;
        margin: 1rem 0 0 1rem;
    }

/***** ****/

    #outro > .box > .text
    {
        color: #fff;
        padding: 2rem;
    }

/***** ****/

    #outro > .box > .image
    {
        min-height: 21.4rem;
        border-top: .3rem solid #fff;
    }

    #outro > .box > .image > img
    {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

/*****
      Media
           ****/

    @media ( min-width: 48em )
    {
        #outro > .box
        {
            max-width: 61rem;
            grid-template-columns: 5rem 1fr 1fr;
        }

    /***** ****/

        #outro > .box > .title > span
        {
            margin: 5rem 0 0 -2.5rem;
            transform: rotate( -90deg );
        }

        #outro > .box:first-child > .title > span
        {
            margin: 2rem 0 0 -2.5rem;
        }

        #outro > .box:not( :first-child ) > .title > span
        {
            margin: 5rem 0 0 -2.5rem;
        }

    /***** ****/

        #outro > .box > .text
        {
            padding: 2rem 2rem 2rem 0;
        }

    /***** ****/

        #outro > .box > .image
        {
            border: 0;
            border-left: .3rem solid #fff;
        }
    }
</style>