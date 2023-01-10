<script>
    import { createEventDispatcher } from "svelte";


    export let text = ''
    export let className = ''
    // export let primary = false;
    // export let secondary = false;

    const dispatch = createEventDispatcher()

    function sayHello() {
        dispatch('hallo 1')
    }
</script>

<section>
    <!-- <button class="btn {className}" class:btn-primary={primary === true} class:btn-secondary={secondary === true}>
        {text}
    </button> -->
    <button class="btn {className}">{text}</button>
</section>