<template>
  <div style="margin-top: 80px;">
    <div>
      <table class="table table-bordered">
        <thead>
        <tr>
          <th scope="col" colspan="2" style="background-color: #f2f2f2">조회조건 입력</th>
        </tr>
        </thead>
        <tbody>
        <tr>
          <th scope="row" style="background-color: #f2f2f2">코드</th>
          <td><input type="text" class="form-control" placeholder="코드를 입력하세요"></td>
        </tr>
        <tr>
          <th scope="row" style="background-color: #f2f2f2">지역</th>
          <td>
            <div class="form-row">
              <label style="padding-right: 5px;">
                <select id="sidoCd" class="form-control">
                  <option value="*">시/도</option>
                  <option value="36">세종특별자치시</option>
                  <option value="50">제주특별자치도</option>
                  <option value="48">경상남도</option>
                  <option value="47">경상북도</option>
                  <option value="46">전라남도</option>
                  <option value="45">전라북도</option>
                  <option value="44">충청남도</option>
                  <option value="43">충청북도</option>
                  <option value="42">강원도</option>
                  <option value="41">경기도</option>
                  <option value="31">울산광역시</option>
                  <option value="30">대전광역시</option>
                  <option value="29">광주광역시</option>
                  <option value="28">인천광역시</option>
                  <option value="27">대구광역시</option>
                  <option value="26">부산광역시</option>
                  <option value="11">서울특별시</option>
                </select>
              </label>
              <label style="padding-right: 5px;">
                <select id="sggCd" class="form-control">
                  <option value="*">시/군/구</option>
                </select>
              </label>
              <label style="padding-right: 5px;">
                <select id="umdCd" class="form-control">
                  <option value="*">읍/면/동</option>
                </select>
              </label>
              <label style="padding-right: 5px;">
                <select id="riCd" class="form-control">
                  <option value="*">리</option>
                </select>
              </label>
            </div>
          </td>
        </tr>
        </tbody>
      </table>
    </div>
    <div class="float-md-right" style="width: 90px;">
      <button type="button" class="btn btn-block btn-md btn-secondary">검색</button>
    </div>
    <br><br><br>
    <div>
      <b-table id="code-table" class="table-bordered" striped hover :items="items" :per-page="perPage"
               :current-page="currentPage"></b-table>
    </div>
    <div class="overflow-auto" align="center">
      <b-pagination
        v-model="currentPage"
        :total-rows="rows"
        :per-page="perPage"
        aria-controls="result-table"
        align="center"
      ></b-pagination>
      <p class="mt-3">Current Page: {{ currentPage }}</p>
    </div>
  </div>


</template>

<script>
  export default {
    name: "Search",

    data() {
      return {
        perPage: 5,
        currentPage: 1,
        items: [
          {코드: 40, 지역명: 'Dickerson'},
          {코드: 21, 지역명: 'Larsen'},
          {코드: 89, 지역명: 'Geneva'},
          {코드: 38, 지역명: 'Jami'},
          {코드: 40, 지역명: 'Dickerson'},
          {코드: 21, 지역명: 'Larsen'},
          {코드: 89, 지역명: 'Geneva'},
          {코드: 38, 지역명: 'Jami'},
          {코드: 40, 지역명: 'Dickerson'},
          {코드: 21, 지역명: 'Larsen'},
          {코드: 89, 지역명: 'Geneva'},
          {코드: 38, 지역명: 'Jami'}
        ]
      }
    },
    computed: {
      rows() {
        return this.items.length
      }
    }
  }
</script>

<style scoped>
  table {
    /*width: 100%;*/
    /*margin: auto;*/
    text-align: center !important;
    /*vertical-align: middle !important;*/
    /*width: 100%;*/
  }
</style>
