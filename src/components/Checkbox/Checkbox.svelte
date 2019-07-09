<script>
  export let checked = false;
  export let label = "";
  export let id = "checkbox" + Math.round(Math.random() * 95002000);
</script>

<style type="text/scss">
  .checkbox {
    --text-color: rgba(0, 0, 0, 0.75);
    margin: 14px;

    * {
      cursor: pointer;
    }

    &__marker {
      width: 16px;
      height: 16px;
      border-radius: 3px;
      background: transparent;
      border: 2px solid grey;
    }

    &__input {
      border: 0;
      clip: rect(0 0 0 0);
      height: 1px;
      margin: -1px;
      overflow: hidden;
      padding: 0;
      position: absolute;
      width: 1px;
      outline: 0;
      -webkit-appearance: none;
    }

    &__label {
      user-select: none;
      margin-left: 12px;
      font-size: 14px;
      color: var(--text-color);
    }

    &:checked {
      // Checked state
      .checkbox__marker {
        background: #ddd;
      }
    }
  }
</style>

<label class="checkbox" for={id}>
  <input {id} class="checkbox__input" type="checkbox" bind:checked />
  <div class="checkbox__marker" />
  {#if label}
    <div class="checkbox__label">{label}</div>
  {/if}
</label>
