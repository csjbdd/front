<template>
  <div class="content">
    <div class="container-fluid">
        <div class="extended-forms">
            <div class="card">
                <!---->
                <!---->
                <div class="card-body">
                    <div class="col-12">
                        <div class="row">
                            <div class="col-lg-4">
                                <h4 class="title">Datetime Picker</h4>
                                <div class="form-group">
                                    <!---->
                                    <!---->
                                    <div
                                        class="el-date-editor el-range-editor el-input__inner el-date-editor--datetimerange">
                                        <i class="el-input__icon el-range__icon el-icon-time"></i>
                                        <input autocomplete="off" name="" class="el-range-input">
                                            <span class="el-range-separator">-</span>
                                            <input autocomplete="off" name="" class="el-range-input">
                                                <i class="el-input__icon el-range__close-icon"></i>
                                            </div>
                                            <!---->
                                            <!---->
                                        </div>
                                    </div>
                                    <div class="col-lg-4">
                                        <h4 class="title">Date Picker</h4>
                                        <div class="form-group">
                                            <!---->
                                            <!---->
                                            <div
                                                class="el-date-editor el-input el-input--prefix el-input--suffix el-date-editor--date">
                                                <!---->
                                                    <datepicker :language="ko" :format="customFormatter"></datepicker>
                                                    <span class="el-input__prefix">
                                                        <i class="el-input__icon el-icon-date"></i>
                                                        <!---->
                                                    </span>
                                                    <span class="el-input__suffix">
                                                        <span class="el-input__suffix-inner">
                                                            <i class="el-input__icon"></i>
                                                            <!---->
                                                            <!---->
                                                            <!---->
                                                            <!---->
                                                        </span>
                                                        <!---->
                                                    </span>
                                                    <!---->
                                                    <!---->
                                                </div>
                                                <!---->
                                                <!---->
                                            </div>
                                        </div>
                                        <div class="col-lg-4">
                                            <h4 class="title">Time Picker</h4>
                                            <div class="form-group">
                                                <!---->
                                                <!---->
                                                <div
                                                    class="el-date-editor el-input el-input--prefix el-input--suffix el-date-editor--time-select">
                                                    <!---->
                                                    <input
                                                        type="text"
                                                        autocomplete="off"
                                                        name=""
                                                        placeholder="Time picker here"
                                                        class="el-input__inner">
                                                        <span class="el-input__prefix">
                                                            <i class="el-input__icon el-icon-time"></i>
                                                            <!---->
                                                        </span>
                                                        <span class="el-input__suffix">
                                                            <span class="el-input__suffix-inner">
                                                                <i class="el-input__icon"></i>
                                                                <!---->
                                                                <!---->
                                                                <!---->
                                                                <!---->
                                                            </span>
                                                            <!---->
                                                        </span>
                                                        <!---->
                                                        <!---->
                                                    </div>
                                                    <!---->
                                                    <!---->
                                                </div>
                                            </div>
                                        </div>
                                        <div class="row">
                                            <div class="col-md-6">
                                                <h4 class="title">Switches</h4>
                                                <div class="row">
                                                    <div class="col-md-4">
                                                        <p class="category">Default</p>
                                                        <div
                                                            class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-on"
                                                            type="primary">
                                                            <div class="bootstrap-switch-container">
                                                                <span class="bootstrap-switch-handle-on  bootstrap-switch-">
                                                                    ON
                                                                </span>
                                                                <span class="bootstrap-switch-label"></span>
                                                                <span class="bootstrap-switch-handle-off bootstrap-switch-default">
                                                                    OFF
                                                                </span>
                                                            </div>
                                                        </div>
                                                        <div
                                                            class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-off"
                                                            type="primary">
                                                            <div class="bootstrap-switch-container">
                                                                <span class="bootstrap-switch-handle-on  bootstrap-switch-">
                                                                    ON
                                                                </span>
                                                                <span class="bootstrap-switch-label"></span>
                                                                <span class="bootstrap-switch-handle-off bootstrap-switch-default">
                                                                    OFF
                                                                </span>
                                                            </div>
                                                        </div>
                                                    </div>
                                                    <div class="col-md-4">
                                                        <p class="category">Plain</p>
                                                        <div
                                                            class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-on">
                                                            <div class="bootstrap-switch-container">
                                                                <span class="bootstrap-switch-handle-on  bootstrap-switch-"></span>
                                                                <span class="bootstrap-switch-label"></span>
                                                                <span class="bootstrap-switch-handle-off bootstrap-switch-default"></span>
                                                            </div>
                                                        </div>
                                                        <div
                                                            class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-off">
                                                            <div class="bootstrap-switch-container">
                                                                <span class="bootstrap-switch-handle-on  bootstrap-switch-"></span>
                                                                <span class="bootstrap-switch-label"></span>
                                                                <span class="bootstrap-switch-handle-off bootstrap-switch-default"></span>
                                                            </div>
                                                        </div>
                                                    </div>
                                                    <div class="col-md-4">
                                                        <p class="category">With Icons</p>
                                                        <div
                                                            class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-on">
                                                            <div class="bootstrap-switch-container">
                                                                <span class="bootstrap-switch-handle-on  bootstrap-switch-">
                                                                    <i class="fa fa-check"></i>
                                                                </span>
                                                                <span class="bootstrap-switch-label"></span>
                                                                <span class="bootstrap-switch-handle-off bootstrap-switch-default">
                                                                    <i class="fa fa-times"></i>
                                                                </span>
                                                            </div>
                                                        </div>
                                                        <div
                                                            class="bootstrap-switch bootstrap-switch-wrapper bootstrap-switch-animate bootstrap-switch-off">
                                                            <div class="bootstrap-switch-container">
                                                                <span class="bootstrap-switch-handle-on  bootstrap-switch-">
                                                                    <i class="fa fa-check"></i>
                                                                </span>
                                                                <span class="bootstrap-switch-label"></span>
                                                                <span class="bootstrap-switch-handle-off bootstrap-switch-default">
                                                                    <i class="fa fa-times"></i>
                                                                </span>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="row">
                                            <div class="col-md-6">
                                                <h4 class="title">Tags</h4>
                                                <span class="el-tag el-tag--warning el-tag--small el-tag--light">
                                                    Tag 1
                                                    <i class="el-tag__close el-icon-close"></i>
                                                </span>
                                                <span class="el-tag el-tag--warning el-tag--small el-tag--light">
                                                    Tag 2
                                                    <i class="el-tag__close el-icon-close"></i>
                                                </span>
                                                <span class="el-tag el-tag--warning el-tag--small el-tag--light">
                                                    Tag 3
                                                    <i class="el-tag__close el-icon-close"></i>
                                                </span>
                                                <input
                                                    type="text"
                                                    placeholder="New Tag"
                                                    size="mini"
                                                    class="form-control input-new-tag"></div>
                                                <div class="col-md-6">
                                                    <h4 class="title">Customisable Select</h4>
                                                    <div class="row">
                                                        <div class="col-md-6">
                                                            <div class="el-select select-danger el-select--large">
                                                                <!---->
                                                                <div class="el-input el-input--large el-input--suffix">
                                                                    <!---->
                                                                    <input
                                                                        type="text"
                                                                        readonly="readonly"
                                                                        autocomplete="off"
                                                                        placeholder="Single Select"
                                                                        class="el-input__inner">
                                                                        <!---->
                                                                        <span class="el-input__suffix">
                                                                            <span class="el-input__suffix-inner">
                                                                                <i class="el-select__caret el-input__icon el-icon-arrow-up"></i>
                                                                                <!---->
                                                                                <!---->
                                                                                <!---->
                                                                                <!---->
                                                                                <!---->
                                                                            </span>
                                                                            <!---->
                                                                        </span>
                                                                        <!---->
                                                                        <!---->
                                                                    </div>
                                                                    <div
                                                                        class="el-select-dropdown el-popper"
                                                                        style="display: none; min-width: 216.25px;">
                                                                        <div class="el-scrollbar" style="">
                                                                            <div
                                                                                class="el-select-dropdown__wrap el-scrollbar__wrap"
                                                                                style="margin-bottom: -17px; margin-right: -17px;">
                                                                                <ul class="el-scrollbar__view el-select-dropdown__list">
                                                                                    <!---->
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Bahasa Indonesia</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Bahasa Melayu</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Català</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Dansk</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Deutsch</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>English</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Español</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Eλληνικά</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Français</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Italiano</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Magyar</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Nederlands</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Norsk</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Polski</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Português</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Suomi</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Svenska</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Türkçe</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Íslenska</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Čeština</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>Русский</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>ภาษาไทย</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>中文 (简体)</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>W"&gt;中文 (繁體)</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>日本語</span>
                                                                                    </li>
                                                                                    <li class="el-select-dropdown__item select-danger">
                                                                                        <span>한국어</span>
                                                                                    </li>
                                                                                </ul>
                                                                            </div>
                                                                            <div class="el-scrollbar__bar is-horizontal">
                                                                                <div class="el-scrollbar__thumb" style="transform: translateX(0%);"></div>
                                                                            </div>
                                                                            <div class="el-scrollbar__bar is-vertical">
                                                                                <div class="el-scrollbar__thumb" style="transform: translateY(0%);"></div>
                                                                            </div>
                                                                        </div>
                                                                        <!---->
                                                                    </div>
                                                                </div>
                                                            </div>
                                                            <div class="col-md-6">
                                                                <div class="el-select select-primary el-select--large">
                                                                    <div class="el-select__tags" style="width: 100%; max-width: 184.25px;">
                                                                        <!---->
                                                                        <span></span>
                                                                        <!---->
                                                                    </div>
                                                                    <div class="el-input el-input--large el-input--suffix">
                                                                        <!---->
                                                                        <input
                                                                            type="text"
                                                                            readonly="readonly"
                                                                            autocomplete="off"
                                                                            placeholder="Multiple Select"
                                                                            class="el-input__inner"
                                                                            style="height: 40px;">
                                                                            <!---->
                                                                            <span class="el-input__suffix">
                                                                                <span class="el-input__suffix-inner">
                                                                                    <i class="el-select__caret el-input__icon el-icon-arrow-up"></i>
                                                                                    <!---->
                                                                                    <!---->
                                                                                    <!---->
                                                                                    <!---->
                                                                                    <!---->
                                                                                </span>
                                                                                <!---->
                                                                            </span>
                                                                            <!---->
                                                                            <!---->
                                                                        </div>
                                                                        <div
                                                                            class="el-select-dropdown el-popper is-multiple"
                                                                            style="display: none; min-width: 216.25px;">
                                                                            <div class="el-scrollbar" style="">
                                                                                <div
                                                                                    class="el-select-dropdown__wrap el-scrollbar__wrap"
                                                                                    style="margin-bottom: -17px; margin-right: -17px;">
                                                                                    <ul class="el-scrollbar__view el-select-dropdown__list">
                                                                                        <!---->
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Bahasa Indonesia</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Bahasa Melayu</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Català</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Dansk</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Deutsch</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>English</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Español</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Eλληνικά</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Français</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Italiano</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Magyar</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Nederlands</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Norsk</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Polski</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Português</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Suomi</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Svenska</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Türkçe</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Íslenska</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Čeština</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>Русский</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>ภาษาไทย</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>中文 (简体)</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>W"&gt;中文 (繁體)</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>日本語</span>
                                                                                        </li>
                                                                                        <li class="el-select-dropdown__item select-primary">
                                                                                            <span>한국어</span>
                                                                                        </li>
                                                                                    </ul>
                                                                                </div>
                                                                                <div class="el-scrollbar__bar is-horizontal">
                                                                                    <div class="el-scrollbar__thumb" style="transform: translateX(0%);"></div>
                                                                                </div>
                                                                                <div class="el-scrollbar__bar is-vertical">
                                                                                    <div class="el-scrollbar__thumb" style="transform: translateY(0%);"></div>
                                                                                </div>
                                                                            </div>
                                                                            <!---->
                                                                        </div>
                                                                    </div>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                    <div class="row">
                                                        <div class="col-md-6">
                                                            <h4 class="title">Progress Bars</h4>
                                                            <div class="progress" style="height: 4px;">
                                                                <div
                                                                    role="progressbar"
                                                                    aria-valuenow="30"
                                                                    aria-valuemin="0"
                                                                    aria-valuemax="100"
                                                                    class="progress-bar bg-default"
                                                                    style="width: 30%;">
                                                                    <!---->
                                                                </div>
                                                            </div>
                                                            <div class="progress" style="height: 4px;">
                                                                <div
                                                                    role="progressbar"
                                                                    aria-valuenow="60"
                                                                    aria-valuemin="0"
                                                                    aria-valuemax="100"
                                                                    class="progress-bar bg-info"
                                                                    style="width: 60%;">
                                                                    <!---->
                                                                </div>
                                                            </div>
                                                            <div class="progress" style="height: 4px;">
                                                                <div class="progress-bar bg-success" style="width: 35%;">
                                                                    <!---->
                                                                </div>
                                                                <div class="progress-bar bg-warning" style="width: 20%;">
                                                                    <!---->
                                                                </div>
                                                                <div class="progress-bar bg-danger" style="width: 10%;">
                                                                    <!---->
                                                                </div>
                                                            </div>
                                                        </div>
                                                        <div class="col-md-6">
                                                            <h4 class="title">Sliders</h4>
                                                            <div
                                                                role="slider"
                                                                aria-valuemin="0"
                                                                aria-valuemax="100"
                                                                aria-orientation="horizontal"
                                                                class="el-slider slider-success"
                                                                aria-valuetext="30"
                                                                aria-label="slider between 0 and 100">
                                                                <!---->
                                                                <div class="el-slider__runway">
                                                                    <div class="el-slider__bar" style="width: 30%; left: 0%;"></div>
                                                                    <div tabindex="0" class="el-slider__button-wrapper" style="left: 30%;">
                                                                        <div
                                                                            class="el-tooltip el-slider__button"
                                                                            aria-describedby="el-tooltip-5928"
                                                                            tabindex="0"></div>
                                                                    </div>
                                                                    <!---->
                                                                    <!---->
                                                                </div>
                                                            </div>
                                                            <br>
                                                                <div
                                                                    role="slider"
                                                                    aria-valuemin="0"
                                                                    aria-valuemax="100"
                                                                    aria-orientation="horizontal"
                                                                    class="el-slider slider-info"
                                                                    aria-valuetext="20-50"
                                                                    aria-label="slider between 0 and 100">
                                                                    <!---->
                                                                    <div class="el-slider__runway">
                                                                        <div class="el-slider__bar" style="width: 30%; left: 20%;"></div>
                                                                        <div tabindex="0" class="el-slider__button-wrapper" style="left: 20%;">
                                                                            <div
                                                                                class="el-tooltip el-slider__button"
                                                                                aria-describedby="el-tooltip-6427"
                                                                                tabindex="0"></div>
                                                                        </div>
                                                                        <div tabindex="0" class="el-slider__button-wrapper" style="left: 50%;">
                                                                            <div
                                                                                class="el-tooltip el-slider__button"
                                                                                aria-describedby="el-tooltip-3045"
                                                                                tabindex="0"></div>
                                                                        </div>
                                                                        <!---->
                                                                    </div>
                                                                </div>
                                                            </div>
                                                        </div>
                                                    </div>
                                                </div>
                                                <!---->
                                            </div>
                                        </div>
                                    </div>
                                </div>
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
        type: ['', 'info', 'success', 'warning', 'danger'],
        notifications: {
          topCenter: false
        },
        ko : ko
      }
    },
    methods: {
      notifyVue (verticalAlign, horizontalAlign) {
        const color = Math.floor((Math.random() * 4) + 1)
        this.$notifications.notify(
          {
            message: `<span>Welcome to <b>Light Bootstrap Dashboard</b> - a beautiful freebie for every web developer.</span>`,
            icon: 'nc-icon nc-app',
            horizontalAlign: horizontalAlign,
            verticalAlign: verticalAlign,
            type: this.type[color]
          })
      },
      customFormatter(date) {
        return date.getFullYear()+'-'+date.getMonth()+'-'+date.getDate()
      }
    }
  }

</script>
<style lang="scss">

</style>
