<template>
  <div class="content">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <card class="strpied-tabled-with-hover"
                body-classes="table-full-width table-responsive"
          >
            <template slot="header">
              <h3 class="card-title">연차사용 현황</h3>
            </template>
            <l-table class="table-hover table-striped"
                     :columns="table1.columns"
                     :data="table1.data">
            </l-table>
          </card>
          <div class="card strpied-tabled-with-hover">
    <span>
        <form class="form-horizontal">
                <div class="card-header">
                    <div>
                        <h3 class="card-title">
                            연차 신청
                        </h3>
                    </div>
                </div>
                <div class="card-body table-full-width table-responsive">
                  <div class="col-12">
                    <div class="row">
                    <div class="col-lg-12">
                    <h4 class="title">연차종류</h4>
                      <select class="custom-select">
                        <option value="1" selected>연차</option>
                        <option value="0.5">반차</option>
                        <option value="0.25">반반차</option>
                      </select>
</div>
                    </div>
                    <div class="row">
                      <div class="col-lg-4">
                        <h4 class="title">시작일자</h4>
                        <div class="form-group">
                            <div
                                class="el-date-editor el-input el-input--prefix el-input--suffix el-date-editor--date">
                                    <datepicker v-model="annual.startDate" :language="ko" :format="customFormatter" :typeable="true"input-class="form-control"></datepicker>
                                    <span class="el-input__prefix">
                                        <i class="el-input__icon el-icon-date"></i>
                                    </span>
                                    <span class="el-input__suffix">
                                        <span class="el-input__suffix-inner">
                                            <i class="el-input__icon"></i>
                                        </span>
                                    </span>
                                </div>
                            </div>
                        </div>
                        
                          <div class="col-lg-4">
                        <h4 class="title">종료일자</h4>
                        <div class="form-group">
                            <div
                                class="el-date-editor el-input el-input--prefix el-input--suffix el-date-editor--date">
                                    <datepicker v-model="annual.endDate" :language="ko" :format="customFormatter" :typeable="true"input-class="form-control" @selected=dateSelected></datepicker>
                                    <span class="el-input__prefix">
                                        <i class="el-input__icon el-icon-date"></i>
                                    </span>
                                    <span class="el-input__suffix">
                                        <span class="el-input__suffix-inner">
                                            <i class="el-input__icon"></i>
                                        </span>
                                    </span>
                                </div>
                            </div>
                        </div>
                          <div class="col-lg-4">
                        <h4 class="title">총일수</h4>
                        <div class="form-group">
                            <div
                                class="el-date-editor el-input el-input--prefix el-input--suffix el-date-editor--date">
                                    <input
                                                    type="text"
                                                    size="mini"
                                                    class="form-control input-new-tag" disabled>
                                    <span class="el-input__prefix">
                                        <i class="el-input__icon el-icon-date"></i>
                                    </span>
                                    <span class="el-input__suffix">
                                        <span class="el-input__suffix-inner">
                                            <i class="el-input__icon"></i>
                                        </span>
                                    </span>
                                </div>
                            </div>
                        </div>
                      </div>
                  </div>
                  <div class="text-center">
                      <button type="submit" class="btn btn-fill btn-info btn-wd">신청하기</button>
                  </div>
                </div>
        </form>
    </span>
  </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  import LTable from 'src/components/Table.vue'
  import Card from 'src/components/Cards/Card.vue'
  import Datepicker from 'vuejs-datepicker'
  import {ko} from 'vuejs-datepicker/dist/locale'
  import Alert from 'src/components/Modals/Alert.vue'
  
  
  const tableColumns = ['전체일수', '연차', '반차', '반반차', '남은일수']
  const tableData = [{
    전체일수: 13,
    연차: '12',
    반차: '0',
    반반차: '0',
    남은일수: '1'
  }]
  export default {
    components: {
      LTable,
      Card,
      Datepicker,
      Alert
    },
    data () {
      return {
        table1: {
          columns: [...tableColumns],
          data: [...tableData]
        },
        ko : ko,
        annual: {
          startDate:'',
          endDate:''
        },
        modal: false,
        message: ''

      }
    },
    methods: {
      customFormatter(date) {
        return this.$moment(date).format("YYYY-MM-DD");
      },
      dateSelected() {
        this.$nextTick(() => {
          alert('hi')
        })
      },
      openModal() {
      this.modal = true
    },
    closeModal() {
      this.modal = false
    },
    doSend() {
      if (this.message.length > 0) {
        alert(this.message)
        this.message = ''
        this.closeModal()
      } else {
        alert('메시지를 입력해주세요.')
      }
    }
    }
  }
</script>
<style>
</style>
