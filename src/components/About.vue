<template>
    <main>

        <!-- START SECTION TOP -->
        <div class="parallax colored-bg pattern-bg" data-stellar-background-ratio="0.5">
            <div class="container">
                <div class="row">
                    <div class="col-sm-12">
                        <h1 class="page-title">Nosotros</h1>

                        <ul class="breadcrumb">
                            <li><router-link to="/">Inicio </router-link></li>
                            <li><b>Nosotros</b></li>
                        </ul>
                    </div> 
                </div>
            </div>
        </div>
        <!-- END SECTION TOP -->

        <!-- BEGIN HIGHLIGHT -->
        <div class="content">
            <div class="container">
                <div class="row">
                    <div class="main col-sm-12">
                        <div class="center">
                            <br>
                            <h2 class="section-highlight" data-animation-direction="from-left" data-animation-delay="50">{{company}}<br>
                                <h4>"El lado humano de las bienes raíces"</h4>
                            </h2>                            <br>
                            <div class="row">
                                <div class="col-md-12">
                                    <h2 class="darker-text" data-animation-direction="from-left" data-animation-delay="250">
                                        <b>Nuestra Empresa </b>
                                    </h2><br>
                                     <p class="text-darker" data-animation-direction="from-left" data-animation-delay="650">
                                        Somos una Empresa con Cimientos Sólidos, con Amplios Conocimientos del Mercado Inmobiliario, ofreciéndote servicios integrales en todo lo relacionado a los Bienes Raíces.
                                    </p>                                    
                                    <p class="text-darker" data-animation-direction="from-left" data-animation-delay="650">
                                        Derivamos de una franquicia española y estamos en México ocupando los estados con mayor Potencial de Crecimiento y Plusvalía .. Querétaro, y Quintana Roo .Tu mejor inversión .
                                    </p>                                                                       
                                </div>
                            </div>
                            <br>
                            <div class="row">
                                <div class="col-md-4">
                                    <h2 class="darker-text" data-animation-direction="from-left" data-animation-delay="250">
                                        <b>VISION</b>
                                    </h2><br>
                                     <p class="text-darker" data-animation-direction="from-left" data-animation-delay="650">
                                        Ser la mejor opción Inmobiliaria, ofreciendo servicios integrales en Bienes Raíces; desde una Renta hasta la construcción tipo Residencial, Comercial e Industrial que brinden confianza, seguridad y Plusvalía a todos nuestros clientes.
                                    </p>
                                </div>
                                <div class="col-md-4">
                                    <h2 class="darker-text" data-animation-direction="from-left" data-animation-delay="250">
                                        <b>MISIÓN</b>
                                    </h2><br>
                                     <p class="text-darker" data-animation-direction="from-left" data-animation-delay="650">
                                        Contribuir al desarrollo del mercado inmobiliario basados en la Honestidad y Transparencia como principios Rectores de nuestros Actos, construyendo sólidas relaciones entre clientes compradores, vendedores, proveedores, Y prestadores de servicios, con el fin de que todos alcancen sus Sueños, Metas y Objetivos Particulares
                                    </p>
                                </div>
                                <div class="col-md-4">
                                    <h2 class="darker-text" data-animation-direction="from-left" data-animation-delay="250">
                                        <b>SERVICIOS</b>
                                    </h2><br>
                                     <ul class="text-darker" data-animation-direction="from-left" data-animation-delay="650">
                                        <li>Compra</li>
                                        <li>Venta</li>
                                        <li>Renta</li>
                                        <li>Créditos Bancarios / Infonavit                                        </li>
                                        <li>Construcción habitacional, industrial y Comercial</li>
                                        <li>Recuperación de Impuestos</li>
                                    </ul>
                                </div>
                            </div>
                            <br>                            
                            <br>
                            <router-link to="/contacto" class="btn btn-default-color" data-animation-direction="from-left" data-animation-delay="850">Contáctanos</router-link>
                        </div>
                    </div>
                    <br>               
                </div>
            </div>
        </div>
        <br>
        <!-- END HIGHLIGHT -->         
        <br>																			
    </main>
</template>

<script>
    import immoService from '@/services/immo.js';
    export default {
        name: 'app',
        data(){
            return{
                company:[],
                logo:[]
            }		
        },
        created(){
            window.scrollTo(0,0);
            immoService.getInfoCompany()
                .then(res => {
                    const foDat=res[0]
                    this.logo=foDat.logo
                    this.company=foDat.company
                })
        }
    }
</script>

<style>
    #ampi-logo img {
        margin-top: 50px;
        border-radius: 9px;
        width: 100px;
    }
    #about-img{
        width:60%;
        text-align: center;
        float: right;
    }
    .text-contact{    
        font-size: 16px;
        text-transform: uppercase;
    }
</style>