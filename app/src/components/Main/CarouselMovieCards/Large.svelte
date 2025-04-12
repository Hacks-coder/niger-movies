<script>
    import Carousel from 'svelte-carousel';
    import { browser } from '$app/environment';

    let carousel;
  
    const handleNextClick = () => {
        carousel.goToNext()
    }

    const movieDisplay = [
        {movieAlbum: "/largeAlbum/img1.webp", movieName: "Love in Easy World"},
        {movieAlbum: "/largeAlbum/img2.webp", movieName: "Hacks gold"},
        {movieAlbum: "/largeAlbum/img3.webp", movieName: "Palm rover"},
        {movieAlbum: "/largeAlbum/img4.webp", movieName: "Deem watch"},
    ]
</script>


<div class="mt-10">
    {#if browser}
  <Carousel
    bind:this={carousel}
    autoplay
    arrows={false}
  >
    {#each movieDisplay as {movieAlbum, movieName}}
        <div style="background-image: url({movieAlbum})" class="bg-center bg-cover bg-no-repeat h-[400px] w-full">
            <p>{movieName}</p>
        </div>
    {/each}
  </Carousel>
{/if}
</div>