<script>
  let scroll;
  let speed = 4;
</script>

<svelte:window bind:scrollY={scroll} />

<h1>{scroll}</h1>
<section>
  <div
    class="box pin"
    style:transform={`translate3d(0, ${scroll * 1.1}px, 0)`}
    style:background="teal"
  />
  <div class="box" />
  <div class="box" />
  <div
    class="box"
    style:transform={`translate3d(0, ${scroll * -1}px, 0)`}
    style:background="red"
  />
  <div class="box" />
  <div class="box" />
  <div class="box" />
  <div class="box" />
</section>

<style>
  h1 {
    position: fixed;
    z-index: 10;
  }
  .box {
    --size: 300px;
    height: var(--size);
    width: var(--size);
    background: lightGrey;
    margin-bottom: 1rem;
  }

  /* 	.pin {
		position: fixed;
	} */
</style>
