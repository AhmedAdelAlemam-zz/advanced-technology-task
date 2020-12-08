<template>
  <div>
    <b-container fluid>
      <Navbar />
      <b-row>
        <b-col lg="1" />
        <b-col lg="10">
          <About />
          <hr />
          <Books />
          <hr />
          <Contact />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import About from "./About";
import Books from "./Books";
import Contact from "./Contact";
import Navbar from "./Navbar";
export default {
  components: {
    About,
    Books,
    Contact,
    Navbar,
  },
};
</script>
