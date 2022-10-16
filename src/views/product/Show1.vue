
<style>
    .data-slide-image {
            display: flex;
        }
    .col-md-4 .col-product {
        padding: 0px;
    }
    .col-product li{
        border: 0px solid transparent;
        cursor: pointer;
        float: left;
        height: auto;
        margin: 10px 0 10px 0;
        padding: 0px;
        text-align: center;
        text-indent: unset;
        width: fit-content;
        opacity: 1;
        transition: none;
    }
    .carousel-indicators {
        position: absolute;
        right: 0;
        bottom: 0;
        left: 0;
        z-index: 15;
        display: -ms-flexbox;
        display: flex;
        -ms-flex-pack: center;
        justify-content: flex-end;
        padding-left: 0;
        margin-right: 15%;
        margin-left: 15%;
        list-style: none;
        flex-wrap: inherit;
        gap: 7px;
    }
    .Easylightbox button {
        position: absolute;
        height: -webkit-fill-available;
        width: -webkit-fill-available;
        opacity: 0;
    }
/*     
    #amin {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 600px;
    max-width: 100%;
    margin: 50px auto;
    position: relative;
    }
    .image {
    width: 400px;
    max-width: 100%;
    } */
</style>


<template>
    
  <div class="dashboar container mt-5 mb-5">
        <div class="product row">
            <div id="productslider" class="carousel col-md-4">
                <div class="carousel-inner">
                    
                    <div class="carousel-item active zoom-image" >
                        <div class=Easylightbox>
                            <button @click="showSingle">Show single picture.</button>
                            <!-- all props & events -->
                            <vue-easy-lightbox
                                :visible="visible"
                                :imgs="product.image"
                                :index="index"
                                @hide="handleHide"
                                >        
                            </vue-easy-lightbox>
                        </div>
                        <img id="zoom_01" :src="product.image" :data-zoom-image="product.image" class="zoom" >   
                    </div>
                    <div class="carousel-item zoom-image">
                        <div class=Easylightbox>
                            <button @click="showSingle">Show single picture.</button>
                            <!-- all props & events -->
                            <vue-easy-lightbox
                                :visible="visible"
                                :imgs="product.image1"
                                :index="index"
                                @hide="handleHide"
                                >        
                            </vue-easy-lightbox>
                        </div>
                        <img id="zoom_01" :src="product.image1" class="zoom">
                    </div>
                    <div class="carousel-item zoom-image">
                        <div class=Easylightbox>
                            <button @click="showSingle">Show single picture.</button>
                            <!-- all props & events -->
                            <vue-easy-lightbox
                                :visible="visible"
                                :imgs="product.image2"
                                :index="index"
                                @hide="handleHide"
                                >        
                            </vue-easy-lightbox>
                        </div>
                        <img id="zoom_01" :src="product.image2" class="zoom">
                    </div>
                    <div class="carousel-item zoom-image">
                        <div class=Easylightbox>
                            <button @click="showSingle">Show single picture.</button>
                            <!-- all props & events -->
                            <vue-easy-lightbox
                                :visible="visible"
                                :imgs="product.image3"
                                :index="index"
                                @hide="handleHide"
                                >        
                            </vue-easy-lightbox>
                        </div>
                        <img id="zoom_01" :src="product.image3" class="zoom">
                    </div>
                    <div class="carousel-item zoom-image">
                        <div class=Easylightbox>
                            <button @click="showSingle">Show single picture.</button>
                            <!-- all props & events -->
                            <vue-easy-lightbox
                                :visible="visible"
                                :imgs="product.image4"
                                :index="index"
                                @hide="handleHide"
                                >        
                            </vue-easy-lightbox>
                        </div>
                        <img id="zoom_01" :src="product.image4" class="zoom">
                    </div>
                </div>

                <div class="col-12 col-product">
                    <ol class="carousel-indicators position-static m-0 justify-content-start" id="slider">
                        <li data-target="#productslider" data-slide-to="0" class="active">
                            <div class="data-slide-image">
                                <img :src="product.image" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="1">
                            <div class="data-slide-image">
                                <img :src="product.image1" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="2">
                            <div class="data-slide-image">
                                <img :src="product.image2" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="3">
                            <div class="data-slide-image">
                                <img :src="product.image3" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="4">
                            <div class="data-slide-image">
                                <img :src="product.image4" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom">
                            </div>
                        </li>
                        
                    </ol>
                </div>
                
            </div>
            <div class="col-md-8">
                <div class="detail-card card border-0 rounded shadow">
                    <div class="card-body">
                        <label class="title font-weight-bold"> {{ product.title }} </label>
                        
                        <div class="price-product" id="price-product" style="font-size: 1.35rem">
                            <s class="price font-weight-bold" style="text-decoration-color:red">Rp. {{ product.price }}</s>
                            <span
                                class="price font-weight-bold mr-4" style="color: green">Rp. {{ calculateDiscount(product) }}</span> 
                            
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
                            
                            <div>
                                <form class="">
                                <tr>     
                                    <label class="font-weight-bold">NO. HP / WHATSAPP</label>
                                    <input type="number"  class="data form-control" id="phone" placeholder="No. HP / WhatsApp">
                                                                
                                    <!-- <td class="font-weight-bold">{{ product.varian }} </td>
                                    <td>:</td>                           
                                    <input type="text"  class="fiil form-control" placeholder="Full Name">        -->
                                    <!-- <select type="text" name="size" id="size" class="form-control input-lg" value="text" required>
                                        <option>{{ product.varian1 }}</option>
                                        <option>{{ product.varian2 }}</option>
                                        <option>{{ product.varian3 }}</option>
                                        <option>{{ product.varian4 }}</option>   
                                    </select> -->
                                </tr>
                                <tr>                                  
                                    <td class="font-weight-bold">{{ product.variasi }} </td>
                                    <td>:</td>                     

                                    <select type="text" name="size" id="size" class="form-control input-lg" value="text" required>
                                        <option>{{ product.variasi1 }}</option>
                                        <option>{{ product.variasi2 }}</option>
                                        <option>{{ product.variasi3 }}</option>
                                        <option>{{ product.variasi4 }}</option>   
                                    </select>
                                </tr>
                            
                                <tr>                                  
                                    <td class="font-weight-bold">Jumlah </td>
                                    <td>:</td>                                  
                                    <select type="text" name="size" id="size" class="form-control input-lg" value="text" required>
                                        <option>1</option>
                                        <option>2</option>
                                        <option>3</option>
                                        <option>4</option>
                                        <option>5</option> 
                                        <option>6</option> 
                                        <option>7</option> 
                                        <option>8</option>
                                        <option>9</option>
                                        <option>10+</option>      
                                    </select>
                                </tr>
                                </form>
                            </div>
                            </tbody>    
                        </table>
                        <!-- <div v-if="state.addToCart"> -->
                            <button @click.prevent="addToCart(product.id, calculateDiscount(product), product.weight)"  class="btn btn-primary btn-lg btn-block" ><i class="fa fa-shopping-cart"></i> TAMBAH KE KERANJANG</button>
                        <!-- </div> -->
                    </div>
                </div>
            </div>
        </div>
        <div class="row mt-5">
            <div class="col-md-12">
                <div class="detail-card card border-0 rounded shadow">
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
