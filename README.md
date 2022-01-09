# vue-codejar

> [CodeJar](https://github.com/antonmedv/codejar) for Vue.

## Installation

```bash
npm install DiscreteTom/vue-codejar
```

## Usage

```vue
<template>
  <code-jar @input="onInput" code-style="background:white;" lang="js" />
</template>

<script>
import CodeJar from "vue-codejar";

export default {
  components: { CodeJar },
  data() {
    return {
      code: "",
    };
  },
  methods: {
    onInput(code) {
      console.log(code);
    },
  },
};
</script>
```

## Props & Events

- Props
  - `value`: the code content.
  - `readonly`
  - `code-style`
  - `lang`: will add a class `language-${lang}` to the code editor, which is useful when you need to highlight your code.
  - `highlighter`: CodeJar highlighter function, see https://github.com/antonmedv/codejar .
  - `line-numbers`: show line number.
- Events
  - `input`: emit the code content.

> `v-model` is supported, but is not recommended since it will resulting in poor performance.

## License

MIT
