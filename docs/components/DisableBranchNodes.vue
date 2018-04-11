<template>
  <treeselect
    :options="options"
    :disable-branch-nodes="true"
    :show-count="true"
    :multiple="true"
    placeholder="Where are you from?"
    :enable-country-searching="true"
    :hide-selected="true"
    />
</template>

<script>
  import countries from './data/countries-of-the-world'

  export default {
    data: () => ({
      options: countries,
    }),
  }
</script>
