<template>
  <div id="app">
        <EmployeeList />
  </div>
</template>
<script>
import EmployeeList from './components/EmployeeList'
export default {
  name: 'App',
  components: {
    EmployeeList
  }
}
</script>

<style>
html {
  background-color:white;
}
body {
  overflow: hidden; /* Hide scrollbars */
}

#app {
  
  font-family: 'Open Sans', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}
.limiter {
  width: 100%;
  margin: 0 auto;
}

.container-table100 {
  width: 100%;
  min-height: 20vh;
  display: -webkit-box;
  display: -webkit-flex;
  display: -moz-box;
  display: -ms-flexbox;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  padding: 33px 30px;
}

.wrap-table100 {
  width: 1170px;
}

table {
  border-spacing: 1;
  border-collapse: collapse;
  background: white;
  border-radius: 25px;
  overflow: hidden;
  width: 100%;
  margin: 0 auto;
  position: relative;
}
table * {
  position: relative;
}
table td, table th {
  padding-left: 8px;
}
table thead tr {
  height: 60px;
  background: #23272A;
}
table tbody tr {
  height: 50px;
}
table tbody tr:last-child {
  border: 0;
}
table td.l, table th.l {
  text-align: right;
}
table td.c, table th.c {
  text-align: center;
}
table td.r, table th.r {
  text-align: center;
}


.table100-head th{
  font-family: 'Open Sans', sans-serif;
  font-size: 18px;
  
  color: #fff;
  line-height: 1.2;
  font-weight: unset;
}

tbody tr:nth-child(even) {
  background-color: #f5f5f5;
}

tbody tr {
  font-family: 'Open Sans', sans-serif;
  font-size: 15px;
  color: #808080;
  line-height: 1.2;
  font-weight: unset;
}

tbody tr:hover {
  color: #555555;
  background-color: #f5f5f5;
  cursor: pointer;
}

.column1 {
  width: 260px;
  padding-left: 40px;
}

.column2 {
  width: 160px;
}

.column3 {
  width: 245px;
}

.column4 {
  width: 110px;
  text-align: right;
}

.column5 {
  width: 170px;
  text-align: right;
}

.column6 {
  width: 222px;
  text-align: right;
  padding-right: 62px;
}


@media screen and (max-width: 120px) {
  table {
    display: block;
  }
  table > *, table tr, table td, table th {
    display: block;
  }
  table thead {
    display: none;
  }
  table tbody tr {
    height: auto;
    padding: 20px 0;
  }
  table tbody tr td {
    padding-left: 40% !important;
    margin-bottom: 24px;
  }
  table tbody tr td:last-child {
    margin-bottom: 0;
  }
  table tbody tr td:before {
    font-family: OpenSans-Regular;
    font-size: 14px;
    color: #999999;
    line-height: 1.2;
    font-weight: unset;
    position: absolute;
    width: 40%;
    left: 30px;
    top: 0;
  }
  .column4,
  .column5,
  .column6 {
    text-align: left;
  }

  .column4,
  .column5,
  .column6,
  .column1,
  .column2,
  .column3 {
    width: 100%;
  }

  tbody tr {
    font-size: 14px;
  }
}


.footer {
  margin-top: auto;
  padding-bottom: 40px;
  display: flex;
  position: relative;
  top: 370px;
  justify-content: space-between;
  align-items: center;
}

.footer__copy {
  font-size: 16px;
  color: #626262;
  flex: 6;
}
.footer__copy strong {
  margin-left: 4px;
}
.footer__love {
  flex: 1;
  color: #626262;
  font-weight: 600;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}
.footer__love span {
  color: #b5001c;
  font-weight: 800;
  margin: 0 8px;
  display: inline-flex;
  align-items: center;
  opacity: 0.8;
}
.footer__love span i {
  font-size: 12px;
  margin-right: 3px;
}
.footer__love a {
  color: #626262;
  text-decoration: none;
  outline: none;
}
.footer__links {
  flex: 2;
  justify-content: flex-end;
  display: flex;
}
.footer__links a {
  margin-left: 20px;
  color: #626262;
  text-decoration: none;
  outline: none;
  transition: all 0.4s;
}
.footer__links a:hover {
  color: #000;
}
</style>
