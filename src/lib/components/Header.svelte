<script lang="ts">
    import { page } from '$app/stores';
    import { derived } from 'svelte/store';

    const currentPath = derived(page, $page => $page.url.pathname);
</script>

<style>
    :root {
        --primary: #14b8a6;
        --accent: #6366f1;
        --gray-light: #f8fafc;
        --text-main: #1e293b;
    }

    .headerAlign {
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 1200px;
        margin: 1em auto 1em auto;
    }

    header{
        font-family: 'Segoe UI', sans-serif;
        background-color: var(--gray-light);
        color: var(--text-main);
        line-height: 1.6;
    }

    .brand {
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }

    .nav {
        list-style: none;
        display: flex;
        gap: 2rem;
        margin: 0;
        padding: 0;
    }

    .brand h2 {
        margin: 0;
        color: var(--primary);
        font-weight: 700;
    }

    .lockLogo {
        width: 2em;
    }

    .nav li a {
        text-decoration: none;
        color: inherit;
        display: block;
    }

    .nav li:hover,
    .nav li.active {
        color: var(--accent);
    }

    .brand h2 {
        margin: 0;
        color: var(--primary);
        font-weight: 700;
    }
</style>

<header>
    <div class="headerAlign">
        <div class="brand">
            <img src="lock.png" alt="lock" class="lockLogo"/>
            <h2>GonePass</h2>
        </div>
        <ul class="nav">
            <li class:active={$currentPath === '/'}><a href="/">Home</a></li>
            <li class:active={$currentPath === '/login'}><a href="/login">Login</a></li>
            <li class:active={$currentPath === '/register'}><a href="/register">Register</a></li>
        </ul>
    </div>
</header>
