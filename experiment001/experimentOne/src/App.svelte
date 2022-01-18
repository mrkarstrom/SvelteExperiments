<script>
  import data from './data.json';
  import Post from './lib/Posts.svelte';
  import Form from './lib/Form.svelte';

  let author = '';
  let post = '';

  let posts = data.data;

  let isChecked = 1;

  function changeChecked(checkedNum) {
    isChecked = checkedNum;
  }

  function addPost() {
    const _post = {
      id: posts.length + 1,
      author: author,
      post: post,
    };
    posts.push(_post);
    posts = posts;

    author = '';
    post = '';
  }
</script>

<main class="h-screen flex flex-col justify-center items-center space-y-4">
  <h1>Add Post</h1>
  <section class="space-y-4">
    <div class="form-control">
      <label for="author" class="label">
        <span class="label-text">Author</span>
      </label>
      <input
        bind:value={author}
        name="author"
        type="text"
        placeholder="Username"
        class="input input-primary input-bordered"
      />
    </div>
    <div class="form-control">
      <label for="post" class="label">
        <span class="label-text">Username</span>
      </label>
      <textarea
        class="textarea h-24 textarea-bordered textarea-primary"
        bind:value={post}
        type="text"
        name="post"
        placeholder="Text"
      />
    </div>
    <button on:click={addPost} class="btn btn-primary w-full">Submit</button>
  </section>

  <section class="overflow-auto space-y-4">
    {#each posts.reverse() as post}
      <Post author={post.author} post={post.post} />
    {/each}
  </section>

  <div>
    <div class="btn-group">
      <input
        on:click={changeChecked(1)}
        type="radio"
        name="options"
        id="option1"
        data-title="1"
        checked={isChecked === 1 ? 'checked' : ''}
        class="btn"
      />
      <input
        on:click={changeChecked(2)}
        type="radio"
        name="options"
        id="option2"
        data-title="2"
        checked={isChecked === 2 ? 'checked' : ''}
        class="btn"
      />
      <input
        on:click={changeChecked(3)}
        type="radio"
        name="options"
        id="option3"
        data-title="3"
        checked={isChecked === 3 ? 'checked' : ''}
        class="btn"
      />
      <input
        on:click={changeChecked(4)}
        type="radio"
        name="options"
        id="option4"
        data-title="4"
        checked={isChecked === 4 ? 'checked' : ''}
        class="btn"
      />
      <input
        on:click={changeChecked(5)}
        type="radio"
        name="options"
        id="option5"
        data-title="5"
        checked={isChecked === 5 ? 'checked' : ''}
        class="btn"
      />
    </div>
  </div>
</main>

<style>
</style>
