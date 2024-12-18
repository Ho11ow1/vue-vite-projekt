<script setup lang="ts">
import { ref, onMounted } from 'vue';
import Button from 'primevue/button';

const roadmapContainer = ref<HTMLElement | null>(null);
const isDragging = ref(false);
const startX = ref(0);
const scrollLeft = ref(0);

const roadmap = ref([
    {
        quarter: 'Q4 2022',
        dateRange: 'Oct 2022 - Dec 2022',
        description: 'Collecting requirements, creating a business model, software documentationand creating a team of top developers.'
    },
    {
        quarter: 'Q1 2023',
        dateRange: 'Jan 2023 - Mar 2023',
        description: 'Starting IPI Mainnet, Requirement analysis, research and development, designing the architecture of the blockchain network and protocols.',
    },
    {
        quarter: 'Q2 2023',
        dateRange: 'Apr 2023 - Sep 2023',
        description: 'Development of multi-chain wallet and native scanner.Creating a smart contract engine.Private offering.'
    },
    {
        quarter: 'Q3 2024',
        dateRange: 'Oct 2023 - Sep 2024',
        description: 'Developing smart contract engine, developer tools, documentation, and basic building blocks'
    },
    {
        quarter: 'Q4 2024',
        dateRange: 'Oct 2024 - Dec 2024',
        description: 'Building a community of developers creating decentralized applications with us. Transitioning existing protocols.'
    },
    {
        quarter: 'Q1 2025 - till later',
        dateRange: 'Jan 2025 - till later',
        description: 'Start of public mining. Creating more of decentralized applications.'
    }
]);

// Function to handle scroll and update the line's color
const handleScroll = () => {
    const container = roadmapContainer.value;
    if (!container) return;

    // Get the scroll position and the total width
    const scrollLeft = container.scrollLeft;
    const scrollWidth = container.scrollWidth - container.clientWidth;

    // Calculate the scroll percentage (0 to 1)
    const scrollPercentage = scrollLeft / scrollWidth;

    // Set the CSS based on scroll percentage
    container.style.setProperty('--scroll-percentage', scrollPercentage.toString());
};

// Function to scroll left
const scrollLeftHandler = () => {
    if (roadmapContainer.value) 
    {
        const scrollAmount = roadmapContainer.value.children[0].clientWidth + 16; // Width of item + gap
        roadmapContainer.value.scrollBy({ left: -scrollAmount, behavior: 'smooth' });
    }
};

// Function to scroll right
const scrollRightHandler = () => {
    if (roadmapContainer.value) 
    {
        const scrollAmount = roadmapContainer.value.children[0].clientWidth + 16; // Width of item + gap
        roadmapContainer.value.scrollBy({ left: scrollAmount, behavior: 'smooth' });
    }
};

const startDragging = (e: MouseEvent) => {
    if (!roadmapContainer.value)
    {
        return;
    }    
    isDragging.value = true;
    roadmapContainer.value.classList.add('grabbing');
    startX.value = e.pageX - roadmapContainer.value.offsetLeft;
    scrollLeft.value = roadmapContainer.value.scrollLeft;
};

const stopDragging = () => {
    if (!roadmapContainer.value)
    {
        return;
    }    
    isDragging.value = false;
    roadmapContainer.value.classList.remove('grabbing');
};

const move = (e: MouseEvent) => {
    if (!isDragging.value || !roadmapContainer.value)
    {
        return;
    }    
    e.preventDefault();
    const x = e.pageX - roadmapContainer.value.offsetLeft;
    const walk = (x - startX.value); // Removed the multiplier for smoother scrolling
    roadmapContainer.value.scrollLeft = scrollLeft.value - walk;
};

onMounted(() => {
    if (roadmapContainer) 
    {
        handleScroll(); // Initial call to set the line color when the page loads
    }
});
</script>


<template>
    <section 
        class="roadmap hidden-el"
        id="roadmap"
        v-motion-slide-visible-once-bottom
    >
        <div class="Section-title">
            <h2 class="text-center mx-auto mb-8 font-medium text-5xl white">
                ROADMAP
            </h2>
            <p class="text-center mx-auto mb-24 font-medium text-medium blue">
                IPI is developing a global network platform for crypto ecosystem.
            </p>
        </div>
        <div class="roadmap-scroll-container ml-auto" ref="roadmapContainer" @scroll="handleScroll" @mousedown="startDragging" @mousemove="move" @mouseup="stopDragging">
            <div class="roadmap-item" v-for="(item, index) in roadmap" :key="index">
                <div class="item-circle"></div>
                <div class="item-content">
                    <div class="quarter white">{{ item.quarter }}</div>
                    <div class="date-range"><h2 class="text-center white">{{ item.dateRange }}</h2></div>
                    <div class="description"><p class="text-center blue">{{ item.description }}</p></div>
                </div>
            </div>
        </div>
        <div class="roadmap-controls mx-auto">
            <!-- <button @click="scrollLeft" class="scroll-button">←</button>
            <button @click="scrollRight" class="scroll-button">→</button> -->
            <Button @click="scrollLeftHandler" severity="secondary" outlined rounded icon="pi pi-chevron-left" class="px-2 py-2"/>
            <Button @click="scrollRightHandler" severity="secondary" outlined rounded icon="pi pi-chevron-right" class="px-2 py-2"/>
        </div>
    </section>
