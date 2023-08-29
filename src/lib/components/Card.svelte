<script lang="ts">
    import Tag from './Tag.svelte';
  
    export let imageUrl: string;
    export let altText = "";
    export let title: string;
    export let description: string;
    export let tags: Array<string> = [];
    export let href = "#";
  </script>
  
  <a class="block card rounded-xl" href={href}>
      <div class="rounded-xl">
          <div class="flex flex-row rounded-xl overflow-hidden space-x-4 h-64">
              <div class="relative w-48">
                  <img class="w-full h-full object-cover" src={imageUrl} alt={altText}>
              </div>
              <div class="flex flex-col justify-between w-2/3 px-4 py-6">
                  <div class="flex flex-col items-start">
                      <div class="text-4xl font-bold">{title}</div>
                      <div class="text-base">{description}</div>
                  </div>
                  <div class="flex flex-row gap-2">
                      {#each tags as tag (tag)}
                          <Tag label={tag} />
                      {/each}
                  </div>
              </div>
          </div>
      </div>
  </a>
  