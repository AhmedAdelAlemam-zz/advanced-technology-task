<template>
  <div class="py-5" id="contact">
    <b-row>
      <b-col lg="4" />
      <b-col lg="4">
        <h1 class="text-center">Contact us</h1>
      </b-col>
    </b-row>
    <b-row class="pt-5">
      <b-col lg="3" />
      <b-col lg="6">
        <form
          class="needs-validation"
          novalidate
          v-on:submit.prevent="onSubmit"
        >
          <div class="form-row">
            <b-col lg="12" class="mb-3">
              <label for="validationCustom01">Your name</label>
              <input
                type="text"
                class="form-control"
                id="validationCustom01"
                placeholder="Your name"
                required
              />
              <div class="valid-feedback">
                Looks good!
              </div>
              <div class="invalid-feedback">
                Please enter your name.
              </div>
            </b-col>
            <b-col lg="12" class="mb-3">
              <label for="validationCustom02">Your email</label>
              <input
                type="text"
                class="form-control"
                id="validationCustom02"
                placeholder="Your email"
                required
              />
              <div class="valid-feedback">
                Looks good!
              </div>
              <div class="invalid-feedback">
                Please enter your email address.
              </div>
            </b-col>
          </div>
          <div class="form-row">
            <b-col lg="12" class="mb-3">
              <label for="validationCustom03">Mobile number</label>
              <input
                type="text"
                class="form-control"
                id="validationCustom03"
                placeholder="Mobile number"
                required
              />
              <div class="valid-feedback">
                Looks good!
              </div>
              <div class="invalid-feedback">
                Please provide a valid mobile.
              </div>
            </b-col>
            <b-col lg="12" class="mb-3">
              <label for="validationCustom04">Leave a message</label>
              <textarea
                rows="5"
                cols="10"
                class="form-control"
                id="validationCustom05"
                placeholder="Your message"
                required
              />
              <div class="valid-feedback">
                Looks good!
              </div>
              <div class="invalid-feedback">
                Please leave a message to us.
              </div>
            </b-col>
          </div>
          <div class="form-group">
            <div class="form-check">
              <input
                class="form-check-input"
                type="checkbox"
                value=""
                id="invalidCheck"
                required
              />
              <label class="form-check-label" for="invalidCheck">
                Agree to terms and conditions
              </label>
              <div class="valid-feedback">
                Looks good!
              </div>
              <div class="invalid-feedback">
                You must agree before submitting.
              </div>
            </div>
          </div>
          <button class="btn btn-primary" type="submit">
            Submit form
          </button>
        </form>
      </b-col>
    </b-row>
  </div>
</template>
<script>
export default {
  methods: {
    onSubmit: () => {
      window.addEventListener(
        "load",
        function() {
          // Fetch all the forms we want to apply custom Bootstrap validation styles to
          var forms = document.getElementsByClassName("needs-validation");
          // Loop over them and prevent submission
          Array.prototype.filter.call(forms, function(form) {
            form.addEventListener(
              "submit",
              function(event) {
                if (form.checkValidity() === false) {
                  event.preventDefault();
                  event.stopPropagation();
                }
                form.classList.add("was-validated");
              },
              false
            );
          });
        },
        false
      );
    },
  },
  mounted() {
    this.onSubmit();
  },
};
</script>
