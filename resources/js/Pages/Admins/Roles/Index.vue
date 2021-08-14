<template>
    <admin-layout>
        <section class="content">
            <div class="row">
                <div class="col-12">
                    <div class="card">
                        <div class="card-header">
                            <div class="card-title">
                                <h3>Roles & Permissions</h3> 
                                <div class="card-tools">
                                    <button type="button" class="btn btn-info text-uppercase" style="letter-spacing:0.13m;">
                                            Create
                                    </button>
                                </div>
                            </div>
                        </div>
                        <div class="card-body table-responsive p-0">
                            <table class="table table-hover text-nowrap">
                                <thead>
                                    <tr>
                                        <th class="text-capitalize">Role Name</th>
                                        <th class="text-capitalize">Permissions</th>
                                        <th class="text-capitalize">Creates</th>
                                        <th class="text-capitalize text-right">Actions</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr v-for="(role,index) in roles" :key="index">
                                        <td>{{role.name}}</td>
                                        <td>permisisons</td>
                                        <td>{{role.created_at}}</td>
                                        <td class="text-right">
                                            <button class="btn btn-success text-uppercase" style="letter-spacing: 0.1em;">
                                            Edit
                                            </button>
                                            <button class="btn btn-success text-uppercase ml-1" style="letter-spacing: 0.1em;">
                                            Delete
                                            </button>
                                        </td>

                                    </tr>
                                </tbody>
                            </table>
                        </div>
                        <div class="card-footer clearfix">
                            pagination links
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <div class="modal fade" id="modal-lg">
            <div class="modal-dialog modal-lg modal-dialog-centered">
                <div class="modal-header">
                    <h4 class="modal-title">title</h4>
                    <button type="button" class="close">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="modal-body overflow-hidden">
                    <div class="h4">
                        <span>Preview: <span class="text-capitalize">form name
                            </span>
                            </span>
                    </div>
                    <div class="card card-primary">
                        <form>
                            <div class="card-body">
                                <div class="form-group">
                                    
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </admin-layout>
</template>

<script>

import AdminLayout from '../../../../js/Layouts/AdminLayout.vue'


export default {
     props: ['roles'],
    components:{AdminLayout}
}
</script>