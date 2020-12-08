<template>
  <div id="books" class="pt-5">
    <b-row class="pt-5">
      <b-col lg="12">
        <h1>Best seller books</h1>
      </b-col>
      <b-col lg="3" class="mb-5" v-for="book in books" :key="book.id">
        <div class="border border-dark rounded">
          <img
            :src="book.book_image"
            class="img-fluid w-100 book-img rounded-top"
          />
          <div class="p-3 book-desc-height">
            <h6 class="font-weight-bold pb-3">
              {{ book.title }}
            </h6>
            <h6 class="pb-3 font-weight-bold">
              By: {{ book.author }} | {{ book.publisher }}
            </h6>
            <p class="text-muted font-weight-bold">
              {{ book.description }}
            </p>
          </div>
          <div class="p-4">
            <b-row>
              <b-col lg="3" />
              <b-col lg="6">
                <b-dropdown
                  id="dropdown-1"
                  class="w-100 buy-btn"
                  variant="info"
                >
                  <template #button-content>
                    <strong class="float-left">Buy</strong>
                  </template>
                  <b-dropdown-item
                    class="dropdown-item"
                    v-for="link in book.buy_links"
                    :key="link.id"
                    :href="link.url"
                    target="_blank"
                  >
                    {{ link.name }}
                  </b-dropdown-item>
                </b-dropdown>
              </b-col>
            </b-row>
          </div>
        </div>
      </b-col>
    </b-row>
  </div>
</template>
<script>
import Axios from "axios";
export default {
  props: {
    books: [],
  },
  mounted() {
    const apiKey = "dV8LWpuXDGW7ojE1FTwBFugbMI9cyCJx";
    Axios.get(
      `https://api.nytimes.com/svc/books/v3/lists/current/hardcover-fiction.json?api-key=${apiKey}`
    ).then((res) => {
      this.books = res.data.results.books;
      console.log(this.books);
    });
  },
};
</script>
<style scoped lang="scss">
.book-img {
  height: 500px !important;
}

.book-desc-height {
  height: 250px;
}
#books .col-lg-3 .border:hover {
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important;
  color: #8fc7c9;
  border-color: #8fc7c9 !important;
  border-width: 2px !important;
  p {
    color: #000 !important;
  }
  .buy-btn:hover {
    box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important;
  }
}
</style>
