<script lang="ts">
    import Footer from "../components/Footer.svelte";
    import Nav from "../components/Nav.svelte";
    import Preloader from "../components/Preloader.svelte";
    import Side from "../components/Side.svelte";
    import { stores } from "@sapper/app";
    import ProductNav from "../components/ProductNav.svelte";
    import SideFilter from "../components/SideFilter.svelte";
    import { onMount } from "svelte";
    let win: any = {};
    onMount(() => {
        win = window;
    });
    const { page } = stores();
    let data;
    let isMainPage = true;
    page.subscribe((value) => {
        data = value;
    });
    $: if (true) {
        let address: any = data.path;
        address = address.split("/");
        address = address[1];
        console.log("2", address);
        if (!isMainPage)
            if (address == "" || address == "category") {
                isMainPage = true;
                if (win.location) win.location.reload();
            }
        if (isMainPage)
            if (address == "cart") {
                isMainPage = false;
                if (win.location) win.location.reload();
            }
    }
    console.log(data);
</script>

<Preloader />
{#if isMainPage}
    <Nav />
    <Side />
{:else}
    <ProductNav />
    <SideFilter />
{/if}

<slot><h2>Svelte is not powering this SITE...</h2></slot>

<Footer />
