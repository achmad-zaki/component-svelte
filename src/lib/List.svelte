<script>
    export let type = ''
    export let data = []
        // {
        //     nama: "achmad zaki",
        //     kelas: "sp.5.1"
        // },
        // {
        //     nama: "achmad roni",
        //     kelas: "sp.5.1"
        // }
</script>

{#if type === 'bullet' || type === ''}    
<ul class="list-item">
    {#each data as items}
        <li class="bullet">{items}</li>
    {/each}
</ul>
{:else if type === 'number'}
<ol class="list-item">
    {#each data as items}
        <li class="number">{items}</li>
    {/each}
</ol>
{/if}