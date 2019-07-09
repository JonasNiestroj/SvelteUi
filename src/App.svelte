<script>
  import Buttons from "./demo/Buttons.svelte";
  import UiComponents from "./demo/UiComponents.svelte";
  import { Screen } from "./components/Layout";

  import { Ripple } from "./components/Ripple";
  import { ToggleButton } from "./components/Toggle";
  import { ToggleGroup } from "./components/Toggle";
</script>

<style type="text/scss">
  :global(body) {
    margin: 0;
  }
  .headbar {
    width: 100%;
    height: 55px;
    display: flex;
    border-bottom: 1px solid rgba(0, 0, 0, 0.25);
    margin-bottom: 20px;
    color: rgba(0, 0, 0, 0.85);
    align-items: center;

      &__center {
        max-width: 1200px;
        margin: 0 auto;
        width: 100%;
        display: flex;
        align-items: center;
      }

      &__link {
        display: inline-flex;
        border-radius: 5px;
        padding: 8px 10px;
        cursor: pointer;
        position: relative;
        font-size: 14px;
      }
  }
</style>

<div class="headbar">
  <div class="headbar__center">
    <div class="headbar__link">
      Textfields
      <Ripple color="#000000" />
    </div>

    <ToggleGroup useNestedElements={false}>
      <ToggleButton>Circle Navigation</ToggleButton>
    </ToggleGroup>

  </div>
</div>
<Screen>
  <UiComponents />
</Screen>
