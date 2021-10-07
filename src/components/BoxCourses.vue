<template>
    <div class="row popular-courses">
        <div class="col-12 text-center">
            <h1>Popular Online Courses</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Pariatur aspernatur, saepe cum deserunt vero eius esse nihil, explicabo optio possimus.</p>
        </div>
        <div class="col-4 info-courses">
            <img class="img-fluid" src="../assets/img/course-5-f-img.jpg" alt="">
            <div class="info-courses-text">
                <div class="d-flex justify-content-lg-between">
                    <h5>Android Developer</h5>
                    <div class="cost-course cost-course-free align-self-center">free</div>
                </div>

                <h6>David Sanders</h6>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Non minus asperiores sit iusto reprehenderit ullam illo qui</p>
                <div class="d-flex mb-3">
                    <div class="d-flex align-items-center me-2">
                        <i class="fas fa-user"></i><span>1</span>
                    </div>
                    <div class="d-flex align-items-center">
                        <i class="fas fa-tag"></i><span>Programming</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="col-4"></div>
        <div class="col-4"></div>

        <div class="circle-container">
            <div class="circle-index"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: "BoxCourses",
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
        background-color: $backgroundPrimary;
        border-radius: 50%;
        margin: 0 10px;
    }
}

.info-courses{
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
        }

        .cost-course{
            text-transform: uppercase;
            background-color: $backgroundPrimary;
            color: $whiteColor;
            border-radius: 20px;
            font-size: 0.8rem;
            padding: 2px 12px;
        }

        .cost-course-free{
            background-color: #ffd740;
        }
    }
}
</style>