</template>

<style scoped>
.roadmap {
    padding: 2rem 1rem;
    overflow-x: hidden;
    mask-image: linear-gradient(to right, hsl(0 0% 0%) 0%, rgbahsl(0 0% hsla(0 0% 0% / 0.2) 0.2) 100%);
    margin-top: 6rem;
}

/* Controls for scrolling */
.roadmap-controls {
    display: flex;
    justify-content: center; /* Center the buttons */
    column-gap:1.5rem;
    margin-bottom: 1rem; /* Spacing below buttons */
}

/* .scroll-button {
    background-color: transparent;
    color: white;
    border:2px solid #fff;
    border-radius: 5px;
    padding: 0.5rem 1rem;
    margin: 0 0.5rem;
    cursor: pointer;
    transition: background-color 0.3s;
}

.scroll-button:hover {
    background-color: hsl(218 16.85% 34.9%);
} */

/* Scroll container for horizontal scrolling */
.roadmap-scroll-container {
    display: flex;
    gap: 16px;
    overflow-x: auto;
    padding-bottom: 10px;
    scrollbar-width: none;
    scroll-behavior: smooth;
    -webkit-overflow-scrolling: touch;
    cursor: grab;
    user-select: none;
    position: relative;
    padding-top: 2rem;
    max-width:1640px;
    scroll-snap-type: x proximity;
    transition: all 0.3s ease-out;
}

.roadmap-scroll-container.grabbing {
    cursor: grabbing;
}

.roadmap-scroll-container::before {
    content: '';
    position: absolute;
    top: 50px;
    left: 0;
    width: calc(100vw + 25%); /* Ensure the line spans the full width of the container */
    height: 3px;
    /*controlled by scroll */
    background: linear-gradient(to right, hsl(218 16.85% 34.9%) 0%, hsl(0 72.22% 50.59%) calc(var(--scroll-percentage, 0%) * 100%), #4a5568 100%);
    z-index: 0;
    transition: background 0.3s ease-in-out;
}

@media (max-width:1600px)
{
    .roadmap-scroll-container::before {
        width: calc(120vw + 25%); /* Ensure the line spans the full width of the container */
    }
}
@media (max-width:1248px)
{
    .roadmap-scroll-container::before {
        width: calc(160vw + 25%); /* Ensure the line spans the full width of the container */
    }
}
@media (max-width:960px)
{
    .roadmap-scroll-container::before {
        width: calc(180vw + 45%); /* Ensure the line spans the full width of the container */
    }
}

/* Each roadmap item */
.roadmap-item {
    flex-shrink: 0;
    max-width:320px;
    position: relative;
    padding-top: 2rem;
    z-index: 1; /* Ensure items stay above the line */
    scroll-snap-align: start;
}

/* The circles go brr */
.item-circle {
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translateX(-50%);
    width: 20px;
    height: 20px;
    background-color:hsl(0 72.22% 50.59%);
    border-radius: 50%;
    z-index: 2; /* Ensure the circle is above the line */
    border: 2px solid #fff;
}

.item-content {
    padding: 1.5rem;
    border-radius: 8px;
    color: #ffffff;
    margin-top: 20px;
}

/*QX - year*/
.quarter {
    font-size: .95rem;
    font-weight: bold;
    margin-bottom: 0.5rem;
    text-align: center;
    position: absolute;
    top: -2rem; /* Move the text above the line */
    left: 50%;
    transform: translateX(-50%);
    white-space: nowrap; /* Ensure the text stays inline */
}

/* The date */
.date-range {
    font-size: 1.1rem;
    font-weight:600;
    color: hsl(211.43 25.3% 83.73%);
    margin-bottom: 1rem;
}

.description {
    font-size: 1rem;
    font-weight: 500;
    line-height: 1.4;
}

@media (max-width: 768px) {
    .roadmap-item {
        width: 250px;
    }

    .item-content {
        padding: 1rem;
    }

    .quarter {
        font-size: 1.1rem;
    }

    .description {
        font-size: 0.95rem;
    }
}

@media (max-width: 560px) {
    .roadmap-item {
        width: 200px;
    }

    .quarter {
        font-size: 1rem;
    }

    .description {
        font-size: 0.85rem;
    }
}
</style>
