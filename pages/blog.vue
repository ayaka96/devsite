<template>
<div>
<!--nav class="navbar navbar-expand-lg navbar-dark bg-dark">
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav mr-auto">
                <li class="nav-item">
                    <NuxtLink class="text-white px-3" to="/">home</NuxtLink>
                </li>
                <li class="nav-item">
                    <NuxtLink class="text-white px-3" to="/blog">blog</NuxtLink>
                </li>
                </ul>
            </div>
        </nav-->
<header>    
<div class="container">
<div class="row">
    <div class="col span-12">
    <div class="head">
        <h1><a href="index.html">Ayaka Omura</a></h1>
		<div class="snsbox">
			<img src="../assets/img/in-icon.png" alt="Instagram">
		    <img src="../assets/img/fb-icon.png" alt="Facebook"></div>
        </div>
    </div></div>
    
<div class="row">
    <div class="col span-12">
        <nav>
        <div id="open"><img src="../assets/img/button.png"></div>
        <div id="close"><img src="../assets/img/button2.png"></div>    
            <div id="navi">
        <ul>
            <li><a href="/">ホーム</a></li>
            <li><NuxtLink to="/blog">Blog</NuxtLink></li>
            <!--li><a href="subpage.html">サブページ</a></li>
            <li><a href="subpage.html">サブページ</a></li>
            <li><a href="subpage.html">お問い合わせ</a></li-->
            </ul>
                </div>
        </nav>
    </div>
        </div>
    </div>
    </header>



<!-- Navbarここまで -->
<div v-for="post of posts" :key="post.slug" class="mx-auto" style="width: 400px; margin: 20px;">
      
<b-card
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 40rem;"
    class="mb-2"
    title=""
  >
  <h3>{{ post.title }}</h3>
    <b-card-text>
    {{ post.description }}
    </b-card-text>
    <NuxtLink :to="post.slug">
    <b-button variant="primary">{{ post.title }}</b-button>
    </NuxtLink>
  </b-card>
  </div>





</div>
</template>


<script>

export default {
  components: {
  },
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },
  async asyncData({ $content }) {
    const posts = await $content("blog").fetch();

    return {
      posts,
    };
  },
}
</script>