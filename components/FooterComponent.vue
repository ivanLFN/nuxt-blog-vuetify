<template>
    <v-container>
      <v-row justify="space-between mt-5">
        <v-col cols="12" md="3">
          <div class="footer-header">
            About
          </div>
          <div class="footer-slogan mt-3">
            Innovation for your success. Together in the future. We will implement your ideas. Technologies for growing your business. Trust us with your future and we will make it better.
          </div>
          <div class="general-info mt-3">
            <span class="general-info-header">Email:</span> info@jstemplate.net <br>
            <span class="general-info-header">Phone:</span> 880 123 456 789
          </div>
        </v-col>

        <v-col cols="12" md="5" class="mt-md-0 mt-4">
          <v-row justify="center">
            <v-col cols="4">
              <div class="d-flex flex-column align-items-start">
                <div class="footer-header">
                  Quick Link
                </div>
                <v-list dense class="pl-0 text-start footer-link-style">
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Home</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">About</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Blog</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Archived</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Contact</v-list-item-title>
                  </v-list-item>
                </v-list>
              </div>
            </v-col>

            <v-col cols="4">
              <div class="d-flex flex-column align-items-start">
                <div class="footer-header">
                  Category
                </div>
                <v-list dense class="footer-link-style">
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">For customer</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Business</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">For manager</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Web</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Mobile</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">UI/UX</v-list-item-title>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-title class="footer-link-between">Checklists</v-list-item-title>
                  </v-list-item>
                </v-list>
              </div>
            </v-col>
          </v-row>
        </v-col>

        <v-col cols="12" md="4" class="mt-md-0 mt-4">
          <div class="news-form px-5">
            <div class="text-center">
              <div class="form-header-first pt-5">
                Weekly Newsletter
              </div>
              <div class="form-header mt-2">
                Get blog articles and offers via email
              </div>
            </div>
            <div>
              <v-form action="/subscribe" method="post">
                <v-row class="mt-4">
                  <v-col cols="12" sm="8">
                    <v-text-field
                      v-model="email"
                      label="Your Email"
                      required
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" sm="4">
                    <v-btn class="submit-btn" type="submit">Subscribe</v-btn>
                  </v-col>
                </v-row>
              </v-form>
            </div>
          </div>
        </v-col>
      </v-row>

      <v-row class="bottom-part mt-5">
        <v-col cols="12" md="4" class="d-flex">
          <div>
            <v-img src="https://img.icons8.com/color/96/bootstrap--v2.png" max-height="50" contain></v-img>
          </div>
          <div>
            Bootstrap
            <div>© JS Template 2024. All Rights Reserved.</div>
          </div>
        </v-col>

        <v-col cols="12" md="8" class="text-md-end mt-md-0 mt-4">
          <v-btn text class="footer-link px-md-3 px-1 bottom-link">Terms of Use</v-btn>
          <v-btn text class="footer-link px-md-3 px-1 bottom-link">Privacy Policy</v-btn>
          <v-btn text class="footer-link px-md-3 px-1">Cookie Policy</v-btn>
        </v-col>
      </v-row>
    </v-container>
</template>

<script>
export default {
  data() {
    return {
      email: ''
    }
  }
}
</script>

<style lang="scss">

.form-header-first {
  font-size: 1.5rem !important;
}

.footer-link-between {
  font-weight: 300 !important;
  font-size: 1.1rem !important;
}

.bottom-link {
  border-right: 1px solid #DCDDDF;
}

.bottom-part {
  border-top: 1px solid #DCDDDF;
  margin-top: 5rem;
}

.footer-link {
  text-decoration: none;
  color: #3B3C4A;
}

.footer-header {
  font-size: 1.4rem;
  color: #181A2A;
  font-weight: 450;
}

.general-info-header {
  color: #181A2A;
  font-weight: bolder;
}

.general-info {
  color: #3B3C4A;
}

.footer-slogan {
  color: #696A75;
  font-weight: 350;
}

.form-header {
  color: #696A75;
}

.form-input {
  padding: 10px;
  border: 1px solid #97989F;
  border-radius: 5px;
}

.input {
  width: 100%;
  border: none;
}

.form-img {
  width: 30px;
  height: auto;
  margin-left: 10px;
}

.news-form {
  background-color: white;
  border-radius: 15px;
}

.submit-btn {
  background-color: #7B4DFF;
  padding: 10px 0;
  border-radius: 5px;
  color: white;
  text-decoration: none;
  font-weight: 350;
}

.footer-link-style {
  background-color: #F5F5F5 !important;
}

</style>
