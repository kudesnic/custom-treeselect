<template>
  <div>
    <treeselect
      :multiple="true"
      :options="options"
      :value-consists-of="valueConsistsOf"
      v-model="value"
      />
    <pre class="result">{{ value }}</pre>
    <p><strong>Value consists of:</strong></p>
    <p class="options">
      <label><input type="radio" value="ALL" v-model="valueConsistsOf">All</label>
      <label><input type="radio" value="BRANCH_PRIORITY" v-model="valueConsistsOf">Branch priority</label>
      <label><input type="radio" value="LEAF_PRIORITY" v-model="valueConsistsOf">Leaf priority</label>
    </p>
  </div>
</template>

<script>
  export default {
    data: () => ({
      value: [],
      valueConsistsOf: 'BRANCH_PRIORITY',
      options: [ {
        id: 'company',
        label: 'Company 🏢',
        children: [ {
          id: 'group-i',
          label: 'Group I 👥',
          children: [ {
            id: 'person-a',
            label: 'Person A 👱',
          }, {
            id: 'person-b',
            label: 'Person B 🧔',
          } ],
        }, {
          id: 'group-ii',
          label: 'Group II 👥',
          children: [ {
            id: 'person-c',
            label: 'Person C 👳',
          }, {
            id: 'person-d',
            label: 'Person D 👧',
          } ],
        }, {
          id: 'person-e',
          label: 'Person E 👩',
        } ],
      } ],
    }),
  }
</script>
