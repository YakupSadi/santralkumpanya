<svelte:head>
    <title>{ $page.status } { $page.error.message }</title>
</svelte:head>

<script>
	import { page } from '$app/stores'
</script>

<div id="error">
    <h1>{ $page.status }</h1>
    <h2>{ $page.error.message }</h2>
</div>

<style>
    #error
    {
        height: 75vh;
        color: #fff;
        display: flex;
        margin-top: 1rem;
        font-weight: bold;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        border-top: .3rem solid #fff;
    }

    #error > h1
    {
        font-size: 7rem;
    }

    #error > h2
    {
        font-size: 1.5rem;
    }

/*****
      Media
           ****/

    @media ( min-width: 36em )
    {
        #error > h1
        {
            font-size: 10rem;
        }

        #error > h2
        {
            font-size: 3rem;
        }
    }
</style>