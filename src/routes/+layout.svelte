<script>import "../app.css";
import './layout.css';
import favicon from '$lib/assets/valentinesLine.svg';

let { children } = $props();</script>

<svelte:head><link rel="icon" href="{favicon}" /></svelte:head>
{@render children()}
