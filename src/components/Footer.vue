<style>
    .pt-5, .py-5 {
        padding-top: 3rem!important;
        display: block;
    }
    p {
        margin-top: 0;
        margin-bottom: 1rem;
    }
    .mr-4, .mx-4 {
        margin-right: 1.5rem!important;
    }
    .fab, .far {
        font-weight: 400;
        font-family: "Font Awesome 5 Brands";
        font-size: 2em;
    }
    @media (min-width: 270px) and (max-width: 767px)
    {
        .pt-5, .py-5 {
            padding-top: 2rem!important;
            display: block;
        }
    }
</style>
<template>
    <footer style="background: #ffffff;border-top: 5px solid #6677ef;" class="pt-5">
        <div class="container-fluid">
            <div class="row-bottom">
                <div class="col-md-5-footer mb-4">
                    <h4 class="font-weight-bold">TENTANG</h4>
                    <hr style="border-top: 3px solid rgb(226 232 240);border-radius:.5rem">
                    <p>
                        Toko Online Shopping/Store Terpercaya di Indonesia. Jual Beli Aman & Harga Termurah! Belanja
                        sekarang.
                    </p>
                    <div class="social">
                        <a href="#" class="mr-4"> <i class="fab fa-facebook fa-2x"></i></a>
                        <a href="#" class="mr-4" style="color:#00c4ff"> <i class="fab fa-twitter fa-2x"></i></a>
                        <a href="#" class="mr-4" style="color: #de2fb8;"> <i class="fab fa-instagram fa-2x"></i></a>
                        <a href="#" style="color: red;"> <i class="fab fa-youtube fa-2x"></i></a>
                    </div>
                </div>
                <div class="col-md-3-footer mb-4">
                    <h4 class="font-weight-bold">PEMBAYARAAN</h4>
                    <hr style="border-top: 3px solid rgb(226 232 240);border-radius:.5rem">
                    <div class="row-footer">
                        <div class="col-md-4 col-4 mb-3">
                            <div class="card h-100 border-0 rounded shadow">
                                <div class="card-body p-2 text-center">
                                    <img src="@/assets/payment/BCA.png" style="width: 50px;">
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4 col-4 mb-3">
                            <div class="card h-100 border-0 rounded shadow">
                                <div class="card-body p-2 text-center">
                                    <img src="@/assets/payment/BNI.png" style="width: 45px;">
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4 col-4 mb-3">
                            <div class="card h-100 border-0 rounded shadow">
                                <div class="card-body p-2 text-center">
                                    <img src="@/assets/payment/BRI.png" style="width: 60px;">
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4 col-4 mb-3">
                            <div class="card h-100 border-0 rounded shadow">
                                <div class="card-body p-2 text-center">
                                    <img src="@/assets/payment/GOPAY.png" style="width: 60px;">
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4 col-4 mb-3">
                            <div class="card h-100 border-0 rounded shadow">
                                <div class="card-body p-2 text-center">
                                    <img src="@/assets/payment/indomaret-logo.png" style="width: 60px;">
                                </div>
                            </div>
                        </div>
                        <div class="col-md-4 col-4 mb-3">
                            <div class="card h-100 border-0 rounded shadow">
                                <div class="card-body p-2 text-center">
                                    <img src="@/assets/payment/atm-bersama.jpg" style="width: 40px;">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-4-footer mb-4">
                    <h4 class="font-weight-bold">KONTAK</h4>
                    <hr style="border-top: 3px solid rgb(226 232 240);border-radius:.5rem">
                    <p>
                        <i class="fa fa-clock"></i> Toko Buka Setiap Hari :
                        <br>
                        Senin - Minggu ( 07.00 s/d 21.00 )
                    </p>
                    <p>
                        <i class="fa fa-map-marker"></i> Jl.Penjernihan, Bendungan hilir, Jakarta City DKI Jakarta, 58591
                    </p>
                </div>
            </div>
            <div class="row text-center mt-3 pb-3">
                <div class="col-md-12">
                    <hr>
                    © <strong>Online Shop</strong> 2020 • Hak Cipta Dilindungi
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {

    }
</script>