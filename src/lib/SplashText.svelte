<script lang="ts">
    export let text: string = '';
</script>

<div>
    <p>{text}</p>
</div>

<style>
    p {
        color: #fafc19;
        text-shadow: 1px 1px #424400, 2px 2px #424400, 3px 3px #424400;
        
        font-family: 'minecraft';

        position: absolute;
        bottom: -30px;
        right: -45px;

        animation: pop 0.58s infinite;
        -webkit-animation: pop 0.58s infinite;
    }

    div {
        -ms-transform: rotate(-25deg);
        -webkit-transform: rotate(-25deg);
        transform: rotate(-25deg);
    }

    @font-face {
        font-family: 'minecraft';
        font-style: normal;
        font-weight: 500;
        src: url('/fonts/minecraft.ttf'); /* IE9 Compat Modes */
    }

    @keyframes pop {
        from {
            transform:scale(0.95)
        }
        50% {
            transform:scale(1)
        }
        to {
            transform:scale(0.95)
        }
    }
    @-webkit-keyframes pop {
        from {
            -webkit-transform:scale(0.95)
        }
        50% {
            -webkit-transform:scale(1)
        }
        to {
            -webkit-transform:scale(0.95)
        }
    }
</style>