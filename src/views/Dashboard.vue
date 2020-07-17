<template>
     <div id="wrapper" v-bind:class="toggle">
        <!-- Sidebar -->
        <Sidebar/>
        <!-- /#sidebar-wrapper -->

        <!-- Page Content -->
        <div id="page-content-wrapper">
            <!-- /#page-topbar -->
            <Topbar @toggle="toggleMenu()"/>
            <!-- /#page-topbar -->
            <div class="container-fluid dashboard">
                <div class="row">
                    <div class="col-lg-3 col-sm-6">
                        <div class="card">
                            <div class="card-body">
                                <div class="media align-items-center">
                                    <div class="media-body">
                                        <h4>20</h4><span>Lorem</span>
                                    </div>
                                    <div class="text-center">
                                       <i class="icofont-user-suited"></i>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6">
                        <div class="card">
                            <div class="card-body">
                                <div class="media align-items-center">
                                    <div class="media-body">
                                        <h4>20</h4><span>Lorem</span>
                                    </div>
                                    <div class="text-center">
                                        <i class="icofont-worker"></i>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6">
                        <div class="card">
                            <div class="card-body">
                                <div class="media align-items-center">
                                    <div class="media-body">
                                        <h4>20</h4><span>Lorem</span>
                                    </div>
                                    <div class="text-center">
                                        <i class="icofont-users-alt-2"></i>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-3 col-sm-6">
                        <div class="card">
                            <div class="card-body">
                                <div class="media align-items-center">
                                    <div class="media-body">
                                        <h4>20</h4><span>Lorem</span>
                                    </div>
                                    <div class="text-center">
                                         <i class="icofont-worker"></i>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="col-12">
                        <div class="card">
                            <div class="card-header">
                                <div class="header-top">
                                    <h5 class="m-0">Lorem ipsum</h5>
                                </div>
                            </div>
                            <div class="card-body">
                                <div class="table-responsive">
                                    <table class="table">
                                        <thead class="thead-light">
                                            <tr>
                                                <th>Lorem ipsum</th>
                                                <th>Lorem ipsum</th>
                                                <th>Lorem ipsum</th>
                                                <th>Lorem ipsum</th>
                                                <th>Lorem ipsum</th>
                                            </tr>
                                        </thead>
                                        <tbody>
                                            <tr>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum@Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>
                                                    <div class="btn-group" role="group">
                                                        <button type="button" title="Visualizar"><i class="icofont-eye-alt"></i></button>
                                                        <button type="button" title="Editar"><i class="icofont-pencil-alt-2"></i></button>
                                                        <button type="button" title="Excluir"><i class="icofont-trash"></i></button>
                                                    </div>
                                                </td>
                                            </tr>
                                            <tr>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum@Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>
                                                    <div class="btn-group" role="group">
                                                        <button type="button" title="Visualizar"><i class="icofont-eye-alt"></i></button>
                                                        <button type="button" title="Editar"><i class="icofont-pencil-alt-2"></i></button>
                                                        <button type="button" title="Excluir"><i class="icofont-trash"></i></button>
                                                    </div>
                                                </td>
                                            </tr>
                                            <tr>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum@Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>
                                                    <div class="btn-group" role="group">
                                                        <button type="button" title="Visualizar"><i class="icofont-eye-alt"></i></button>
                                                        <button type="button" title="Editar"><i class="icofont-pencil-alt-2"></i></button>
                                                        <button type="button" title="Excluir"><i class="icofont-trash"></i></button>
                                                    </div>
                                                </td>
                                            </tr>
                                            <tr>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>Lorem ipsum@Lorem ipsum</td>
                                                <td>Lorem ipsum</td>
                                                <td>
                                                    <div class="btn-group" role="group">
                                                        <button type="button" title="Visualizar"><i class="icofont-eye-alt"></i></button>
                                                        <button type="button" title="Editar"><i class="icofont-pencil-alt-2"></i></button>
                                                        <button type="button" title="Excluir"><i class="icofont-trash"></i></button>
                                                    </div>
                                                </td>
                                            </tr>
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <!-- /#page-footer -->
            <Footer/>
            <!-- /#page-footer -->
        </div>
        <!-- /#page-content-wrapper -->

     </div>
</template>

<script>
import Sidebar from '../components/Sidebar';
import Topbar from '../components/Topbar';
import Footer from '../components/Footer';

export default {
  name: 'Home',
  components: {
    Sidebar, Topbar, Footer
  },
  data(){
    return{
      toggle: '',
      toggleBool: false
    }
  },
  methods:{
      toggleMenu(){
          this.toggleBool = !this.toggleBool;
          if(this.toggleBool == true){
            this.toggle = 'toggled'
          }else{
            this.toggle = ''
          }
      }
  }
}
</script>

<style>
.table td {
    padding: 0.75rem;
    vertical-align: top;
    border-top: 1px solid #dee2e6;
    vertical-align: middle;
    text-align: center;
}

.table .btn-group button{
        border: none;
    padding: 10px;
    width: 40px;
    height: 40px;
    margin: 0 5px;
}

.table .btn-group button i{
    font-size: 18px;
}

.table .thead-light th {
    color: #495057;
    background-color: #e9ecef;
    border-color: #dee2e6;
    text-align: center;
}

.table tbody tr{
    border-bottom: 1px solid #f6f6f6;
}

.table tbody tr td .btn-group button i{
    font-size: 18px !important;
}
</style>
