<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue';
import { RiTelegramFill } from "@remixicon/vue";
import { RiMailLine } from "@remixicon/vue";

import Textarea from 'primevue/textarea';
const value2 = ref('');
const nameInput = ref('');
const emailInput = ref('');

import Button from 'primevue/button'; 
const loading = ref(false);

const load = () => {
    loading.value = true;
    setTimeout(() => {
        loading.value = false;
        // Clear all input fields
        value2.value = '';  // Clear textarea
        nameInput.value = ''; // Clear name input
        emailInput.value = ''; // Clear email input
        
        // Clear native input fields
        const inputs = document.querySelectorAll('input');
        inputs.forEach(input => {
            input.value = '';
        });
    }, 2000);
};

// let Visible = ref(true);

// let Observer: IntersectionObserver | null = null;

// onMounted(() => 
// {
// 	Observer = new IntersectionObserver((entries) => 
// 	{
// 		entries.forEach(entry => 
// 		{
// 			Visible.value = entry.isIntersecting;
// 		});
// 	});

// 	const target = document.getElementById('contact');
// 	if (target) 
// 	{
// 		Observer.observe(target);
// 	}
// });

// onUnmounted(() => 
// {
// 	if (Observer)
// 	{
// 		Observer.disconnect();
// 	}
// })

</script>

<template>
	<section 
		class="container mx-auto px-8 mb-56 mt-96 flex justify-center items-center hidden-el animate" 
		id="contact" 
		v-motion-slide-visible-once-bottom
	>
		<div class="Contact-details mr-14">
			<div class="contact-section">
				<div class="rotating-circles">
					<div class="circle circle-outer"></div>
					<div class="circle circle-inner"></div>
				</div>
				<div class="contact-info flex flex-col py-24 px-24">
					<a href="mailto:hello@ipi.io" class="flex items-center gap-2">
						<RiMailLine style="width:30px; height:30px;"> </RiMailLine>
						<p class="">
							hello@ipi.io
						</p>
					</a>
					<a href="https://t.me/@ipicoin" class="flex items-center gap-2">
						<RiTelegramFill style="width:30px; height:30px;"> </RiTelegramFill>
						<p class="">
							@ipicoin
						</p>
					</a>
				</div>
			</div>
		</div>
		<div class="Form max-w-screen-sm">
			<div class="Form-top">
				<h2 class="mb-8 text-2xl font-semibold white">
					CONTACT US
				</h2>
				<p class="mb-12 text-base font-medium dark-blue">
					We are always open and we welcome and questions you have for our team. 
					If you wish to get in touch, please fill out the form below. Someone from our 
					team will get back to you shortly.
				</p>
			</div>
			<form>
				<div class="flex flex-col md:flex-row gap-8 mb-10">
					<div class="Names w-full md:w-1/2 max-w-[260px]">
						<h4 class="mb-3 font-bold text-xs tracking-widest blue">
							YOUR NAME
						</h4>
						<input 
							type="text" 
							v-model="nameInput"
							placeholder="Input your name" 
							class="w-full border-solid border border-neutral-600 bg-transparent font-medium rounded-lg px-5 py-2 white"
						>
					</div>
					<div class="Emails w-full md:w-1/2 max-w-[260px]">
						<h4 class="mb-3 font-bold text-xs tracking-widest blue">
							YOUR E-MAIL
						</h4>
						<input 
							type="email" 
							v-model="emailInput"
							placeholder="Input your E-mail" 
							class="w-full border-solid border border-neutral-600 bg-transparent font-medium rounded-lg px-5 py-2"
						>
					</div>
				</div>
				<div class="msg">
					<div class="Bot">
						<h4 class="mb-2 font-bold text-xs tracking-widest blue">
							YOUR MESSAGE
						</h4>
						<Textarea 
							id="over_label" 
							placeholder="Your message goes here" 
							v-model="value2" 
							rows="5" 
							cols="58" 
							autoResize 
							class="w-full"
						/>
					</div>
				</div>
				<div class="btn mt-8">
					<Button 
						type="button" 
						label="Submit" 
						icon="pi pi-send" 
						:loading="loading" 
						@click="load" 
						rounded 
						class="ml-auto"
					/>
				</div>
			</form>
		</div>
	</section>
</template>

<style scoped>

Button {
    background-color: hsl(0, 85%, 60%); 
    border-color: hsl(0, 85%, 60%);
	color: hsl(20, 100%, 100%);
}

Button:hover {
    background-color: hsl(195, 85%, 60%) !important; 
    border-color: hsl(195, 85%, 60%) !important;
    color: hsl(20, 100%, 100%) !important;
}

@media (min-width:768px)
{
	section{
		gap:16rem;
	}
}

.p-textarea{
	background-color:transparent;
}

/* button:hover{
	background-color:aliceblue;
	border-color:aliceblue;
	color:#dc2626;
} */

.p-button{
	padding:1rem 1.5rem;
}

.max-w-screen-sm{
	max-width:560px;
}

.contact-section {
	position: relative;
	display: flex;
	justify-content: center;
	align-items: center;
}

.rotating-circles {
	position: absolute;
	width: 350px;
	height: 350px;
	/* background-image:url(/dot-c-azalea.png);
	background-position-x:19%;
	background-position-y:12%;
	background-repeat:no-repeat; */
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

.Names > input,
.Emails > input{
	max-width:260px;
}

@media (max-width:1024px)
{
	section{
		max-width:1024px;
		padding-bottom:8rem;
		gap:3rem;
	}
	.Contact-details{
		margin-right:20px;
	}
	.Form{
		max-width:480px;
	}
	input{
		padding-right:0;
	}
	.Names > input,
	.Emails > input{
		max-width:240px;
	}
}

@media (max-width:940px)
{
	section{
		flex-wrap:wrap-reverse
	}
	.Form{
		max-width:100%;
		width:100%;
	}
	.top{
		justify-content:space-between;
	}
}

.Form {
	width: 100%;
}

.Names input,
.Emails input {
	width: 100%;
	max-width: 260px;
}

.btn {
	display: flex;
	justify-content: flex-end;
}

@media (max-width: 768px) {
	.Names input,
	.Emails input {
		max-width: 100%;
	}

	.Form {
		padding: 0 1rem;
	}
}

.Names,
.Emails {
    flex: 1;
    min-width: 0; /* This prevents flex items from overflowing */
}

.Names input,
.Emails input {
    width: 100%;
}

@media (max-width: 768px) {
    .flex.flex-row {
        gap: 4px; /* Reduce gap on mobile */
    }
    
    .Names,
    .Emails {
        width: 50%;
    }
}

</style>