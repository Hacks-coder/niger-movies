<script>
    import Carousel from 'svelte-carousel';
    import { browser } from '$app/environment';

    let carousel;
  
    const handleNextClick = () => {
        carousel.goToNext()
    }

    const movieDisplay = [
        {movieAlbum: "/largeAlbum/img1.jpeg", movieName: "Love in Easy World"},
        {movieAlbum: "/largeAlbum/img2.jpeg", movieName: "Hacks gold"},
        {movieAlbum: "/largeAlbum/img3.jpeg", movieName: "Palm rover"},
        {movieAlbum: "/largeAlbum/img4.jpeg", movieName: "Deem watch"},
    ]
</script>


<div class="mt-10">
    {#if browser}
  <Carousel
    bind:this={carousel}
  >
    {#each movieDisplay as {movieAlbum, movieName}}
        <div style="background-image: url({movieAlbum})" class="bg-center bg-cover h-100">
            <p>{movieName}</p>
        </div>
    {/each}
  </Carousel>
{/if}
</div>