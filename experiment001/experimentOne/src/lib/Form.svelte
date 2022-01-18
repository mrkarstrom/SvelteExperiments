<script>
  export let addPost;
  let author = '';
  let post = '';

  function sendAddPost() {
    addPost(author, post);
    author = '';
    post = '';
  }
</script>

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
  <button on:click={sendAddPost} class="btn w-full">Submit</button>
</section>
