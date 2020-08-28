<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
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
        </nav>
    <b-card
    title="Card Title"
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
    <b-card-text>
      Some quick example text to build on the card title and make up the bulk of the card's content.
    </b-card-text>

    <b-button href="#" variant="primary">Go somewhere</b-button>
  </b-card>
    
    </div>
    
</template>