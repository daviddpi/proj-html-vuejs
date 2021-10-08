<template>
    <div class="row popular-courses">
        <div class="col-12 text-center">
            <h1>Popular Online Courses</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur aspernatur, saepe cum deserunt vero eius esse nihil, explicabo optio possimus.</p>
        </div>
        <div class="col-12 col-md-4 info-courses" v-for="(element, index) in arrayCourses[indexBox]" :key="'outer'+index">
            <div class="img-hoover-zoom">
                <img class="img-fluid" :src="require(`../assets/img/${element.src}`)" alt="Immagine">
            </div>
            <div class="info-courses-text">
                <div class="d-flex justify-content-between">
                    <h5>{{ element.course }}</h5>
                    <div class="cost-course cost-course-free align-self-center" :class="(element.cost != 'free') ? notFree : freeCost">{{element.cost}}</div>
                </div>

                <h6>{{element.name}}</h6>
                <p>{{element.info}}</p>
                <div class="d-flex mb-3">
                    <div class="d-flex align-items-center me-2">
                        <i class="fas fa-user"></i><span>{{element.user}}</span>
                    </div>
                    <div class="d-flex align-items-center">
                        <i class="fas fa-tag"></i><span>{{element.type}}</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="circle-container">
            <div class="circle-index" @click="activeBox(sign)" v-for="(circle, sign) in arrayCourses.length" :key="sign"
            :class="(sign == indexBox) ? active : ''"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: "BoxCourses",
    props: {
        arrayCourses: Array
    },

    data(){
        return{
            indexBox: 0,
            active: 'active',
            freeCost: "cost-course-free",
            notFree: "cost-not-free",
        }
    },

    methods: {
        activeBox(sign){
            this.indexBox = sign;
        }
    },
}   
</script>

<style lang="scss" scoped>
@import '../style/general.scss';
@import '../style/color.scss';


.popular-courses{

    h1{
        font-family: $primaryFont;
        font-weight: bold;
        margin-bottom: 15px;
    }

    p{
        width: 70%;
        margin: 0 auto;
        margin-bottom: 100px;
    }

    .circle-container{
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top: 45px;
    }

    .circle-index{
        height: 15px;
        width: 15px;
        background-color: rgba(85, 172, 238, 0.5);
        border-radius: 50%;
        margin: 0 10px;
    }

    .active{
        background-color: $backgroundPrimary;
    }
}

.info-courses{

    .img-hoover-zoom{
        overflow: hidden;

        img{
            transition: transform .5s ease;

            &:hover{
                transform: scale(1.3);
            }
        }
    }

    .info-courses-text{
        border: 0.5px solid #f2f2f2;
        padding: 10px;
        padding-top: 15px;
        background-color: $whiteColor;
        position: relative;
        h5{
            // padding-top: 15px;
            font-family: $primaryFont;
            font-weight: bold;
            font-size: 1.2rem;
        }

        h6{
            font-size: 0.9rem;
            color: $textColorGrey;
        }

        p{
            width: 100%;
            margin-bottom: 20px;
            color: #a4a4a4;
        }

        i{
            color: #b9b9b9;
            padding-right: 5px;
        }

        span{
            color: #b9b9b9;
            text-transform: uppercase;
        }

        .fa-tag{
            transform: rotate(90deg);
            padding: 0 5px;
        }

        .cost-course{
            text-transform: uppercase;
            color: $whiteColor;
            border-radius: 20px;
            font-size: 0.8rem;
            padding: 2px 12px;
        }

        .cost-course-free{
            background-color: #ffd740;
        }

        .cost-not-free{
             background-color: $backgroundPrimary
        }
    }
}
</style>