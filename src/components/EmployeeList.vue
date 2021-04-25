<template>
  <div>
    <h1 style="color: black;">Corona API</h1>
    <div class="limiter">
      <div class="container-table100">
        <div class="wrap-table100">
          <div class="table100">
            <table>
              <thead>
                <tr class="table100-head">
                  <th class="column1">Vaka Sayısı</th>
                  <th class="column2">Vefat Sayısı</th>
                  <th class="column3">Test Sayısı</th>
                </tr>
              </thead>
              <tr
                style="color: #b5001c;"
                v-for="item in list"
                v-bind:key="item.id"
              >
                <td class="column1">{{ item.infected }}</td>
                <td class="column2">{{ item.deceased }}</td>
                <td class="column3">{{ item.tested }}</td>
              </tr>
            </table>
          </div>
        </div>
      </div>
      <h1 style="color: #444E59;">
        Bilgiler her gün otomatik güncellenmektedir.
        <a
          aria-label="VueJS Project Site"
          rel="noopener"
          style="text-decoration:none; color: #F2B755;"
          target="blank__"
          href="https://covid19.saglik.gov.tr"
          ><br />covid19.saglik.gov.tr</a
        >
      </h1>
    </div>
    <footer class="footer">
      <div class="footer__copy">
        Copyright &copy; {{ new Date().getFullYear() }}
        <strong>JuPiteRRY</strong>
      </div>
      <div class="footer__love">
        We <span><i class="fas fa-heart"></i> love</span>
        <a
          aria-label="VueJS Project Site"
          rel="noopener"
          target="_blank"
          href="https://vuejs.org"
          >VueJS</a
        >
      </div>
      <div class="footer__links"></div>
    </footer>
  </div>
</template>
<script>
import Vue from "vue";
import axios from "axios";
import VueAxios from "vue-axios";

Vue.use(VueAxios, axios);
export default {
  name: "EmployeeList",
  data() {
    return { list: undefined };
  },
  mounted() {
    Vue.axios
      .get(
        "https://api.apify.com/v2/key-value-stores/28ljlt47S5XEd1qIi/records/LATEST?disableRedirect=true"
      )
      .then((resp) => {
        this.list = resp;
        console.warn(resp.data);
      });
  },
};
</script>
