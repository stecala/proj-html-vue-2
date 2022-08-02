<template>
  <header class="container-fluid w-100 ">
        <div class="row" >

            <div class="col-lg-5 d-none d-xl-block">
                 <div class="row pt-4 mb-5">
                    <div class="col-9 mx-auto big-logo-container">
                        <img src="/img/logo-restaurant-2x.png" alt="restaurant logo">
                    </div>
                 </div>
                 <!-- card -->
                 <div class="row pt-5">
                    <div class="col-6 mx-auto mt-5">
                        <bannerCard :infoForCard="infoForCard" />
                    </div>
                 </div>
            </div>


            <!-- navbar -->
            <div class="col-12 col-lg-12 col-xl-7 position-relative px-0">
                <div class="row align-items-center">
                    <div class="col-9 d-lg-none small-logo-container">
                        <img src="/img/logo-restaurant-2x.png" alt="restaurant logo">
                    </div>
                    <div class="col-3 text-end d-lg-none" >
                        <label for="checkbox" class="hamburger"  >
                            <input type="checkbox" id="checkbox" >
                            <span class="line line-main" @click="changeStatusActive()"></span>
                            <span class="line line-split"></span>
                        </label>
                    </div>   
                </div>

                <!-- big navbar -->
                <nav class="d-lg-block d-none" >
                    <div class="gradient">
                        <ul class=" d-flex mx-auto justify-content-around flex-wrap w-100">
                            <li v-for="navbarLink in navbarItems" :key="navbarLink.id" class="d-flex flex-row" >
                                <a :href="navbarLink.url">
                                    <span :class="navbarLink.selected == true ? 'selected-link' : 'unselected-link'">{{navbarLink.name}}</span>
                                </a>
                                <div class="new-tile new-tile-white ms-2 align-self-center" v-if="navbarLink.new">
                                    <span>NEW</span>
                                </div>
                            </li>
                            <li class="unselected-link">
                                <a href="#"><i class="fa-solid fa-cart-shopping"></i></a> 
                            </li>
                        </ul>
                    </div>
                  
                </nav>

                <!-- dropdown menu -->
                <div class="position-absolute hamburger-dropdown-container " :class="isActive == true ? 'd-block scale-in-tr' : isFirst() ">
                    <ul class="pb-3">
                        <li v-for="navbarLink in navbarItems" :key="navbarLink.id" class="py-2 pe-5 d-flex"> 
                            <a :href="navbarLink.url">
                                <span :class="navbarLink.selected == true ? 'selected-dropdown-link' : 'unselected-dropdown-link'">{{navbarLink.name}}</span>
                            </a>
                            <div class="new-tile new-tile-dark ms-2 align-self-center" v-if="navbarLink.new">
                                <span>NEW</span>
                            </div>
                        </li>
                        <li class="unselected-dropdown-link">
                           <a href="#"><i class="fa-solid fa-cart-shopping"></i></a> 
                        </li> 
                    </ul>
                </div>

            </div>
        </div>
  </header>
</template>

<script>
import bannerCard from './common/bannerCard.vue'
export default {
    data(){
        return{
            isActive : false,
            counterForAnimation : 0,
            navbarItems : [
                {   
                    id : 0,
                    name : 'Home',
                    url : '#',
                    new : false,
                    selected : true,
                },
                {
                    id : 1,
                    name : 'Culinary History',
                    url : '#',
                    new : false,
                    selected : false,
                },
                {
                    id : 2,
                    name : 'Our Team',
                    url : '#',
                    new : false,
                    selected : false,
                },
                {
                    id : 3,
                    name : 'Our Menu',
                    url : '#menu',
                    new : false,
                    selected : false,
                },
                {
                    id : 4,
                    name : 'Takeout',
                    url : '#',
                    new : true,
                    selected : false,
                },
                {
                    id : 5,
                    name : 'Bulletin',
                    url : '#',
                    new : false,
                    selected : false,
                },
                {
                    id : 6,
                    name : 'Reservation',
                    url : '#',
                    new : false,
                    selected : false,
                },
            ],
            infoForCard : {
                subtitle : 'the best table in town',
                title : 'fine dining experience',
                text : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Fuga adipisci aut consequatur nam! Eius quas labore aperiam non.',
                btn : {
                    url : '#',
                    txt_btn : 'explore the menu' 
                }
            },
        }
    },
    methods:{
        changeStatusActive(){
            this.counterForAnimation++
            this.isActive = !this.isActive
            console.log(this.isActive , this.counterForAnimation)
        },
        resetStatusActive(){
            this.isActive = false
        },
        isFirst(){
            if(this.counterForAnimation == 0){
                return 'd-none'
            }
            else{
                return 'scale-out-tr'
            }
        }
    },
    components : {
        bannerCard,
    },
}
</script>

<style scoped lang="scss">
@import '../assets/style/dropdown.scss';
@import '../assets/style/hamburger.scss';

    header{
        background-color: var(--dark);
        color: var(--txt-white);
    }
    .small-logo-container{
        height: 50px;
        img{
            height: 100%;
            width: 100%;
            max-width: 285px;
        }
    }
    .big-logo-container{
        img{
            width: 100%;
            max-width: 300px;
        }
    }

    .new-tile{
        font-size: 0.6rem;
        font-weight: bold;
        border: 1px solid var(--dark-grey);
        padding: 2px 7px;
    }
    .new-tile-dark{
        color: var(--dark);
    }
    .new-tile-white{
        color: var(--txt-white);
    }
    nav{
        height: 100vh;
        background-image: url('../../public/img/slider52x.jpg');
        background-position: 50% 75%;
        background-size: cover;
        ul{
            list-style: none;
            padding: 0;
            li{
                display: inline-block;
                a{
                    
                    .unselected-link{
                        font-weight: 400;
                        color: var(--silver);
                    }
                    .selected-link{
                        font-weight: 700;
                        color: var(--txt-white);
                    }
                    &:hover{
                        color: var(--txt-white);
                    }
                }
                i{
                    color: var(--silver);
                }
               
            }
        }
    }
    .gradient{
        width: 100%;
        height: 100%;
        padding-top: 40px;
        background-image: linear-gradient(rgba(0, 0, 0, 0.651), transparent);
    }
</style>