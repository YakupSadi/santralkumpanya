<script>
    import '../global.css'

    import { onNavigate } from '$app/navigation'

    import Header from '../components/Header.svelte'
    import Footer from '../components/Footer.svelte'


    onNavigate( ( navigation ) => {

	    if ( !document.startViewTransition ) return

	    return new Promise( ( resolve ) => {

		    document.startViewTransition( async () => {

			    resolve()

			    await navigation.complete
		    })
	    })
    })


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