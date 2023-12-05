<script>
    import { fade }    from 'svelte/transition'
    import { onMount } from 'svelte'


    let menuOpen   = false
    let clickedBtn = false
    let scrollStat = true
    let innerWidth = null


    onMount(() => {

        onResize()
    })


    function toggleMenu()
    {
        if( 992 >= innerWidth )
        {
            menuOpen   = !menuOpen
            scrollStat = !scrollStat
            clickedBtn = !clickedBtn
        }
    }


	const wheel = ( node, options ) => {

		let { scrollStat } = options

		const handler = e => {

		    if( !scrollStat ) e.preventDefault()
		}

		node.addEventListener( 'wheel', handler, { passive: false } )

		return {

			update( options )
            {
				scrollStat = options.scrollStat
			},
			destroy()
            {
				node.removeEventListener( 'wheel', handler, { passive: false } )
			}
		}
    }


    function onResize()
    {
        innerWidth = window.innerWidth

        if( 992 >= innerWidth )
        {
            if( clickedBtn )
            {
                menuOpen   = true
                scrollStat = false
            }
            else menuOpen = false
        }
        else
        {
            menuOpen   = true
            scrollStat = true
        }
    }
</script>

<svelte:window use:wheel={{ scrollStat }} on:resize={ onResize } />

<header id="header">
    { #if menuOpen }
        <nav transition:fade>
            <ul>
                <li>
                    <a href="/" on:click={ toggleMenu }>Ana Sayfa</a>
                </li>
                <li>
                    <a href="/test" on:click={ toggleMenu }>Mesut Süre İle İlişki Testi</a>
                </li>
                <li>
                    <a href="/alone" on:click={ toggleMenu }>Yalnızım Mesut Bey</a>
                </li>
                <li>
                    <a href="/about" on:click={ toggleMenu }>Hakkımızda</a>
                </li>
                <li>
                    <a href="/scene" on:click={ toggleMenu }>Sahne Üstü</a>
                </li>
            </ul>
        </nav>
    { /if }

    <button on:click={ toggleMenu }>
        { #if menuOpen }
            <svg xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 384 512">
                <path d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"
                />
            </svg>
        { :else }
            <svg xmlns="http://www.w3.org/2000/svg" height="1em" viewBox="0 0 448 512">
                <path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"
                />
            </svg>
        { /if }
    </button>
</header>

<style>
    #header
    {
        display: flex;
        margin-bottom: 1rem;
        padding: 1rem 1rem 0;
        justify-content: right;
    }

    #header > nav
    {
        left: 0;
        z-index: 1;
        top: 4.5rem;
        width: 100%;
        height: 90vh;
        display: flex;
        padding: 0 1rem;
        position: fixed;
        align-items: center;
        justify-content: center;
        background-color: #221333;
    }

    #header > nav > ul
    {
        gap: 1rem;
        display: flex;
        flex-direction: column;
    }

    #header > nav > ul > li > a
    {
        color: #fff;
        font-size: 1.1rem;
        text-align: center;
        padding: .5rem 1rem;
        border-radius: .3rem;
        transition: .3s all ease;
        border: .2rem solid #e21c21;
    }

    #header > nav > ul > li > a:hover
    {
        background-color: #e21c21;
    }

    #header > button
    {
        display: flex;
        padding: .7rem;
        fill: #e21c21;
        cursor: pointer;
        font-size: 1.5rem;
    }

/*****
      Media
           ****/

    @media ( min-width: 62em )
    {
        #header
        {
            justify-content: center;
            padding: 2rem 2rem 1rem;
        }

        #header > nav
        {
            top: 0;
            left: 0;
            padding: 0;
            width: 100%;
            position: relative;
            height: fit-content;
        }

        #header > nav > ul
        {
            gap: 1rem;
            width: fit-content;
            flex-direction: row;
            justify-content: center;
        }

        #header > button
        {
            display: none;
        }
    }
</style>