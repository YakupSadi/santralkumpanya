<div class="box">
    <div class="item">
        <span>Hazırlık</span>
        <span>Aşağıdaki sorulara göz atın. Kamera karşısına geçmeye hazır olun!</span>
    </div>

    <div class="item">
        <span>Action!</span>
        <span>Çift olarak herhangi bir kameranın karşısına geçin ve sorulara cevaplarınızı verin! Cep telefonu bile olur, sorun değil! ;)</span>
    </div>

    <div class="item">
        <span>YouTube'a yükleyin!</span>
        <span>Çektiğiniz videoyu YouTube'a "Liste Dışı / Unlisted" olarak yükleyin.</span>
    </div>

    <div class="item">
        <span>Formu Doldurun!</span>
        <span>Aşağıdaki formu doldurarak başvurunuzu tamamlayın. Videonuzun linkini kopyalayıp ilgili kısma yapıştırmayı unutmayın!</span>
    </div>
</div>

<style>
    .box
    {
        gap: 1rem;
        display: grid;
        margin-top: 2rem;
        grid-template-columns: 1fr;
    }

/***** ****/

    .box > .item
    {
        height: 20rem;
        display: flex;
        padding: 0 1rem;
        text-align: center;
        flex-direction: column;
        justify-content: center;
    }

    .box > .item > span:nth-child( 1 )
    {
        font-size: 1.7rem;
        margin-bottom: 1rem;
        background-color: #fff;
    }

    .box > .item > span:nth-child( 2 )
    {
        font-size: 1.2rem;
    }

    .box > .item:nth-child( 1 )
    {
        background-color: #f2bf5e;
    }

    .box > .item:nth-child( 2 )
    {
        background-color: #ff6161;
    }

    .box > .item:nth-child( 3 )
    {
        background-color: #536eb7;
    }

    .box > .item:nth-child( 4 )
    {
        background-color: #75cba8;
    }


/*****
      Media
           ****/

    @media ( min-width: 36em )
    {
        .box
        {
            grid-template-columns: repeat( 2, 1fr );
        }
    }

    @media ( min-width: 62em )
    {
        .box
        {
            grid-template-columns: repeat( 4, 1fr );
        }
    }
</style>