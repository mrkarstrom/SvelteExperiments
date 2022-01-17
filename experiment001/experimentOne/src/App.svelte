<script>
  let isChecked = 1;

  function changeChecked(checkedNum) {
    isChecked = checkedNum;
  }
</script>

<main class="flex flex-col justify-center items-center h-screen space-y-4">
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
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    text-align: center;
    padding: 1em;
    margin: 0 auto;
  }

  img {
    height: 16rem;
    width: 16rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin: 2rem auto;
    max-width: 14rem;
  }

  p {
    max-width: 14rem;
    margin: 1rem auto;
    line-height: 1.35;
  }

  @media (min-width: 480px) {
    h1 {
      max-width: none;
    }

    p {
      max-width: none;
    }
  }
</style>
