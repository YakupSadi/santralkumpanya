<svelte:head>
    <title>Yalnızım Mesut Bey</title>
</svelte:head>

<script>
    import Steps from '../../components/Steps.svelte'
</script>

<div id="test">
    <div class="steps">
        <div class="text">
            <span>YALNIZIM MESUT BEY'E KONUK OLARAK</span>
            <span>KATILMAK MI İSTİYORSUNUZ?</span>
        </div>

        <Steps />
    </div>

    <div class="questions">
        <div class="text">
            <span>SORULAR</span>
        </div>

        <div class="box">
            <div class="item">
                <span>#1</span>
                <span>Ne zamandır yalnızsın?</span>
            </div>
            <div class="item">
                <span>#11</span>
                <span>Eski sevgilinin sevgilisi senden daha başarılı diyebilir miyiz? Daha yakışıklı/güzel/seksi diyebilir miyiz? Dürüst ol!</span>
            </div>
        </div>
    </div>

    <div class="form">
        <div class="text">
            <span>BAŞVURU FORMU</span>
        </div>

        <div class="box">
            <form>
                <input type="text" placeholder="Adınız ve Soyadınız">
                <input type="text" placeholder="Yaşadığınız Şehir">
                <input type="text" placeholder="Mesleğiniz">
                <input type="text" placeholder="Email Adresi">
                <input type="text" placeholder="Telefon Numarası">
                <input type="text" placeholder="Başvuru Videonuzun Youtube Linki">

                <input type="submit" value="Send">
            </form>
        </div>
    </div>
</div>

<style>
    #test
    {
        gap: 5rem;
        display: flex;
        margin: 1rem 0;
        flex-direction: column;
    }

/***** ****/

    #test > .steps > .text
    {
        text-align: center;
    }

    #test > .steps > .text > span
    {
        color: #fff;
    }
    
    #test > .steps > .text > span:nth-child( 1 )
    {
        display: inline;
        font-size: 2rem;
        background-color: #e21c21;
    }

    #test > .steps > .text > span:nth-child( 2 )
    {
        font-size: 1.7rem;
        font-weight: bold;
    }

/***** ****/

    #test > .questions > .text > span
    {
        color: #fff;
        font-size: 2rem;
        text-align: center;
    }

/***** ****/

    #test > .questions > .box
    {
        padding: 0 1rem;
        margin-top: 2rem;
    }

/***** ****/

    #test > .questions > .box > .item
    {
        gap: 1rem;
        display: grid;
        margin: 1rem auto;
        grid-template-columns: 1fr;
    }

/***** ****/

    #test > .questions > .box > .item > span:nth-child( 1 )
    {
        color: #fff;
        display: flex;
        height: 4.2rem;
        margin-top: 2rem;
        padding: 1.5rem 0;
        font-size: 1.5rem;
        align-items: center;
        justify-content: center;
        background-color: #e21c21;
    }

    #test > .questions > .box > .item > span:nth-child( 2 )
    {
        color: #fff;
        display: flex;
        padding: 1rem;
        font-size: 1.2rem;
        align-items: center;
        border: .2rem solid #fff;
    }

    #test > .form > .text > span
    {
        color: #fff;
        font-size: 2rem;
        text-align: center;
    }

/***** ****/

    #test > .form > .box
    {
        width: 100%;
        padding: 0 1rem;
        margin: 2rem auto;
    }

    #test > .form > .box > form
    {
        gap: 1rem;
        display: flex;
        flex-direction: column;
    }

    #test > .form > .box > form > input
    {
        color: #fff;
        outline: none;
        padding: 1rem;
        font-size: 1.2rem;
        border: .2rem solid #fff;
    }

    #test > .form > .box > form > input[ type="submit" ]
    {
        margin: 0 auto;
        cursor: pointer;
        font-weight: bold;
        width: fit-content;
        padding: 1rem 5rem;
        background-color: #e21c21;
    }

/*****
      Media
           ****/

    @media ( min-width: 36em )
    {
        #test > .steps > .text > span
        {
            margin: 0 1rem;
        }

    /***** ****/

        #test > .form > .box
        {
            max-width: 50rem;
        }

        #test > .questions > .box > .item
        {
            max-width: 50rem;
            grid-template-columns: 5rem 1fr;
        }

        #test > .questions > .box > .item > span:nth-child( 1 )
        {
            margin-top: 0;
        }

    /***** ****/

        #test > .form > .box > form > input[ type="submit" ]
        {
            padding: 1rem 10rem;
        }
    }
</style>