<script>
    import { onMount } from 'svelte';
    let currentPath = '';

    onMount(async() => {
        currentPath = window.location.pathname;
    });

    export let href;
</script>

<nav>
    <ul class="thick-boy">
        <li class:active="{currentPath === '/'}"><a href="/">HOME</a></li>
        <li class:active="{currentPath.includes('/about-the-author')}"><a href="/about-the-author/">ABOUT THE AUTHOR</a></li>
        <li class:active="{currentPath.includes('/preview-the-novel')}"><a href="/preview-the-novel/">PREVIEW</a></li>
        <li class:active="{currentPath.includes('/buy-the-book')}"><a href="/buy-the-book/">BUY A COPY</a></li>-
    </ul>
</nav>

<style lang="scss">
    nav {
      margin-left: auto;
    }

    nav ul {
        list-style: none;
        display: flex;
        flex-direction: row;
        align-items: flex-end;
        justify-content: center;

        li {
          padding: 2px 20px;

          &.active {
            border: 1px solid #9A7036;
          }

          a {
            font-size: 11px;
            color: #FFF;
            opacity: .7;
            text-decoration: none;
          }

        }
    }
</style>