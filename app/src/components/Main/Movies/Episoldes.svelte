<script>

    const movieDisplay = [
        {movieAlbum: "/largeAlbum/img1.webp", movieName: "Love in Easy World"},
        {movieAlbum: "/largeAlbum/img2.webp", movieName: "Hacks gold"},
        {movieAlbum: "/largeAlbum/img3.webp", movieName: "Palm rover"},
        {movieAlbum: "/largeAlbum/img4.webp", movieName: "Deem watch"},
    ]
</script>

<div class="@container mt-10">
    <div class="grid grid-cols-2 gap-2 @3xl:grid-cols-4">
        {#each movieDisplay as {movieAlbum, movieName}}
            <div class="bg-cover bg-center h-50 rounded-xl flex items-end justify-center font-bold" style="background-image: url({movieAlbum});">
                <p class="text-white text-center">{movieName}</p>
            </div>
        {/each}
    </div>
</div>


<style>
    
</style>