<style>
  .group {
    display: flex;
    flex-wrap: wrap;
  }
  :global(.popover + .popover) {
    margin: 0 10px !important;
  }

  .content {
    padding: 10px;
    background: #fff;
  }
</style>

<div class="group">
  {#each bopomofo as e}
  <Popover arrowColor="#fff" action="hover">
    <button slot="target">{e.zhuyin}</button>
    <div slot="content" class="content">{e.origin}</div>
  </Popover>
  {/each}

</div>

<script>
  import Popover from 'svelte-popover'
  const bopomofo = [
	  { zhuyin: 'ㄅ', origin: '「包」之古字，取其聲'},
	  { zhuyin: 'ㄆ', origin: '「扑」之古字，取其聲'},
  ]
</script>
