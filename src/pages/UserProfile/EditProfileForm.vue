<template>
  <card>
    <h4 slot="header" class="card-title">프로필</h4>
    <form>
      <div class="row">
        <div class="col-md-5">
          <base-input type="text"
                    label="회사명"
                    :disabled="true"
                    placeholder="Light dashboard"
                    v-model="user.company">
          </base-input>
        </div>
        <div class="col-md-3">
          <base-input type="text"
                    label="이름"
                    placeholder="Username"
                    v-model="user.username">
          </base-input>
        </div>
        <div class="col-md-4">
          <base-input type="email"
                    label="이메일"
                    placeholder="Email"
                    v-model="user.email">
          </base-input>
        </div>
      </div>

      <div class="row">
        <div class="col-md-6">
          <base-input type="text"
                    label="생년월일"
                    placeholder="First Name"
                    v-model="user.firstName">
          </base-input>
        </div>
        <div class="col-md-6">
          <base-input type="text"
                    label="연락처"
                    placeholder="Last Name"
                    v-model="user.lastName">
          </base-input>
        </div>
      </div>

      <div class="row">
        <div class="col-md-12">
          <base-input type="text"
                    label="주소"
                    placeholder="Home Address"
                    v-model="user.address">
          </base-input>
        </div>
      </div>

      <div class="row">
        <div class="col-md-4">
          <base-input type="text"
                    label="성별"
                    placeholder="나이"
                    v-model="user.city">
          </base-input>
        </div>
        <div class="col-md-4">
          <base-input type="text"
                    label="입사날짜"
                    placeholder="Country"
                    v-model="user.country">

          </base-input>
        </div>
        <div class="col-md-4">
          <base-input type="number"
                    label="나이"
                    placeholder="ZIP Code"
                    v-model="user.postalCode">
          </base-input>
        </div>   
        <div class="col-md-4">
        </div>    
      </div>
      <div class="row">
        <div class="col-md-12">
          <div class="form-group">
            <label>자기소개</label>
            <textarea rows="5" class="form-control border-input"
                      placeholder="Here can be your description"
                      v-model="user.aboutMe">
              </textarea>
          </div>
        </div>
      </div>
      <div class="text-center">
        <button type="submit" class="btn btn-info btn-fill float-right" @click.prevent="updateProfile">
          저장
        </button>
      </div>
      <div class="clearfix"></div>
    </form>
  </card>
</template>
<script>
  import Card from 'src/components/Cards/Card.vue'
  import Datepicker from 'vuejs-datepicker'
  import {ko} from 'vuejs-datepicker/dist/locale'

  export default {
    components: {
      Card,
      Datepicker
    },
    data () {
      return {
        user: {},
        ko : ko
      }
    },
    methods: {
      updateProfile () {
        alert('Your data: ' + JSON.stringify(this.user))
      },
      customFormatter(date) {
        return date.getFullYear()+'-'+date.getMonth()+'-'+date.getDate()
      }
    },
    created() {
      this.$axios.get('http://localhost:8081/profile/user').then(response => {
        this.user = response.data;
      }).catch(error => {
        console.log(error)
      })
    },
  }

</script>
<style>

</style>
