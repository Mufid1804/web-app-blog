<script>
    import Card from '$lib/components/Card.svelte';
    let times = 10;
</script>
<div class="fixed top-0 left-0 w-full h-screen bg-gradient-to-b from-primary-400 z-[-1]"></div>
  
<div class="flex flex-col justify-center items-center gap-4">
    <div class="mt-4 text-5xl font-bold text-center">
        Maryam Azizah's Notes
    </div>
    <div class="flex flex-col p-4 overflow-y-auto items-center h-full">
        <div class="flex flex-col gap-4 mb-4 w-[768px]">
            {#each Array(times) as _, i}
            <Card 
                imageUrl="https://cataas.com/cat/says/hello%20world!" 
                altText="Cat Hello World!" 
                title="Judul Konten" 
                description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Omnis nisi tempora dolorum nostrum est dicta eos tempore ducimus quasi eius, error magni totam odit amet. Lorem ipsum dolor sit amet consectetur adipisicing elit. Rerum ad vitae qui, magni voluptates quia." 
                tags={['Cat', 'Animal']}
                href="/elements/cards"
            />
            {/each}
        </div>
    </div>
</div>
