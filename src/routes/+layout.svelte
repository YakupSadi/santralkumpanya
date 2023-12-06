<script>
    import '../global.css'

    import Header from '../components/Header.svelte'
    import Footer from '../components/Footer.svelte'


    let isHeaderClicked = false

    function handleHeaderClick( newIsHeaderClicked )
    {
        isHeaderClicked = newIsHeaderClicked.detail

        document.body.style.overflow = isHeaderClicked ? 'hidden' : 'auto'
    }
</script>

<Header on:headerClicked={ handleHeaderClick } />

<slot />

<Footer />

<!-- 
    https://www.santralkumpanya.com/hakkimizda
    https://marketsplash.com/tutorials/svelte/svelte-head/
 -->