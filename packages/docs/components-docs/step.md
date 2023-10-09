# Step

Loop a series of steps to show current project process

## Basic Usage

Combine `er-step` with `er-step-item`, and you'll get a step component. You can set the current step by activeIndex property . You also can change the mode or size by
set the property.

```vue preview
<<<<<<< HEAD
<template>
  <er-step :active-index="2">
    =======
    <script setup lang="ts">
      import { ref } from 'vue';

      const index = ref(-1);
      const next = () => index.value++;
    </script>

    <template>
      <er-step :active-index="index">
        >>>>>>> upstream/main
        <er-step-item title="开始" desc="活动详情" />
        <er-step-item title="下单" desc="浏览" />
        <er-step-item title="审核" desc="后台审核" />
        <er-step-item title="流程结束" desc="流程结束" />
      </er-step>
      <<<<<<< HEAD
    </template></er-step
  >
</template>
```

## Different Mode

=======
<er-button @click="next">下一步</er-button>
</template>

````

## Step bar with icon

A variety of custom icons can be used in the step bar.

```vue preview
<template>
  <er-step :active-index="1">
    <er-step-item title="开始" desc="下单">
      <template #icon>
        <er-icon name="zan"></er-icon>
      </template>
    </er-step-item>
    <er-step-item title="过程" desc="支付">
      <template #icon>
        <er-icon name="heart-o"></er-icon>
      </template>
    </er-step-item>
    <er-step-item title="结束" desc="送达">
      <template #icon>
        <er-icon name="clock"></er-icon>
      </template>
    </er-step-item>
  </er-step>
</template>
````

## Vertical step bar

> > > > > > > upstream/main

To change the display mode to `vertical` or `horizontal`, you can set the mode property. The default mode is horizontal.

```vue preview
<<<<<<< HEAD
<template>
  <er-button @click="changeMode" type="primary" size="small"
    >垂直/水平</er-button
  >
  =======
  <script lang="ts" setup>
    import { ref } from 'vue';
    const currentMode = ref('vertical');
    const changeMode = () => {
      currentMode.value =
        currentMode.value === 'horizontal' ? 'vertical' : 'horizontal';
    };
  </script>

  <template>
    <er-button @click="changeMode">垂直/水平</er-button>
    >>>>>>> upstream/main
    <er-step :active-index="2" :mode="currentMode">
      <er-step-item title="开始" desc="活动详情" />
      <er-step-item title="下单" desc="浏览" />
      <er-step-item title="审核" desc="后台审核" />
      <er-step-item title="流程结束" desc="流程结束" />
    </er-step>
    <<<<<<< HEAD
    <er-step :active-index="2" :mode="currentMode" size="small">
      <er-step-item title="开始" desc="活动详情" />
      <er-step-item title="下单" desc="浏览" />
      <er-step-item title="审核" desc="后台审核" />
      <er-step-item title="流程结束" desc="流程结束" />
    </er-step>
    <er-step :active-index="2" :mode="currentMode" size="mini">
      <er-step-item title="开始" desc="活动详情" />
      <er-step-item title="下单" desc="浏览" />
      <er-step-item title="审核" desc="后台审核" />
      <er-step-item title="流程结束" desc="流程结束" />
    </er-step>
  </template>
  <script lang="ts" setup>
    import { ref } from 'vue';
    const currentMode = ref('horizontal');
    const changeMode = () => {
      currentMode.value =
        currentMode.value === 'horizontal' ? 'vertical' : 'horizontal';
    };
  </script>
</template>
```

## Different Size

```vue preview
<template>
  <er-step size="default" :active-index="2" :mode="currentMode">
    <er-step-item title="开始" desc="活动详情" />
    <er-step-item title="下单" desc="浏览" />
    <er-step-item title="审核" desc="后台审核" />
    <er-step-item title="流程结束" desc="流程结束" />
  </er-step>
  <er-step size="small" :active-index="2" :mode="currentMode">
    <er-step-item title="开始" desc="活动详情" />
    <er-step-item title="下单" desc="浏览" />
    <er-step-item title="审核" desc="后台审核" />
    <er-step-item title="流程结束" desc="流程结束" />
  </er-step>
  <er-step size="mini" :active-index="2" :mode="currentMode">
    <er-step-item title="开始" desc="活动详情" />
    <er-step-item title="下单" desc="浏览" />
    <er-step-item title="审核" desc="后台审核" />
    <er-step-item title="流程结束" desc="流程结束" />
  </er-step>
</template>
```

## Dynamic setting activeIndex

You can dynamically set the current step through a reactive property called activeIndex

```vue preview
<script lang="ts" setup>
import { ref } from 'vue';
const activeIndex = ref(0);
const setActive = () => {
  activeIndex.value++;
};
</script>
<template>
  <er-button type="primary" @click="setActive">步骤推进</er-button>
  <er-step size="mini" :active-index="activeIndex" :mode="currentMode">
    <er-step-item />
    <er-step-item />
    <er-step-item />
    <er-step-item />
    <er-step-item />
    <er-step-item />
    <er-step-item />
    <er-step-item />
=======
</template>
```

## Sizes

```vue preview
<template>
  <er-step size="large" :active-index="2">
    <er-step-item title="开始" desc="活动详情" />
    <er-step-item title="下单" desc="浏览" />
    <er-step-item title="审核" desc="后台审核" />
    <er-step-item title="流程结束" desc="流程结束" />
  </er-step>
  <er-step :active-index="2">
    <er-step-item title="开始" desc="活动详情" />
    <er-step-item title="下单" desc="浏览" />
    <er-step-item title="审核" desc="后台审核" />
    <er-step-item title="流程结束" desc="流程结束" />
  </er-step>
  <er-step size="small" :active-index="2">
    <er-step-item title="开始" desc="活动详情" />
    <er-step-item title="下单" desc="浏览" />
    <er-step-item title="审核" desc="后台审核" />
    <er-step-item title="流程结束" desc="流程结束" />
    >>>>>>> upstream/main
  </er-step>
</template>
```

## Step API

### Step Attributes

<<<<<<< HEAD
| Name | Description | Type | Default |
| ----------- | -------------------------------------- | --------------------- | ---------- |
| mode | Set the horizontal or vertical display | `horizontal/vertical` | horizontal |
| size | Set the size | `mini/small/default` | default |
| activeIndex | Set current step | `number | -1 |

### Step Methods

| Name           | Description                | Parameters |
| -------------- | -------------------------- | ---------- |
| getActiveIndex | Get the current step index | -          |

=======
| Name | Description | Type | Default |
| ------------ | ----------------------- | --------------------------------- | ------------ |
| mode | display direction | `'vertical' \| 'horizontal'` | `horizontal` |
| active-index | current activation step | `number` | `-1` |
| size | button size | `'large' \| 'default' \| 'small'` | `default` |

### Step Methods

| Name           | Description                   | Parameters            |
| -------------- | ----------------------------- | --------------------- |
| getActiveIndex | get current active Step index | 'activeIndex: number' |

## StepItem API

> > > > > > > upstream/main

### StepItem Attributes

| Name | Description | Type | Default |
| ---- | ----------- | ---- | ------- |

<<<<<<< HEAD
| title | Set main title | `string` | - |
| desc | Set the subtitle | `string` | - |
=======
| title | step title | `string` | `''` |
| desc | step description | `string` | `''` |

### StepItem Slots

| Name | Description |
| ---- | ----------- |
| icon | custom icon |

> > > > > > > upstream/main
