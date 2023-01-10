<script>
    export let headers = []
    export let data = []
</script>

<table class="table-components">
    <thead>
        <tr>
            {#each headers as head}
                <th>{head}</th>
            {/each}
        </tr>
    </thead>
    <tbody>
        {#each data as items, no}  
        <tr>
            <td>{no + 1}</td>
            {#each items as mhs}                
                <td>{mhs}</td>
            {/each}
        </tr>
        {/each}
    </tbody>
</table>