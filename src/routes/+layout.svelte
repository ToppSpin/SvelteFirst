<script>
    import Navbar from "./navbar.svelte";
import navbar from "./navbar.svelte"
</script>

<div class="TheApp">
    <Navbar />
    
    <main>
        <slot />
    </main>
</div>

<style>

</style>