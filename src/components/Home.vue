// src/components/Home.vue

<template>

  <div class="content">

      <!-- Start Page Loading -->
      <div class="loading"><img src="static/img/loading.gif" alt="loading-img"></div>
      <!-- End Page Loading -->
    <!-- Start Page Header -->
    <div class="page-header">
      <h1 class="title">welcome!</h1>
        <ol class="breadcrumb">
          <li>这是一个基于stellar之上的钱包服务，可以通过stellar地址进行快速的转账、支付、发行资产等。将持续提供更好的用户体验和更强大的功能！</li>
          <!-- <li class="active">This is a stellar wallet!You can follow it on <a href="https://github.com/blocklol">@github.com/block.lol</a></li> -->
        </ol>

      <!-- Start Page Header Right Div -->
      <div class="right">

      </div>
      <!-- End Page Header Right Div -->

    </div>
    <!-- End Page Header -->


   <!-- //////////////////////////////////////////////////////////////////////////// -->
  <!-- START CONTAINER -->
  <!-- <div class="container-widget"> -->




    <!-- Start First Row -->
    <div class="row">
      <!-- Start Top balance -->
      <keep-alive>
      <balance></balance>
      <!-- End Top balance -->
      </keep-alive>

      <!-- Start Transfer -->
      <transfer></transfer>
      <!-- End Transfer -->
      <receive></receive>
      <!-- Start history -->
      <history></history>
      <!-- End history -->

    </div>
    <!-- End First Row -->


    <!-- Start Second Row -->
    <div class="row">


    </div>
    <!-- End Second Row -->
    <!-- Start Third Row -->
    <!-- <div class="row">


      <div class="col-md-12 col-lg-6">
        <div class="panel panel-widget" style="height:205px;">
          <div class="panel-title">
            General Stats
          </div>
          <div class="panel-body">

            <div class="easypie margin-b-50" data-percent="82"><span>82%</span>New Visit</div>
            <div class="easypie margin-b-50" data-percent="30"><span>30%</span>Order</div>
            <div class="easypie margin-b-50 margin-b-40" data-percent="62"><span>62%</span>Page View</div>
            <div class="easypie margin-b-50" data-percent="15"><span>15%</span>Client</div>
            <div class="easypie margin-b-50" data-percent="45"><span>45%</span>Storage</div>
            <div class="easypie margin-b-50" data-percent="75"><span>76%</span>Comments</div>

          </div>
        </div>
      </div>
      <div class="col-md-6 col-lg-3">
        <div class="widget socialbox" style="background:#02A8F3; height:205px;">

          <p class="text">
            Never in all their history have men been able truly...
          </p>
          <p class="text-info">22 May, 2015 via mobile</p>

          <div class="logo"><i class="fa fa-twitter"></i></div>

          <ul class="info">
            <li><i class="fa fa-retweet"></i>694</li>
            <li><i class="fa fa-star-o"></i>2.192</li>
          </ul>

        </div>
      </div>

      <div class="col-md-6 col-lg-3">
        <div class="widget socialbox" style="background:#47639E; height:205px;">

          <p class="text">
            Science has not yet mastered prophecy.
          </p>
          <p class="text-info">22 May, 2015 via mobile</p>

          <div class="logo"><i class="fa fa-facebook"></i></div>

          <ul class="info">
            <li><i class="fa fa-thumbs-up"></i>694</li>
            <li><i class="fa fa-comment"></i>2.192</li>
          </ul>

        </div>
      </div>

    </div> -->
    <!-- End Third Row -->

  <!-- </div> -->
  <!-- END CONTAINER -->
   <!-- //////////////////////////////////////////////////////////////////////////// -->

  <!-- Start Footer -->
  <div class="row footer">
    <div class="col-md-6 text-left">
    Copyright © 2017 <a href="#" target="_blank"></a> All rights reserved.
    </div>
    <div class="col-md-6 text-right">
      <!-- Design and Developed by <a href="#" target="_blank">@block.lol</a> -->
    </div>
  </div>
  <!-- End Footer -->

<!-- <pre>{{$data|json}}</pre> -->

  </div>
</template>

<script>

import balance from './balance'
import history from './history'
import transfer from './transfer'
import receive from './receive'

export default{
  data(){
      return{
      }
  },
  components:{
    'balance':balance,
    'history':history,
    'transfer':transfer,
    'receive':receive,
  },
  mounted(){
    if(!sessionStorage.Keypair){
      var vm = this;
      vm.$router.push('/');
    }
  },
  methods:{

  }
};


</script>
