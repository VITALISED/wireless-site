<script>
	import { page } from '$app/stores';
    import pfp from '$lib/images/pfp.png'
</script>

<header>
    <div class="corner">
        <img src={pfp} alt='pfp'>
    </div>

    <nav>
        <ul>
            <li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
            <li aria-current={$page.url.pathname === '/blog' ? 'page' : undefined}>
				<a href="/blog">Thinking Crap</a>
			</li>
            <li aria-current={$page.url.pathname === '/projects' ? 'page' : undefined}>
				<a href="/projects">Stuff</a>
			</li>
        </ul>
    </nav>

    <div class="corner">
        <!-- do later -->
    </div>
</header>

<style>
    header {
        display: flex;
        justify-content: space-between;
        background: rgb(13, 17, 23);
    }

    .corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
        padding-top: 2px;
        padding-left: 20px;
		width: 3em;
		height: 3em;
		object-fit: contain;
	}

    nav {
		display: flex;
		justify-content: center;
		--background: red;
	}

    path {
		fill: purple;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
</style>