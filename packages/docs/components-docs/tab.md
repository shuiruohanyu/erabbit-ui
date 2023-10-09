# Tab

Tab component

## Basic Usage

<<<<<<< HEAD
Combine `er-tabs` with `er-tabs-panel`, and you'll get a tabs component. You can set the current active by v-model property . You also can change the size or type by
=======
Combine `er-tab` with `er-tab-panel`, and you'll get a tabs component. You can set the current active by v-model property . You also can change the size or type by

> > > > > > > upstream/main
> > > > > > > set the property.

```vue preview
<script lang="ts" setup>
import { ref } from 'vue';
const activeName = ref('begin');
</script>
<<<<<<< HEAD
<template>
  <er-tabs v-model="activeName">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
  =======

  <template>
    <er-tab v-model="activeName">
      <er-tab-panel label="开始" name="begin">1</er-tab-panel>
      <er-tab-panel label="下单" name="order">2</er-tab-panel>
      <er-tab-panel label="审核" name="approval">3</er-tab-panel>
      <er-tab-panel label="流程结束" name="end">4</er-tab-panel>
    </er-tab>
    >>>>>>> upstream/main
  </template>
</template>
```

## Different size

<<<<<<< HEAD
To change the display size to `mini/small`, you can set the size property. The default size is default.

````vue preview
<template>
  <er-button @click="changeSize" type="primary" size="small"
    >default/small/mini</er-button
  >
  <er-tabs v-model="activeName" :size="size">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
</template>
======= To change the display size to `small` `large`, you can set the size
property. The default size is `default`. ```vue preview
<template>
  <er-tab :size="size">
    <er-tab-panel label="开始" name="begin">1</er-tab-panel>
    <er-tab-panel label="下单" name="order">2</er-tab-panel>
    <er-tab-panel label="审核" name="approval">3</er-tab-panel>
    <er-tab-panel label="流程结束" name="end">4</er-tab-panel>
  </er-tab>
  <er-button @click="change"> default/small/large </er-button>
</template>

>>>>>>> upstream/main
<script lang="ts" setup>
import { ref } from 'vue';
const activeName = ref('begin');
const size = ref('default');
<<<<<<< HEAD
let list = ['small', 'mini', 'default'];
const changeSize = () => {
=======

let list = ['small', 'large', 'default'];
const change = () => {
>>>>>>> upstream/main
  size.value = list[0];
  list = [...list.slice(1), list[0]];
};
</script>
````

## Different Position

```vue preview
<template>
  <<<<<<< HEAD
  <er-tabs v-model="activeName" :size="size" tab-position="left">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
  <er-tabs v-model="activeName" :size="size" tab-position="right">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
  <er-tabs v-model="activeName" :size="size" tab-position="top">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
  <er-tabs v-model="activeName" :size="size" tab-position="bottom">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
</template>
<script lang="ts" setup>
import { ref } from 'vue';
const activeName = ref('begin');
const size = ref('default');
let list = ['small', 'mini', 'default'];
const changeSize = () => {
  size.value = list[0];
=======
  <er-tab :tab-position="position">
    <er-tab-panel label="开始" name="begin">1</er-tab-panel>
    <er-tab-panel label="下单" name="order">2</er-tab-panel>
    <er-tab-panel label="审核" name="approval">3</er-tab-panel>
    <er-tab-panel label="流程结束" name="end">4</er-tab-panel>
  </er-tab>
  <er-button @click="change"> top/right/bottom/left </er-button>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
const position = ref('top');

let list = ['top', 'right', 'bottom', 'left'];
const change = () => {
  position.value = list[0];
>>>>>>> upstream/main
  list = [...list.slice(1), list[0]];
};
</script>
```

## Different type

<<<<<<< HEAD
You can set the type `card/border-card` to change the showMode

````vue preview
<template>
  <er-tabs type="card">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
  <er-tabs type="border-card">
    <er-tabs-panel label="开始" name="begin">1</er-tabs-panel>
    <er-tabs-panel label="下单" name="order">2</er-tabs-panel>
    <er-tabs-panel label="审核" name="approval">3</er-tabs-panel>
    <er-tabs-panel label="流程结束" name="end">4</er-tabs-panel>
  </er-tabs>
</template>
======= You can set the type `card` `border-card` to change the showMode ```vue
preview
<template>
  <er-tab :type="type">
    <er-tab-panel label="开始" name="begin">1</er-tab-panel>
    <er-tab-panel label="下单" name="order">2</er-tab-panel>
    <er-tab-panel label="审核" name="approval">3</er-tab-panel>
    <er-tab-panel label="流程结束" name="end">4</er-tab-panel>
  </er-tab>
  <er-button @click="change"> card/border-card/default </er-button>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
const type = ref('');

let list = ['card', 'border-card', ''];
const change = () => {
  type.value = list[0];
  list = [...list.slice(1), list[0]];
};
</script>
>>>>>>> upstream/main
````

## Tabs API

### Tabs Attributes

| Name    | Description        | Type            | Default |
| ------- | ------------------ | --------------- | ------- |
| v-model | Set the active Tab | `string/number` | -       |

<<<<<<< HEAD
| size | Set the size | `mini/small/default` | default |
=======
| size | Set the size | `large/small/default` | default |

> > > > > > > upstream/main
> > > > > > > | type | Set the show Mode | `default/card/border-card` | default |
> > > > > > > | tabPosition | Set the tabs direction | `left/right/top/bottom` | top |

### Tabs Event

| Name      | Description                   | Parameters              |
| --------- | ----------------------------- | ----------------------- |
| tab-click | trigger it when click the tab | tabspanel name or index |

### TabsPanel Attributes

| Name  | Description                     | Type     | Default |
| ----- | ------------------------------- | -------- | ------- |
| label | Set show tab title              | `string` | -       |
| name  | Set the unqiue value of the tab | `string` | -       |
