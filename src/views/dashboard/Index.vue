<style>
    .dashboar .side-2 {
        display: grid;
        grid-template-columns: 25% auto;
        gap: 30px;
    }
    @media (min-width: 270px) and (max-width: 767px)
        {
        .dashboar.container-fluid.mb-5.mt-4 {
            padding-top: 4rem;
        }
        .dashboar .side-2 {
            display: flex;
            grid-template-columns: 25% auto;
            gap: 10px;
        }
        ul.profile-menu.list-group {
            display: flex;
            justify-content: space-between;
        }
        
        .mt-4 .row .col-md-3-dashboar {
            flex: 0 0 100%;
            max-width: 100%;
        }
        .fas {
            -moz-osx-font-smoothing: grayscale;
            -webkit-font-smoothing: antialiased;
            display: flex;
            font-style: normal;
            font-variant: normal;
            text-rendering: auto;
            line-height: 1;
            justify-content: center;
        }
        .list-group-item {
            padding: 15px;
            font-size: 0.7rem;
        }
        .mt-4 .row .col-md-9-dashboar {
            flex: 0 0 100%;
            max-width: 100%;
        }
    }
</style>
<template>
    <div class="dashboar container-fluid mb-5 mt-4">
        <div class="side-2 row">
            <div class="col-md-3-dashboar mb-4">
                <CustomerMenu />
            </div>
            <div class="col-md-9-dashboar mb-4">
                <div class="card border-0 rounded shadow">
                    <div class="card-body">
                        <h5 class="font-weight-bold"> <i class="fas fa-tachometer-alt"></i> DASHBOARD</h5>
                        <hr>
                        Selamat Datang <strong>{{ user.name }}</strong>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    //import customer menu component
    import CustomerMenu from '@/components/CustomerMenu'
    import { computed, onMounted } from 'vue'
    import { useStore } from 'vuex'

    export default {

        components: {
            //customer menu component
            CustomerMenu
        },

        setup() {
            
            //store vuex
            const store = useStore()

            //mounted
            onMounted(() => {

                //panggil action "getUser" dari module "auth" vuex
                store.dispatch('auth/getUser')

            })

            const user = computed(() => {
                return store.getters['auth/currentUser']
            })

            //return a state and function
            return {
                store,
                user
            }

        }

    }
</script>
