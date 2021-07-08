<script lang="ts">
  import { onMount } from "svelte";

  let win: any = {};
  let route: any;
  onMount(() => {
    win = window;
    route = win.location.pathname;
    route = route.split("/");
    route = route[1];
    console.log(route);
  });
  const nav = (active: string) =>{
    route = active;
  }
</script>

<div class="footer-nav-area" id="footerNav">
  <div class="container h-100 px-0">
    <div class="suha-footer-nav h-100">
      <ul class="h-100 d-flex align-items-center justify-content-between ps-0">
        <li on:click="{()=>{nav('')}}" class:active={route == ""}>
          <a href="/"><i class="lni lni-home" />Home</a>
        </li>
        <li on:click="{()=>{nav('category')}}" class:active={route == "category"}>
          <a href="/category"><i class="lni lni-gallery" />Category</a>
        </li>
        <li on:click="{()=>{nav('cart')}}" class:active={route == "cart"}>
          <a href="/cart"><i class="lni lni-shopping-basket" />Cart</a>
        </li>
        <li on:click="{()=>{nav('blog')}}" class:active={route == "blog"}>
          <a href="/blog"><i class="lni lni-rss-feed" />Feeds</a>
        </li>
       
        <li on:click="{()=>{nav('accounts')}}" class:active={route == "accounts"}>
          <a href="/accounts"><i class="lni lni-user" />accounts</a>
        </li>
      </ul>
    </div>
  </div>
</div>
