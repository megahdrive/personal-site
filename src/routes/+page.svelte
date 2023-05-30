<script lang="ts">
    import HyperlinkSet from "$lib/HyperlinkSet.svelte";
    import Description from "../lib/Description.svelte";
    import SplashText from "../lib/SplashText.svelte";

    import "../lib/javascript/fa.min.js";

    let splashes: string[] = [
        "5 stars!",
        "Masterful!",
        "Translate, pls",
        "No way!",
        "Bona fide!",
        "My website...!",
        "It's free",
        "Fr fr ong",
        "Not legal advice",
        "Not sponsored!",
    ]

    let splash = splashes[Math.floor(Math.random() * splashes.length)];
</script>

<svelte:head>
    <title>Landing</title> 
</svelte:head>

<div style="width:200px;">
    <h1>こんにちは！</h1>
    <SplashText text={splash} />
</div>

<Description text="Hi, welcome to my website. I'm a fullstack programmer from Michigan. I am interested in Japanese culture and spend my spare time reading manga and fanfiction." />

<div class="HyperLink-Sets">
    <HyperlinkSet style="grid-row: 1;grid-column: 1;" header="Awesome websites" links={[
        {"name": "szurubooru", "description": "a polished, danbooru-like imageboard engine", "url": "https://github.com/rr-/szurubooru"},
        {"name": "python-aternos", "description": "an unofficial API for aternos written in python", "url": "https://github.com/DarkCat09/python-aternos"},
        {'name': 'wiby.me', "description": "cool web1 search engine", "url": "http://wiby.me/"},
        {'name': "modrinth", "description": "awesome minecraft mod site", "url": "https://www.modrinth.com"},
        {"name": "japanese sfx db", "description": "a database of sounds in anime/manga", "url": "https://gist.github.com/UserUnknownFactor/093a2296c5a4d9ef7b404728ebde94a3"},
        {"name": "earth.nullschool.net", "description": "an awesome mapping of the earth based on realtime weather data", "url": "https://earth.nullschool.net"},
    ]} />
    
    <HyperlinkSet style="grid-row: 1;grid-column: 2;" header="My tech" links={[
        {"name": "JS/TS", "description": "Bad programming language", "url": "https://nodejs.org/en"},
        {"name": "PHP", "description": "Hypertext preprocessor", "url": "https://php.net"},
        {"name": "Golang (for web backends/compute)", "description": "The Go programming language", "url": "https://go.dev"},
        {"name": "Python", "description": "Funny snake language", "url": "https://www.python.org/"},
        {"name": "C#", "description": "Probably my most experienced language behind Python", "url": "https://learn.microsoft.com/en-us/dotnet/csharp/"},
        {"name": "Java", "description": "WORA language that is actually pretty good", "url": "https://www.java.com"},
    ]} />
</div>

<div class="Social-Menu">
    <h2>
        <a href="https://www.discord.com/users/887425441508519997"><i class="fa-brands fa-discord"></i></a>
        <a href="https://www.reddit.com/u/megahdrive"><i class="fa-brands fa-reddit"></i></a>
    </h2>
</div>

<style>
    .HyperLink-Sets {
        display: grid;
        grid-auto-columns: minmax(0, 1fr);
        position: relative;
        bottom: 12px;
    }

    .Social-Menu {
        text-align: center;
    }
    .Social-Menu a {
        color: white;
        -moz-transition: all .2s ease-in;
        -o-transition: all .2s ease-in;
        -webkit-transition: all .2s ease-in;
        transition: all .2s ease-in;
    }

    .Social-Menu a:hover {
        color: wheat;
    }
</style>