<template>
        <div class="container mt-5 ">
             <div class="box-1 position-relative--own">
                  <div class="position-absolute--own box-2 ">
                        <div class="box-3 position-absolute--own">
                              <div class="box-4 position-absolute--own">
                                    <div class="box-5 position-absolute--own">
                                          <div class="box-6 position-absolute--own text-center">
                                                <h3 style="margin-top: 45%">Center Box</h3>
                                          </div>
                                    </div>
                              </div>
                        </div>
                  </div>
             </div>
        </div>
</template>

<script>
export default {
  name: "Nasted.vue"
}
</script>

<style scoped>
        .position-relative--own{
          position: relative;
        }
        .position-absolute--own{
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
        }

        .box-1{
          width: 800px;
          height: 800px;
          background-color: red;
        }
        .box-2{
          width: 700px;
          height: 700px;
          background-color: #c1bf51;
        }
        .box-3{
          width: 600px;
          height: 600px;
          background-color: #147ae7;
        }
        .box-4{
          width: 500px;
          height: 500px;
          background-color: #f3e708;
        }
        .box-5{
          width: 400px;
          height: 400px;
          background-color: #20dd4f;
        }
        .box-6{
          width: 300px;
          height: 300px;
          background-color: #12b3db;
        }

</style>
