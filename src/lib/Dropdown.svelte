<script>
    import { fade } from "svelte/transition";
    export let className = ''
    let isShow = false
    const dropDown = () => {
        isShow = !isShow
        console.log(isShow)
    }
</script>

<section>
    <div class="dropdown">
        <button class="btn {className}" on:click={dropDown}>
            <slot></slot>
            <div class="arrow">
                {#if isShow}
                    <i class="fa-solid fa-chevron-up"></i>
                {:else}
                    <i class="fa-solid fa-chevron-down"></i>
                {/if}
            </div>
        </button>
        {#if isShow}
            <div transition:fade class="dropdown-content">
                <li>
                    <a href="/">Option 1</a>
                </li>
                <li>
                    <a href="/">Option 2</a>
                </li>
                <li>
                    <a href="/">Option 3</a>
                </li>
            </div>
        {/if}
    </div>
</section>

<style>
    .dropdown {
        position: relative;
    }

    .dropdown-content {
        position: absolute;
        background-color: #FFF;
        border: 1px solid #249DE9;
        margin-top: 3px;
        border-radius: 5px;
        width: 50%;
        right: 0;
    }

    .dropdown-content li {
        list-style: none;
        padding: 10px;
    }

    .dropdown-content li a {
        padding: 10px;
        text-decoration: none;
        color: #000000;
        opacity: calc(80%);
        transition: 0.3s;
        background-color: #FFF;
    }

    .dropdown-content a:hover {
        background-color: #F2F6FF;
        border-radius: 5px;
    }

    .btn {
        background-color: #FFF;
        text-transform: capitalize;
        padding: 12px 30px;
        border-radius: 5px;
        font-size: 16px;
        display: flex;
        cursor: pointer;
    }

    .btn-outline-primary {
        border: 1px solid #000000;
    }

    .btn-outline-primary:focus {
        border-color: #249DE9;
    }

    .arrow {
        opacity: calc(50%);
        margin-left: 30px;
    }
</style>