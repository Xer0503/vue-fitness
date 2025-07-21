<script setup></script>
<template>
    <div class="grid md:grid-cols-3 text-center p-3 py-5 bg-gray-200">
        <div>Location</div>
        <div class="px-3">

            <form action="#">
                <div id="contact" class="flex flex-col gap-5">
                    <h1 class="font-bold text-3xl">Contact Us</h1>
                    <input class="border px-2 py-2 w-auto shadow rounded-2xl" type="text" placeholder="email">
                    <textarea class="border shadow px-2 py-3 rounded" name="" id="" cols="3" placeholder="message here"></textarea>
                    <span class="text-center">
                        <button class="bg-orange-600 text-white w-35 rounded-2xl py-2">Send</button>
                    </span>
                </div>
            </form>
        </div>

        <div id="about">
            <ul>
                <li>
                    <i class="fa-brands fa-github"></i>
                    <a href="#about" >
                        Xer0503
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>