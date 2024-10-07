<script setup>



</script>

<template>

    <section class="container mt-24 mx-auto px-8 flex justify-center gap-24 items-center">
        <div class="Contact-details mr-96">
            <div class="contact-section">
                <div class="rotating-circles">
                    <div class="circle circle-outer"></div>
                    <div class="circle circle-inner"></div>
                </div>
                <div class="contact-info flex flex-col py-24 px-24">
                    <p class="flex"><img src="https://placehold.co/20x20" alt="Email Icon"> <a href="/">hello@ipi.io</a></p>
                    <p class="flex"><img src="https://placehold.co/20x20" alt="Telegram Icon"> <a href="/">@ipicoin</a></p>
                </div>
            </div>
        </div>
        <div class="Form max-w-screen-sm">
            <h2 class="mb-8 text-gray-200 text-2xl font-medium">
                CONTACT US
            </h2>
            <p class="mb-12 text-gray-400 text-base font-medium">
                We are always open and we welcome and questions you have for our team. 
                If you wish to get in touch, please fill out the form below. Someone from our 
                team will get back to you shortly.
            </p>
            <form class="">
                <div class="top mb-10 flex gap-8">
                    <div class="Names">
                        <h4 class="text-gray-400 mb-3 ml-2 font-bold text-xs tracking-widest">
                            YOUR NAME
                        </h4>
                        <input type="text" placeholder="Input your name" class="border-solid border border-neutral-600  bg-transparent font-medium rounded-lg px-5 py-2">
                    </div>
                    <div class="Emails">
                        <h4 class="text-gray-400 mb-3 ml-2 font-bold text-xs tracking-widest">
                            YOUR E-MAIL
                        </h4>
                        <input type="email" placeholder="Input your E-mail" class="border-solid border border-neutral-600  bg-transparent font-medium rounded-lg px-5 py-2">
                    </div>
                </div>
                <div class="msg">
                    <div class="Bot">
                        <h4 class="text-gray-400 mb-2 ml-2 font-bold text-xs tracking-widest">
                            YOUR MESSAGE
                        </h4>
                        <input type="text" placeholder="Your message goes here" class="border-solid border border-neutral-600  bg-transparent font-medium rounded-lg px-5 py-2 h-28 w-full">
                    </div>
                </div>
                <div class="btn mt-8 flex flex-row-reverse">
                    <button type="submit" class="border-solid border-2 border-red-600 bg-red-600 text-gray-100 text-base font-medium rounded-3xl px-10 py-3">
                        SEND
                    </button>
                </div>
            </form>
        </div>
    </section>

</template>

<style scoped>

button:hover{
    background-color:aliceblue;
    border-color:aliceblue;
    color:#dc2626;
}

.max-w-screen-sm{
    max-width:560px;
}

.contact-section {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.rotating-circles {
  position: absolute;
  width: 300px;
  height: 300px;
}

.circle {
  border-radius: 50%;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.circle-outer {
  width: 100%;
  height: 100%;
  border: 2px solid transparent;
  border-top-color: white; /* Top section white */
  border-right-color: rgba(255, 255, 255, 0.2); /* Right section light white */
  border-bottom-color: rgba(255, 255, 255, 0.2); /* Bottom section light white */
  border-left-color: white; /* Left section white */
  animation: rotate 20s infinite linear;
}

.circle-inner {
  width: 70%;
  height: 70%;
  border: 2px solid transparent;
  border-top-color: white; /* Top section white */
  border-right-color: rgba(255, 255, 255, 0.2); /* Right section light white */
  border-bottom-color: rgba(255, 255, 255, 0.2); /* Bottom section light white */
  border-left-color: white; /* Left section white */
  animation: rotate-reverse 15s infinite linear;
}

@keyframes rotate {
  0% {
    transform: translate(-50%, -50%) rotate(0deg);
  }
  100% {
    transform: translate(-50%, -50%) rotate(360deg);
  }
}

@keyframes rotate-reverse {
  0% {
    transform: translate(-50%, -50%) rotate(0deg);
  }
  100% {
    transform: translate(-50%, -50%) rotate(-360deg);
  }
}

.contact-info {
  position: relative;
  text-align: center;
  z-index: 1;
}

.contact-info p {
  margin: 10px 0;
  font-size: 18px;
}

.contact-info img {
  vertical-align: middle;
  margin-right: 8px;
}

</style>