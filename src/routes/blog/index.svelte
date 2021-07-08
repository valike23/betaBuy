<script context="module" lang="ts">
	export function preload() {
		return this.fetch(`blog.json`).then((r: { json: () => any; }) => r.json()).then((posts: { slug: string; title: string, html: any }[]) => {
			return { posts };
		});
	}
</script>

<script lang="ts">
	export let posts: { slug: string; title: string, html: any }[];
</script>

<style>
	ul {
		margin: 0 0 1em 0;
		line-height: 1.5;
	}
</style>

<svelte:head>
	<title>Blog: BetaBuy</title>
</svelte:head>

  <!-- svelte-ignore a11y-invalid-attribute -->
<div class="page-content-wrapper">
	<!-- Top Products-->
	<div class="top-products-area py-3">
	  <div class="container">
		<div class="section-heading d-flex align-items-center justify-content-between">
		  <h6>Blog List</h6>
		  <!-- Layout Options-->
		  
		</div>
		<div class="row g-3">
		  <!-- Single Blog Card-->
		  <div class="col-12 col-md-6">
			<div class="card blog-card list-card">
			  <!-- Post Image-->
			  <div class="post-img"><img src="img/bg-img/12.jpg" alt=""></div>
			  <!-- Post Bookmark--><a class="post-bookmark" href="#"><i class="lni lni-bookmark"></i></a>
			  <!-- Read More Button--><a class="btn btn-danger btn-sm read-more-btn" href="blog-details.html">Read More</a>
			  <!-- Post Content-->
			  <div class="post-content">
				<div class="bg-shapes">
				  <div class="circle1"></div>
				  <div class="circle2"></div>
				  <div class="circle3"></div>
				  <div class="circle4"></div>
				</div>
				<!-- Post Catagory--><a class="post-catagory d-block" href="#">Review</a>
				<!-- Post Title--><a class="post-title d-block" href="blog-details.html">The 5 best reviews in Suha</a>
				<!-- Post Meta-->
				<div class="post-meta d-flex align-items-center justify-content-between flex-wrap"><a href="#"><i class="lni lni-user"></i>Suha</a><span><i class="lni lni-timer"></i>2 min</span></div>
			  </div>
			</div>
		  </div>
		  <!-- Single Blog Card-->
		  <div class="col-12 col-md-6">
			<div class="card blog-card list-card">
			  <!-- Post Image-->
			  <div class="post-img"><img src="img/bg-img/13.jpg" alt=""></div>
			  <!-- Post Bookmark--><a class="post-bookmark" href="#"><i class="lni lni-bookmark"></i></a>
			  <!-- Read More Button--><a class="btn btn-warning btn-sm read-more-btn" href="blog-details.html">Read for $0.9</a>
			  <!-- Post Content-->
			  <div class="post-content">
				<div class="bg-shapes">
				  <div class="circle1"></div>
				  <div class="circle2"></div>
				  <div class="circle3"></div>
				  <div class="circle4"></div>
				</div>
				<!-- Post Catagory--><a class="post-catagory d-block" href="#">Shopping</a>
				<!-- Post Title--><a class="post-title d-block" href="blog-details.html">The best deals of this week</a>
				<!-- Post Meta-->
				<div class="post-meta d-flex align-items-center justify-content-between flex-wrap"><a href="#"><i class="lni lni-user"></i>Suha</a><span><i class="lni lni-timer"></i>4 min</span></div>
			  </div>
			</div>
		  </div>
		  <!-- Single Blog Card-->
		  <div class="col-12 col-md-6">
			<div class="card blog-card list-card">
			  <!-- Post Image-->
			  <div class="post-img"><img src="img/bg-img/14.jpg" alt=""></div>
			  <!-- Post Bookmark--><a class="post-bookmark" href="#"><i class="lni lni-bookmark"></i></a>
			  <!-- Read More Button--><a class="btn btn-danger btn-sm read-more-btn" href="blog-details.html">Read More</a>
			  <!-- Post Content-->
			  <div class="post-content">
				<div class="bg-shapes">
				  <div class="circle1"></div>
				  <div class="circle2"></div>
				  <div class="circle3"></div>
				  <div class="circle4"></div>
				</div>
				<!-- Post Catagory--><a class="post-catagory d-block" href="#">Tips</a>
				<!-- Post Title--><a class="post-title d-block" href="blog-details.html">5 tips for buy original products</a>
				<!-- Post Meta-->
				<div class="post-meta d-flex align-items-center justify-content-between flex-wrap"><a href="#"><i class="lni lni-user"></i>Suha</a><span><i class="lni lni-timer"></i>7 min</span></div>
			  </div>
			</div>
		  </div>
		  <!-- Single Blog Card-->
		  <div class="col-12 col-md-6">
			<div class="card blog-card list-card">
			  <!-- Post Image-->
			  <div class="post-img"><img src="img/bg-img/15.jpg" alt=""></div>
			  <!-- Post Bookmark--><a class="post-bookmark" href="#"><i class="lni lni-bookmark"></i></a>
			  <!-- Read More Button--><a class="btn btn-warning btn-sm read-more-btn" href="blog-details.html">Read for $0.69</a>
			  <!-- Post Content-->
			  <div class="post-content">
				<div class="bg-shapes">
				  <div class="circle1"></div>
				  <div class="circle2"></div>
				  <div class="circle3"></div>
				  <div class="circle4"></div>
				</div>
				<!-- Post Catagory--><a class="post-catagory d-block" href="#">Offer</a>
				<!-- Post Title--><a class="post-title d-block" href="blog-details.html">Mega Deals: Up to 75% discount</a>
				<!-- Post Meta-->
				<div class="post-meta d-flex align-items-center justify-content-between flex-wrap"><a href="#"><i class="lni lni-user"></i>Suha</a><span><i class="lni lni-timer"></i>8 min</span></div>
			  </div>
			</div>
		  </div>
		  <!-- Single Blog Card-->
		  <div class="col-12 col-md-6">
			<div class="card blog-card list-card">
			  <!-- Post Image-->
			  <div class="post-img"><img src="img/bg-img/16.jpg" alt=""></div>
			  <!-- Post Bookmark--><a class="post-bookmark" href="#"><i class="lni lni-bookmark"></i></a>
			  <!-- Read More Button--><a class="btn btn-danger btn-sm read-more-btn" href="blog-details.html">Read More</a>
			  <!-- Post Content-->
			  <div class="post-content">
				<div class="bg-shapes">
				  <div class="circle1"></div>
				  <div class="circle2"></div>
				  <div class="circle3"></div>
				  <div class="circle4"></div>
				</div>
				<!-- Post Catagory--><a class="post-catagory d-block" href="#">Trends</a>
				<!-- Post Title--><a class="post-title d-block" href="blog-details.html">Bridal shopping is the latest trends of this month</a>
				<!-- Post Meta-->
				<div class="post-meta d-flex align-items-center justify-content-between flex-wrap"><a href="#"><i class="lni lni-user"></i>Suha</a><span><i class="lni lni-timer"></i>6 min</span></div>
			  </div>
			</div>
		  </div>
		  <!-- Single Blog Card-->
		  <div class="col-12 col-md-6">
			<div class="card blog-card list-card">
			  <!-- Post Image-->
			  <div class="post-img"><img src="img/bg-img/17.jpg" alt=""></div>
			  <!-- Post Bookmark--><a class="post-bookmark" href="#"><i class="lni lni-bookmark"></i></a>
			  <!-- Read More Button--><a class="btn btn-warning btn-sm read-more-btn" href="blog-details.html">Read for $0.33</a>
			  <!-- Post Content-->
			  <div class="post-content">
				<div class="bg-shapes">
				  <div class="circle1"></div>
				  <div class="circle2"></div>
				  <div class="circle3"></div>
				  <div class="circle4"></div>
				</div>
				<!-- Post Catagory--><a class="post-catagory d-block" href="#">News</a>
				<!-- Post Title--><a class="post-title d-block" href="blog-details.html">How to easily buy a product</a>
				<!-- Post Meta-->
				<div class="post-meta d-flex align-items-center justify-content-between flex-wrap"><a href="#"><i class="lni lni-user"></i>Suha</a><span><i class="lni lni-timer"></i>3 min</span></div>
			  </div>
			</div>
		  </div>
		</div>
	  </div>
	  <div class="container">
		<div class="section-heading pt-3">
		  <h6>Read by category</h6>
		</div>
		<div class="row g-3">
		  <!-- Single Blog Catagory-->
		  <div class="col-6 col-sm-4">
			<div class="card blog-catagory-card">
			
			  <div class="card-body"><a href="#"><i class="lni lni-quotation"></i><span class="d-block">Review</span></a></div>
			</div>
		  </div>
		  <!-- Single Blog Catagory-->
		  <div class="col-6 col-sm-4">
			<div class="card blog-catagory-card">
			  <div class="card-body"><a href="#"><i class="lni lni-shopping-basket"></i><span class="d-block">Shopping</span></a></div>
			</div>
		  </div>
		  <!-- Single Blog Catagory-->
		  <div class="col-6 col-sm-4">
			<div class="card blog-catagory-card">
			  <div class="card-body"><a href="#"><i class="lni lni-bulb"></i><span class="d-block">Tips</span></a></div>
			</div>
		  </div>
		  <!-- Single Blog Catagory-->
		  <div class="col-6 col-sm-4">
			<div class="card blog-catagory-card">
			  <div class="card-body"><a href="#"><i class="lni lni-offer"></i><span class="d-block">Offer</span></a></div>
			</div>
		  </div>
		  <!-- Single Blog Catagory-->
		  <div class="col-6 col-sm-4">
			<div class="card blog-catagory-card">
			  <div class="card-body"><a href="#"><i class="lni lni-bolt-alt"></i><span class="d-block">Trends</span></a></div>
			</div>
		  </div>
		  <!-- Single Blog Catagory-->
		  <div class="col-6 col-sm-4">
			<div class="card blog-catagory-card">
			  <div class="card-body"><a href="#"><i class="lni lni-paperclip"></i><span class="d-block">News</span></a></div>
			</div>
		  </div>
		</div>
	  </div>
	</div>
  </div>
  <!-- Internet Connection Status-->
  <div class="internet-connection-status" id="internetStatus"></div>
<!-- <ul>
	{#each posts as post}
		
		<li><a rel="prefetch" href="blog/{post.slug}">{post.title}</a></li>
	{/each}
</ul> -->
