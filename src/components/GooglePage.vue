<template>
    <div class="">
        <div class="flex justify-end bg-transperant my-2">
            <a href="#responsive-header" class="inline-block text-center lg:text-sm text-xs lg:px-2 lg:pt-3 px-1 pt-3 leading-none border rounded text-black-700 border-white">
                Gmail
            </a>
            <a href="https://www.google.co.in/imghp?hl=en&tab=ri&ogbl" class="inline-block text-center lg:text-sm text-xs lg:px-2 px-1 pt-3 leading-none border rounded text-black-700 border-white">
                Images
            </a>
            <a href="#" class="inline-block text-center lg:text-sm text-xs px-3 py-3 leading-none border rounded-full text-black-700 border-white hover:border-transparent hover:text-black-900 hover:bg-gray-200"><i class="fas fa-th fa-1x"></i></a>
            <a href="#" class="inline-block text-center lg:text-lg text-xs mx-2 my-1 lg:px-3 lg:py-2 px-2 py-2 leading-none border rounded-full text-black-700 border-white border-4 text-black-900 bg-red-900 text-white hover:border-gray-400">D</a>  
        </div> 
        <div class="justify-center flex lg:mt-24 sm:mt-10 xs:mt-10">
            <div class="w-1/3  h-auto"></div>
            <div class="w-1/3  h-auto justify-center">
                <img alt="google logo" class="object-center lg:h-32 sm:h-12 lg:w-8/12 lg:mx-16 md:mx-8 sm:mx-16 lg:pl-8 md:mx-8" src="../assets/google.png" />
            </div>
            <div class="w-1/3  h-auto"></div>
        </div> 
        <div class="flex mb-4">
            <div class="w-1/4 h-auto"></div>
            <div class="w-1/2 h-auto">
                <div class="w-auto mt-4">
                    <div class="justify-center flex">
                        <div class="flex shadow rounded-full border-gray-200 border-2 lg:h-12 w-4/5 mx-auto">
                            <div class="pin-r pin-t sm:mx-3 lg:py-3">
                                <i class="fa fa-search lg:text-lg text-xs lg:mx-1 mx-1" aria-hidden="true"></i>
                            </div>
                            <input type="search" class="w-full outline-none lg:h-auto sm:h-6 lg:text-lg text-xs" placeholder="Search Google or type a URL">
                            <div class="pin-r pin-t float-right sm:mx-1 lg:py-3">
                                <i class="fa fa-microphone lg:text-lg text-xs lg:mx-4 mx-1" aria-hidden="true"></i>    
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="w-1/4 h-auto"></div>
        </div>
        <div class="lg:mx-4 mx-2"> 
            <div class="justify-center flex lg:mx-32 mt-6 lsm:w-full">
                <div class="container justify-center flex lg:w-full my-2 lg:mx-64">
                    <div class="h-auto lg:w-auto w-auto pt-4 pb-4 bg-white sm:rounded-t md:rounded-b-lg lg:rounded xl:rounded-r hover:border-black hover:text-black-900 hover:bg-gray-200" v-for="item in items" v-bind:key="item.id" >
                        <div class="bg-gray-300 h-12 w-12 lg:mx-10 mx-3 justify-center rounded-full"> 
                            <img alt="Vue logo" :src="item.img" width="55%" class="pt-3 ml-3" />
                        </div>    
                        <div class="text-center mt-5"> <p class="text-xs font-sans font-semibold">{{item.msg}}</p></div>
                    </div>
                    <div class="h-auto w-auto pt-4 pb-4 bg-white sm:rounded-t md:rounded-b-lg lg:rounded xl:rounded-r hover:border-black hover:text-black-900 hover:bg-gray-200" >
                        <div class="bg-gray-300 h-12 w-12 lg:mx-8 mx-2 justify-center rounded-full"> 
                            <img alt="Vue logo" src="../assets/plus.png" width="30%" class="pt-4 ml-4" />
                        </div>    
                        <div class="text-center mt-5"> <p class="text-xs font-sans font-semibold">Add shortcut</p></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'GooglePage',
        props: {
            msg: {
            type: String,
            default: '',
            },
        },
        data () {
            return {
                items: [
                    {id:1,
                    img: require('../assets/logo.png'),
                    msg:"hello"},
                    {id:2,
                    img:require("../assets/github.svg"),
                    msg:"Github"},
                    {id:3,
                    img:require('../assets/cp.png'),
                    msg:"Webmail Login"},
                    {id:4,
                    img:require('../assets/gmail.png'),
                    msg:"Gmail"},
                ]
            }
        },
    };
</script>