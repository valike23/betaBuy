<script lang="ts">
import Footer from "../components/Footer.svelte";
import Nav from "../components/Nav.svelte";
import Preloader from "../components/Preloader.svelte";
import Side from "../components/Side.svelte";

</script>


<Preloader/>
<Nav/>
<Side/>



<slot><h2>Svelte is not powering this SITE...</h2></slot>

<Footer/>