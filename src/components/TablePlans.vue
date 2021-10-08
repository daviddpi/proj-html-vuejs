<template>
    <div class="row plans-section">
        <div class="col-12 text-center">
            <h1>Pricing Plans</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur aspernatur, saepe cum deserunt vero eius.</p>
        </div>
        <div class="col-12">
            <div class="svg-icon">
                <img id="icon-circle-svg" src="../assets/svg/svg-0.svg">
                <img id="cart" src="../assets/svg/svg-2.svg">
            </div>
            <table id="table-plans">
                <!-- Prezzi abbonamenti -->
                <tr>
                    <th><h4>Save up to 40% by paying weekly</h4></th>
                    <th class="price-plans">
                        <img class="img-fluid" src="../assets/img/h5-custom-icon-7.png" alt="immagine di una lampadina">
                        <h4>Standard <br>$12</h4>
                    </th>
                    <th class="price-plans">
                        <img class="img-fluid" src="../assets/img/h5-custom-icon-7.png" alt="immagine di una lampadina">
                        <h4>Standard <br>$12</h4>
                    </th>
                    <th class="price-plans">
                        <img class="img-fluid" src="../assets/img/h5-custom-icon-7.png" alt="immagine di una lampadina">
                        <h4>Standard <br>$12</h4>
                    </th>
                </tr>

                <tr>
                    <td>Number of Courses</td>
                    <td>2</td>
                    <td>2</td>
                    <td>2</td>
                </tr>
                <tr>
                    <td>Time</td>
                    <td>15 days</td>
                    <td>15 days</td>
                    <td>15 days</td>
                </tr>
                <tr>
                    <td>Web Designing</td>
                    <td>&check;</td>
                    <td>&check;</td>
                    <td>&check;</td>

                </tr>
                <tr>
                    <td>Human-Centered Design</td>
                    <td>&check;</td>
                    <td>&check;</td>
                    <td>&check;</td>

                </tr>
                <tr>
                    <td>Basic Marketing</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                </tr>
                <tr>
                    <td>Python for Everybody</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                </tr>
                <tr>
                    <td>Android Developer</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                </tr>
                <tr>
                    <td>Business English</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                    <td>&cross;</td>
                </tr>
                <tr>
                    <td></td>
                    <td>
                        <button class="mybtn btn-table">get it now</button>
                    </td>
                    <td>
                        <button class="mybtn">get it now</button>
                    </td>
                    <td>
                        <button class="mybtn btn-table">get it now</button>
                    </td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
export default {
    name: "tablePlans",
}
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/color.scss';

.plans-section{

    position: relative;

    .svg-icon{
        position: absolute;
        top: 300px;
        right: -8.5px;
        transform: translate(50%);
        img{
            display: block;
            height: 40px;
            width: 40px;

            &:hover{
                cursor: pointer;
            }
        }

        #icon-circle-svg{
            background-color: #ee2852;
            padding: 2.5px;
            margin-bottom: 7px;
        }

        #cart{
            padding: 5px;
            background-color: $whiteColor;
        }
    }

    h1{
        font-family: $primaryFont;
    }
    p{
        margin-bottom: 100px;
    }

    #table-plans{
        margin: 0 auto;
    }

    #table-plans td, #table-plans th {
        border: 1px solid #ddd;
        padding: 8px;
    }

    #table-plans{

        th{
            width: calc(100% / 4);
            background-color: $whiteColor;
            border-top: 5px solid #d6f2ff;
            padding: 15px;
            font-family: $primaryFont;
        }

        tr:last-child{
            td{
                background-color: #f7fdff;

            }

            td:first-child{
                border-left: none;
                border-bottom: none;
            }
        }

        td{
            height: 60px;
            background-color: $whiteColor;
        }

        td:first-child{
            font-family: $primaryFont;
            padding-left: 20px;
        }

        td:not(:first-child){
            text-align: center;
        }

        .price-plans{
            background-color: #f7fdff;
            text-align: center;
        }

        .btn-table{
            background-color: $whiteColor;
            color: #808080;
            border: 1px solid #eaebeb;
        }

    }
}
</style>