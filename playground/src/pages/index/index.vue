<script setup lang='ts'>
import { ref } from 'vue'

const tree = ref({
  label: 'Top Level',
  children: [
    { label: 'First Level' },
    { label: 'First Level', children: [{ label: 'Second Level' }] },
  ],
})
</script>

<template>
  <div class="block">
    <h1>Basic (4)</h1>
    <ComponentA msg="a" />
    <component-b msg="b" />
    <ComponentC msg="c" />
    <ComponentD />
    <h3>Recursive Components</h3>
    <recursive :data="tree" />
    <Book />
  </div>

  <div class="block">
    <h1>Ano UI (2)</h1>
    <AButton>Button</AButton>
  </div>

  <div class="block">
    <h1>Uni UI (2)</h1>
    <uni-calendar
      :insert="true"
      :lunar="true"
      start-date="2019-3-2"
      end-date="2019-5-20"
    />
    <uni-test>test</uni-test>
  </div>
  <div class="block">
    <h1>Wot Design Uni</h1>
    <wd-button type="success" block>
      Button
    </wd-button>
  </div>
  <div class="block">
    <h1>Uv UI</h1>
    <uv-button type="success" block>
      Button
    </uv-button>
  </div>
</template>

<style scoped>
.block {
  padding: 0px 20px 10px 20px;
  margin: 20px 20px;
  border: 1px solid #888;
  border-radius: 5px;
}
</style>
