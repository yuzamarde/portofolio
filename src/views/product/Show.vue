
<style>
    .container-fluid, .container-lg, .container-md, .container-sm, .container-xl {
        width: 100%;
        padding-right: 10px;
        padding-left: 10px;
        margin-right: auto;
        margin-left: auto;
    }
    
    .product {
        display: grid;
        grid-template-columns: 65% auto;
        padding-bottom: 45px;
        column-gap: 15px;
        
    }
    .product .col-md-4{
        max-width: 100%;
        padding: 0px;
        height: 700px;
    }
    .product .col-md-4 .rounded{
        padding: 0px;
    }
    .rounded-content{
        box-shadow: 0 .5rem 1rem rgba(0,0,0,.15)!important;
    }
    .product .col-md-4 .rounded .p-2{
        padding: 0px !important;
    }       
        
    .product .col-md-8{
        max-width: 100%;
        padding: 0px !important;
    }
    .detail-card{
        height: 50rem;
    }
    .data-slide-image {
            display: flex;
        }
    .col-md-4 .col-product {
        padding: 0px;
        display: flex;
        position: inherit;
        margin-top: -130px;
        justify-content: center;
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
    div .price-product {
        display: flex;
        width: 100%;
        gap: 10px;
    }
    .title{
        font-size: 30px;
    }
    .btn-sm {
        padding: 0px 5px;
        font-size: 10px;
        line-height: 0;
        border-radius: .2rem;
        width: -webkit-fit-content;
        width: -moz-fit-content;
        width: fit-content;
    }
    .btn-add{
        display: inline-block;
        font-weight: 400;
        z-index: 0;
        position: absolute;
        color: #ffffff;
        text-align: center;
        margin-top: 10px !important;
        vertical-align: middle;
        width: 90%;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        background: linear-gradient( 90deg ,#9758ea,#5f10f3);
        
        border: 1px solid transparent;
        padding: .375rem .75rem;
        font-size: 0.7rem;
        line-height: 1.5;
        border-radius: .80rem;
        transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
    }
    .btn-disable {
        display: inline-block;
        position: absolute;
        font-weight: 400;
        color: #ffffff;
        text-align: center;
        margin-top: 10px !important;
        vertical-align: middle;
        width: 90%;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        border: 1px solid transparent;
        padding: .375rem .75rem;
        font-size: 0.7rem;
        line-height: 1.5;
        border-radius: .80rem;
        transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
    }
    .btn-disable:hover {
        display: inline-block;
        position: absolute;
        font-weight: 400;
        color: #f5f0f0;
    }
    .description {
        width: 100%;
        display: table-row;
    }
    .series {
        display: flex!important;
        padding-top: 20px;
        gap: 10px;
    }
    .form-fill .series .s-flex {
        display: flex!important;
        flex-direction: column;
        width: 60%;
    }
    .form-fill .s-flex .font-weight-bold{
        font-weight: 100;
        gap: 0px;
        text-align: inherit;
        padding: 0px;
    }
    .form-fill .s-flex {
        width: 30%;
        display: flex;
        padding-bottom: 5px;
        flex-direction: column;
    }
    form .series .s-flex .font-weight-bold{
        font-weight: 100;
        gap: 0px;
        text-align: inherit;
        padding: 0px;
    }
    .a-flex {
        display: flex!important;
        padding-top: 25px;
        gap: 10px;
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
        justify-content: space-between !important;
        padding-left: 0;
        margin-right: 15%;
        margin-left: 15%;
        list-style: none;
        flex-wrap: inherit;
        gap: 7px;
    }
    
    .zoom-image{
        height: 50rem;
    }
    .Easylightbox button {
        position: absolute;
        height: -webkit-fill-available;
        width: -webkit-fill-available;
        opacity: 0;
    }
    .card-description {
        background: #ffffff;
        color: black;
        padding-top: 15px;
        width: 100%;
        border: #ffffff;
    }
    .form-control-option {
        display: flex;
        width: 90%;
        height: calc(1.5em + .75rem + 2px);
        padding: .375rem .75rem;
        font-size: 1rem;
        font-weight: 400;
        line-height: 1.5;
        color: #495057;
        background-color: rgb(240, 239, 239);
        background-clip: padding-box;
        border: 1px solid #ced4da;
        border-radius: 0.30rem 0.30rem 0.30rem 0.30rem;
        transition: border-color .15s ease-in-out;
        box-shadow: .15s ease-in-out;
        position: relative;
        flex: 1 1 auto;
        min-width: 0;
        margin-bottom: 0;
    }
    .carousel-inner-product {
            position: relative;
            width: 100%;
            overflow: hidden;
            border-radius: 30px;
            box-shadow: 0 .5rem 1rem rgba(0,0,0,.15)!important;
        }
    .zoom{
        width: 100%;
         object-fit: cover;
         height: 100%;
    }
    .card-body-keterangan {
        padding: 30px;
    }
    .price-product .price{
        font-size: 20px;
    }
    .zoom-li{
        border-radius: 10px;
        box-shadow: 0 .5rem 1rem rgba(0,0,0,.15)!important;
    }
    .click-zoom{
        position: absolute;
        color: #fff;
        padding: 15px;
    }
    @media (min-width: 270px) and (max-width: 767px)
    {
        html, body {
            max-width: 100%;
            overflow-x: hidden;
        } 
        .product {
            display: flex;
            flex-direction: column;
            padding-bottom: 0px;
            -moz-column-gap: 15px;
            column-gap: 15px;
        }
        .zoom-li{
            width: 50px !important;
            height: 50px !important;
            border-radius: 10px;
            box-shadow: none !important;
        }
        .btn-sm {
            padding: 0px 5px;
            font-size: 10px;
            line-height: 0;
            border-radius: .2rem;
            width: fit-content;
        }
        .zoom{
            width: 100%;
            height: 70vh;
            object-fit: cover;
        }
        .col-md-8 .detail-card {
            display: flex;
            padding: 0px 15px 15px 15px;
            height: fit-content;
            box-shadow: none !important;
        }
        .series {
            display: flex!important;
            padding-top: 15px;
            gap: 10px;
        }
        .form-control-option {
            display: flex;
            width: 90%;
            height: calc(1.5em + .75rem + 2px);
            padding: 5px 5px 5px 5px;
            font-size: .7rem;
            height: 25px;
        }
        .btn-add {
            margin-top: 5px !important;
            vertical-align: middle;
            width: 92%;
        }
        .btn-disable {
            margin-top: 5px !important;
            vertical-align: middle;
            width: 92%;
        }
        .col-md-8 .card .card-body-product .title {
            text-align: left;
            color: #fff;
            /* display: block; */
            font-weight: 700 !important;
            position: absolute;
            margin-top: -135px;
            font-size: 18px !important;
            text-shadow: 1px 3px 7px black;
        }
        .carousel-item{
            height: auto;
        }
        .product .col-md-4 {
            max-width: 100%;
            padding: 0px;
            height: fit-content;
        }
        .table {
            width: 100%;
            margin-bottom: 5px;
            color: #212529;
        }
        .container{
            padding-left: 15px !important;
            padding-right: 15px !important;
        }
        .dashboar {
            padding-top: 0rem;
        }
        .col-md-4 .col-product {
            padding: 0px;
            background-color: rgb(255, 255, 255);
            border-radius: 15px 15px 0px 0px;
            display: flex;
            position: inherit;
            margin-top: -20px;
            padding-left: 15px;
            padding-right: 10px;
            justify-content: left;
        }
        .col-product li{
            margin: 15px 0 10px 0;
        }
        .price-product .price{
            font-size: 17px;
        }
        .rounded-content {
            box-shadow: none !important;
        }
        .carousel-inner-product {
            position: relative;
            width: 100%;
            height: 70%;
            overflow: hidden;
            padding-top: 35px;
            border-radius: 0px;
        }
        .col-md-8 .card .card-body .price {
            text-align: center;
            font-size: 15px !important;
        }
        .card-body-product{
            flex: 0 0 auto;
            min-height: 1px;
            padding: 0px 0px 30px 0px;
        }
        .card-body-keterangan {
            padding: 15px;
        }
        .font-weight-bold {
            font-weight: 100!important;
        }
        .badge-success {
            color: #fff;
            font-size: 7px !important;
            background-color: #ffc107  !important;
        }
        .click-zoom{
            position: absolute;
            color: #fff;
            padding: 5px;
            font-size: 10px;
        }
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
                <div class="carousel-inner-product">
                    
                    <div class="carousel-item active zoom-image" >
                        <span class="click-zoom">click to zoom</span>
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
                                <img :src="product.image" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom-li">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="1">
                            <div class="data-slide-image">
                                <img :src="product.image1" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom-li">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="2">
                            <div class="data-slide-image">
                                <img :src="product.image2" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom-li">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="3">
                            <div class="data-slide-image">
                                <img :src="product.image3" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom-li">
                            </div>
                        </li>
                        <li data-target="#productslider" data-slide-to="4">
                            <div class="data-slide-image">
                                <img :src="product.image4" onerror="this.style.display='none'; opacity: '0';" style="width: 100px; height: 100px;" class="zoom-li">
                            </div>
                        </li>
                        
                    </ol>
                </div>
                
            </div>
            <div class="col-md-8">
                <div class="detail-card card border-0 rounded shadow">
                    <div class="card-body-product" @change="getName" >
                        <label class="title font-weight-bold"> {{ product.title }} </label>
                        
                        <div class="price-product" id="price-product" style="font-size: 1.35rem">
                              
                                <button class="btn btn-sm" style="color: #ffffff;background: #ffc107;">
                                        DISKON {{ product.discount }} %
                                </button>
                            
                            <s class="price font-weight-bold" style="text-decoration-color:red; font-weight: 700!important;">Rp. {{ product.price }}</s>
                            <span
                                class="price font-weight-bold mr-4" style="color: green;font-weight: 700!important;">Rp. {{ calculateDiscount(product) }}</span> 
                            
                        </div>
                        <table class="table table-borderless mt-3">
                            
                            
                            <div class="description">
                                <form class="form-fill" >
                                    
                                    <div class="series">
                                        <tr class="s-flex" @change="getSeries" >                                  
                                            <td class="font-weight-bold">{{ product.varian }} : </td>
                                                                    

                                            <select type="text" name="size" id="size" class="form-control-option input-lg" value="text" 
                                                v-model="state.type1" required>
                                                <option>{{ product.varian1 }}</option>
                                                <option>{{ product.varian2 }}</option>
                                                <option>{{ product.varian3 }}</option>
                                                <option>{{ product.varian4 }}</option>   
                                            </select>

                                        </tr>
                                        <tr class="s-flex">                          
                                            <td class="font-weight-bold">{{ product.variasi }} : </td>                              
                                            <select type="text" name="size" id="size" class="form-control-option input-lg" value="text"  v-model="state.type2" required>
                                                <option>{{ product.variasi1 }}</option>
                                                <option>{{ product.variasi2 }}</option>
                                                <option>{{ product.variasi3 }}</option>
                                                <option>{{ product.variasi4 }}</option>      
                                            </select>
                                        </tr>
                                    </div> 
                                    <tr class="s-flex">     
                                        <td class="font-weight-bold"> Jumlah : </td>                        
                                                
                                        <select type="text" name="size" id="size" class="form-control-option input-lg" value="text" v-model="state.jumlah" @change="getProperties" required>
                                                
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
                        </table>
                        <table class="table table-borderless mt-3">
                            <button class="btn btn-disable btn-lg btn-block" style="background:#bbb9b9;" ><i class="fa fa-shopping-cart"  type="submit"></i> TAMBAH KE KERANJANG</button>    
                        
                            <button v-if="state.addToCart" @click.prevent="addToCart(product.id, calculateDiscount(product), product.weight, product.varian)" class="btn btn-add btn-lg btn-block" ><i class="fa fa-shopping-cart" type="submit"></i> TAMBAH KE KERANJANG</button>    
                        </table>
                        
                        <div class="a-flex">
                            <a :href="product.link1" class="btn btn-primary btn-lg btn-block" style="cursor:pointer; background: linear-gradient( -180deg,#008543,#2DA947);"><i class="fa fa-shopping-cart"></i> TOKOPEDIA</a>
                                
                            <a :href="product.link2" class="btn btn-primary btn-lg btn-block" style="cursor:pointer; background: linear-gradient( -180deg,#f53d2d,#f63);"><i class="fa fa-shopping-cart"></i> SHOPEE</a>
                        </div>
                    </div>
                    <div class="card-description">
                        <label class="" style="font-size: 20px;">Detail product
                        </label>
                        
                        <hr>
                        <div>
                            <tr>
                                <td class="font-weight-bold" style="padding-left: 0px;">BERAT</td>
                                <td>:</td>
                                <td>
                                    <span class="badge badge-pill badge-success"
                                        style="font-size: 14px;border-radius: .3rem;padding: .25em .5em .2em;"> {{ product.weight }}
                                        gram</span>
                                </td>
                            </tr>
                        </div> 
                        <div v-html="product.description"></div>
                    </div>        
                </div>
            </div>
        </div>
        <div class="row mt-5">
            <div class="col-md-12">
                <div class="card border-0 rounded-content shadow">
                    <div class="card-body-keterangan">
                        <label class="font-weight-bold" style="font-size: 20px;">Keterangan</label>
                        <hr>
                        <div v-html="product.content"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
</template>


<script>
import { ref, computed, onMounted, reactive } from 'vue'   // computed dan onMounted

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
                    this.imgs = 'http://via.placeholder.com/350x150'
                    // or
                    this.imgs = {
                    title: 'this is a placeholder',
                    src: 'http://via.placeholder.com/350x150'
                    }
                    this.show()
                },
                showMultiple() {
                    // this.imgs = [
                    // 'http://localhost:8000/storage/products/puxAYov7votos8ClIs4GEnPBA74Bao2UBA59mAD5.jpeg',
                    // 'http://localhost:8000/storage/products/gETJuuiLv6eQSOsFHoTz7WTQxfom9RSCpGhNeNdB.jpeg'
                    // ]
                    // or
                    this.imgs = [
                    {src: 'http://localhost:8000/storage/products/puxAYov7votos8ClIs4GEnPBA74Bao2UBA59mAD5.jpeg' },
                    'http://localhost:8000/storage/products/gETJuuiLv6eQSOsFHoTz7WTQxfom9RSCpGhNeNdB.jpeg'
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

            //user state
            
            //validation state
            const validation = ref([])

            //onMounted akan menjalankan action "getDetailProduct" di module "product" Vuex
            onMounted(() => {
                store.dispatch('product/getDetailProduct', route.params.slug)
            })

            //computed properti digunakan untuk mendapatkan data detail product dari state "product" di module "product" Vuex
            const product = computed(() => {
                return store.state.product.product
            })

            const state = reactive({
                jumlah:          '',
                type1:          '',
                type2:          ''      // <-- state jumlah   
            })

            // const validation = reactive({
            //     jumlah:      false, // <-- validation jumlah
            // })
            /**
             * function addToCart
             */
            
            function addToCart(product_id, price, weight,) {
                
                //check token terlebih dahulu
                const token = store.state.auth.token
                
                if(!token) {  
                    return router.push({name: 'login'})
                }

                //panggil action addToCart di module cart
                store.dispatch('cart/addToCart', {
                    product_id: product_id,
                    price: price*state.jumlah,
                    weight: weight*state.jumlah,
                    quantity: state.jumlah,
                    type1: state.type1,
                    type2: state.type2
                    
                }) 
                let jumlah = state.jumlah 
                let type1 = state.type1  
                let type2 = state.type2              
                store.dispatch('cart/addToCart', jumlah, type1, type2)
                .catch(error => {
                    //assign validaation message
                    validation.value = error
                })
                
            }
            
            
            function getProperties (){
                //show button checkout
                state.addToCart = true
                
            }
            
            // if (!state.jumlah) {
            //     validation.jumlah = true
            // }
            

            return {
                route,
                router,
                store,
                state,              // <-- state form
                validation,
                product,
                getProperties,
                addToCart
            }
        
        }

    }
</script>

