<template>
    <section id="app">
        <div class="area">
            <div class="container">
                <div class="body_area">
                    <div class="row">
                        <div class="col-md-12">
                            <div class="float-left-side">
                                <font-awesome-icon icon="print" />
                            </div>
                            <div class="float-right-side">
                                <h5>{{printer}}</h5>
                                <p>{{ip}}</p>
                            </div>
                        </div>
                    </div>
                    <div class="row m-t-16" >
                        <div class="col-md-4">
                            <div class="icons">
                                <button type="button" class="btn  btn-primary btn_icon customBtn">{{badge[0]}}</button>
                                <button type="button" class="btn  btn-success btn_icon customBtn">{{badge[1]}}</button>
                                <button type="button" class="btn  btn-danger btn_icon customBtn">{{badge[2]}}</button>
                            </div>
                        </div>
                        <div class="col-md-2">
                        </div>
                        <div class="col-md-6">
                            <p class="printing-percentage">Printing 64%</p>
                            <div class="progress" >
                                <div class="progress-bar" role="progressbar" style="width: 64%;" aria-valuenow="64" aria-valuemin="0" aria-valuemax="100">64%</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: "App",
        data: function() {
            return {
                printer: 'Canon IPF6400',
                ip: '172.16.254.1',
                badge:['147','89','2']
            };
        },
    };
</script>
<style>
    #app {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-evenly;
        width: 100%;
    }
    .area{
        margin-top: 10%;
        min-width:35%;
    }
    .body_area{
        padding: 5% 5%;
        box-shadow: 0 1px 8px 1px #adb5bd;
        border-radius: 10px;
    }
    .float-left-side{
        float: left;
        display: block;
        font-size: 35px;
        padding: 1px 10px;
        border: 1px solid #adb5bd2e;
        background: #adb5bd2e;
        margin-right: 20px;}
    .float-right-side{
        float: left;
    }
    .btn_icon{
        border-radius: 20px;
    }
    .icons{
        display: flex;
    }
    .customBtn {
        border-radius: 100px !important;
        padding: 1px 10px 1px 10px !important;
        font-size:15px !important;
        margin-right: 5px;
    }
    .progress {
        height: 8px !important;
        background: 'transparent';
        font-size: 0px !important;
    }
    .progress-bar {
        border-radius:100px;
    }
    .printing-percentage {
        font-size: 12px;
        margin-bottom: 1px;
    }
    .m-t-16 {
        margin-top: 16px;
    }
</style>
