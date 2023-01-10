<script>
    let current = '3';
</script>

<section>
    <ul class="pagination">
        <li class="page-item">
            <button class="page-link"><i class="fa-solid fa-chevron-left"></i></button>
        </li>
        <li class="page-item">
            <button class="page-link {current === '1' ? 'active' : ''}" on:click="{() => current = '1'}">1</button>
        </li>
        <li class="page-item">
            <button class="page-link {current === '2' ? 'active' : ''}" on:click="{() => current = '2'}">2</button>
        </li>
        <li class="page-item">
            <button class="page-link {current === '3' ? 'active' : ''}" on:click="{() => current = '3'}">3</button>
        </li>
        <li class="page-item">
            <button class="page-link"><i class="fa-solid fa-chevron-right"></i></button>
        </li>
    </ul>
</section>

<style>
    .pagination {
        display: flex;
        align-items: center;
    }

    .page-item {
        list-style: none;
        margin: 0 5px;
    }

    .page-link {
        padding: 10px 17px;
        text-decoration: none;
        transition: 0.3s;
        color: #000000;
        border: none;
        font-size: 16px;
        background-color: transparent;
    }

    .page-link.active {
        background-color: #249DE9;
        color: #FFF;
        border-radius: 100%;
    }

    .page-link:hover {
        background-color: #249DE9;
        color: #FFF;
        border-radius: 100%;
    }
</style>