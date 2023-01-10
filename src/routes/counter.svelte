<script>
let count = 0;

function incriment() {
    count += 1;
}
</script>

<div class="counter">
    <p>{count}</p>
    <button on:click={incriment}>+1</button>
</div>

<style>
.counter {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: fit-content;
    color: black;
    transition: color 1s;
}
:global(body.dark-mode) .counter{
            color:white;
            transition: color 1s;
        }
button {
    background-color: #f76027;
    color: white;
    border: none;
    border-radius: 4px;
    padding: 0.5rem;
    text-transform: uppercase;
        }
button:active {
    background-color: #c64d08;
        }
:global(body.dark-mode) button {
    background-color: #0084f6;
    color: white;
        }
:global(body.dark-mode) button:active {
        background-color: #0071d4;
        }
</style>