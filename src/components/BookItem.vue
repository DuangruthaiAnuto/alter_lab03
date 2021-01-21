<template>
  <div>
    <div class="book-item">
      <h1>{{ book.title }}</h1>

      <div style="width: 100%; text-align: left">
        <img
          style="float: left; padding: 20px"
          width="150px"
          v-bind:src="book.thumbnailUrl"
        />
        <div style="padding:20px;">
          <b>Author:</b>{{ book.author }}<br />
          <b>Category:</b>{{ book.category }}<br />
          <b>ISBN:</b>{{ book.isbn }}<br />
          <b>Page:</b>{{ book.pageCount }}<br />
          <b>Description:</b><br />
          <p>{{ book.shortDescription }}</p>
        </div>
      </div>
      <br />
    </div>
  </div>
</template>

<script>
export default {
  name: "BookItem",
  components: {},
  props: ["book"],
};
</script>



<style>
.book-item {
  background: #f4f4f4;
  padding: 50px;
  border-bottom: 1px #cccccc dotted;
}
</style>