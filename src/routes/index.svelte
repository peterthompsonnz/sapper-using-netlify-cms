<script>
  import { onMount } from "svelte";

  onMount(() => {
    if (window.netlifyIdentity) {
      window.netlifyIdentity.on("init", user => {
        if (!user) {
          window.netlifyIdentity.on("login", () => {
            document.location.href = "/admin/";
          });
        }
      });
    }
  });
</script>

<style>
  h1,
  figure,
  p {
    text-align: center;
    margin: 1em auto;
  }

  h1 {
    font-size: 2.25rem;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  figure {
    margin: 0 0 1rem 0;
  }

  img {
    max-width: 100%;
    margin: 0 0 1rem 0;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.26);
    border-radius: 5px;
  }

  p {
    margin: 1rem auto 2rem 0;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 3rem;
    }
  }
</style>

<svelte:head>
  <title>Sapper project template</title>
  <script src="https://identity.netlify.com/v1/netlify-identity-widget.js">

  </script>
</svelte:head>

<h1>Peter T's Blog</h1>

<figure>
  <img
    alt="Road through the tussock on the Beebys range"
    src="images/road-to-nowhere.jpg" />
  <figcaption>
    Road to nowhere - Beebys Knob,
    <a
      href="https://www.doc.govt.nz/parks-and-recreation/places-to-go/nelson-tasman/places/nelson-lakes-national-park/?tab-id=50578">
      Nelson Lakes National Park
    </a>
    , New Zealand.
  </figcaption>
</figure>

<p>
  At this stage most of the content on this site will be in the blogging
  section.
</p>
<hr />
