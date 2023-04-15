<script>
  import Box from "./../lib/Box.svelte";
  export let data;
  let allArticles = data.articlesPost;
</script>

<div class="cnt">
  <h1 class="large">Welcome to SvelteKit</h1>
  <p>
    Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
  </p>
</div>
<div class="cnt mt-5">
  {#each allArticles as item (item.id)}
    <Box>
      <h1>{item.title}</h1>
      <p>{item.desc}</p>
    </Box>
  {/each}
</div>

<style>
  .cnt {
    display: flex;
    flex-direction: column;
    text-align: center;
    justify-content: center;
    align-items: center;
  }
  .mt-5 {
    margin-top: 30px;
  }
  h1,
  p {
    margin: 5px;
  }
  .large {
    font-size: 3rem;
  }
</style>
