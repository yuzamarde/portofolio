<template>
  <div class="container mt-5 mb-5">
        <div class="row">
            <div class="col-md-4">
                
                <div class="card border-0 rounded shadow">
                    <div class="card-body p-2">
                        <div>
                            <button @click="showSingle">Show single picture.</button>
                            <button @click="showMultiple">Show a group of pictures.</button>

                            <!-- all props & events -->
                            <vue-easy-lightbox
                            scrollDisabled
                            escDisabled
                            moveDisabled
                            :visible="visible"
                            :imgs="imgs"
                            :index="index"
                            @hide="handleHide"
                            ></vue-easy-lightbox>
                        </div>
                         <img :src="product.image" id="zoom_01" class="zoom">
                    </div>
                </div>
            </div>
            <div class="col-md-8">
                <div class="card border-0 rounded shadow">
                    <div class="card-body">
                        <label class="font-weight-bold" style="font-size: 20px;"> {{ product.title }} </label>
                        <hr>
                        <div class="price-product" id="price-product" style="font-size: 1.35rem"><span
                                class="font-weight-bold mr-4" style="color: green">Rp. {{ calculateDiscount(product) }}</span> 
                            <s class="font-weight-bold" style="text-decoration-color:red">Rp. {{ product.price }}</s>
                        </div>
                        <table class="table table-borderless mt-3">
                            <tbody>
                                <tr>
                                    <td class="font-weight-bold">DISKON</td>
                                    <td>:</td>
                                    <td>
                                        <button class="btn btn-sm" style="color: #ff2f00;border-color: #ff2f00;">
                                            DISKON {{ product.discount }} %
                                        </button>
                                    </td>
                                </tr>
                                <tr>
                                    <td class="font-weight-bold">BERAT</td>
                                    <td>:</td>
                                    <td>
                                        <span class="badge badge-pill badge-success"
                                            style="font-size: 14px;border-radius: .3rem;padding: .25em .5em .2em;"> {{ product.weight }}
                                            gram</span>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                        <button @click.prevent="addToCart(product.id, calculateDiscount(product), product.weight)" class="btn btn-primary btn-lg btn-block"><i class="fa fa-shopping-cart"></i> TAMBAH KE KERANJANG</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="row mt-5">
            <div class="col-md-12">
                <div class="card border-0 rounded shadow">
                    <div class="card-body">
                        <label class="font-weight-bold" style="font-size: 20px;">KETERANGAN</label>
                        <hr>
                        <div v-html="product.content"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { computed, onMounted } from 'vue'   // computed dan onMounted
import { useStore } from 'vuex' // store Vuex
import { useRoute, useRouter } from 'vue-router' // vue router
import VueEasyLightbox from 'vue-easy-lightbox'

    export default {
        components: {
        VueEasyLightbox
        },
        data() {
        return {
            imgs: '', // Img Url , string or Array of string
            visible: false,
            index: 0 // default: 0
        }
        },
        methods: {
        showSingle() {
            this.imgs = 'http://localhost:8000/storage/products/hPtBcfZdYExpXGugY3RhTXs7HbWEKVsf0EXmLVBY.jpeg'
            // or
            this.imgs = {
            title: 'this is a placeholder',
            src: 'http://localhost:8000/storage/products/hPtBcfZdYExpXGugY3RhTXs7HbWEKVsf0EXmLVBY.jpeg'
            }
            this.show()
        },
        showMultiple() {
            this.imgs = [
            'http://via.placeholder.com/350x150',
            'http://via.placeholder.com/350x150'
            ]
            // or
            this.imgs = [
            { title: 'test img', src: 'http://via.placeholder.com/350x150' },
            'http://via.placeholder.com/350x150'
            ]
            // allow mixing

            this.index = 1 // index of imgList
            this.show()
        },
        show() {
            this.visible = true
        },
        handleHide() {
            this.visible = false
        }
        },
        setup() {

            //vue route
            const route = useRoute()

            //vue router
            const router = useRouter()

             //store vuex
            const store = useStore()

            //onMounted akan menjalankan action "getDetailProduct" di module "product" Vuex
            onMounted(() => {
                store.dispatch('product/getDetailProduct', route.params.slug)
            })

            //computed properti digunakan untuk mendapatkan data detail product dari state "product" di module "product" Vuex
            const product = computed(() => {
                return store.state.product.product
            })

            /**
             * function addToCart
             */
            function addToCart(product_id, price, weight) {
                
                //check token terlebih dahulu
                const token = store.state.auth.token

                if(!token) {
                    return router.push({name: 'login'})
                }

                //panggil action addToCart di module cart
                store.dispatch('cart/addToCart', {
                    product_id: product_id,
                    price: price,
                    weight: weight,
                    quantity: 1
                }) 

            }

            return {
                route,
                router,
                store,
                product,
                addToCart
            }

        }

    }
</script>