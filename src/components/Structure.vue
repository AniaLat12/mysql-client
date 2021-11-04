<template>
    <section>
      <div class="table-title">{{ table.toUpperCase() }}</div>
    <table>
      <tr>
        <th>NAME</th>
        <th>TYPE</th>
        <th>NULL</th>
        <th>KEY</th>
        <th>DEFAULT</th>
        <th>EXTRA</th>
      </tr>
      <tr v-for="src in structure" :key="src.Field">
        <td> {{src.Field}} </td>
        <td> {{src.Type}} </td>
        <td> {{src.Null}} </td>
        <td> {{src.Key}} </td>
        <td> {{src.Default}} </td>
        <td> {{src.Extra}} </td>
        {{ name }}

      </tr>
    </table>
  </section>
</template>

<script>
export default {
    name: "Structure",
    props: {
        name: String
    }
}
</script>

<style>

</style>