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
        <li>
          <a href="message.html"><i class="lni lni-life-ring" />Support</a>
        </li>
        <li>
          <a href="cart.html"><i class="lni lni-shopping-basket" />Cart</a>
        </li>
        <li><a href="pages.html"><i class="lni lni-heart" />Pages</a></li>
        <li on:click="{()=>{nav('settings')}}" class:active={route == "settings"}>
          <a href="/settings"><i class="lni lni-cog" />Settings</a>
        </li>
      </ul>
    </div>
  </div>
</div>
