<script>
    function toggle() {
        window.document.body.classList.toggle('dark-mode')
    }
    </script>
        <button on:click={toggle}>
        <slot/>
        </button>

    <style>
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