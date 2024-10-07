<script setup>


</script>

<template>

    <section class="coins container mx-auto mb-96">
        <div class="Section-title">
            <h2 class="text-center mx-auto mb-8 font-medium text-5xl text-neutral-300">
                COINS
            </h2>
            <p class="text-center mx-auto mb-24 font-medium text-medium text-neutral-300">
                Breakdown of our Coin Recipients.
            </p>
        </div>
        <div class="container flex mx-auto flex-row items-center justify-between">
            <div class="grid grid-cols-2 items-center gap-4 max-w-xl">
                <div class="distribution-item border-solid border-2 rounded-lg text-left px-8 py-3">
                    <h2 class="distribution-title text-xl mb-4">
                        Public Coin Sale 6.5M
                    </h2>
                    <p class="distribution-des max-w-64">
                        65% (To ensure maximal decentralization)
                    </p>
                </div>
                <div class="distribution-item border-solid border-2 rounded-lg text-left px-8 py-3 grid-column">
                    <h2 class="distribution-title text-xl mb-4">
                        Team Incentive 1.5M
                    </h2>
                    <p class="distribution-des max-w-64">
                        15% (Reward for building software)
                    </p>
                </div>
                <div class="distribution-item border-solid border-2 rounded-lg text-left px-8 py-3 grid-column">
                    <h2 class="distribution-title text-xl mb-4">
                        Marketing 1M
                    </h2>
                    <p class="distribution-des max-w-64">
                        10% (Advertising and promotional <br/>activities)
                    </p>
                </div>
                <div class="distribution-item border-solid border-2 rounded-lg text-left px-8 py-3 grid-column">
                    <h2 class="distribution-title text-xl mb-4">
                        Reserve Fund
                    </h2>
                    <p class="distribution-des max-w-64">
                        7% (To be burned after 36 <br/>months)
                    </p>
                </div>
                <div class="flex flex-row">
                    <div class="distribution-item border-solid border-2 rounded-lg text-left px-8 py-3 grid-column">
                    <h2 class="distribution-title text-xl mb-4">
                        Bug bounty
                    </h2>
                    <p class="distribution-des max-w-64">
                        3% (6 months lockup)
                    </p>
                </div>
                </div>
            </div>
            <!-- Interactive Pie Chart Section -->
            <div class="flex flex-col items-center mr-64">
                <div class="pie-chart">
                    <div class="slice slice-1" title="65% Public Coin Sale"></div>
                    <div class="slice slice-2" title="15% Team Incentive"></div>
                    <div class="slice slice-3" title="10% Marketing"></div>
                    <div class="slice slice-4" title="7% Reserve Fund"></div>
                    <div class="slice slice-5" title="3% Bug Bounty"></div>
                </div>
            </div>

            <div class="flex items-center">
                <div class="info-section grid grid-cols-2 gap-6 max-w-96">
                    <div class="info-box flex items-center px-3 py-3">
                        <div class="info-line purple"></div>
                        <div class="info-content flex flex-col">
                            <p class="info-title text-neutral-300">START TIME</p>
                            <p class="info-value font-semibold">July, 2023</p>
                        </div>
                    </div>
                    <div class="info-box flex items-center px-3 py-3">
                        <div class="info-line orange"></div>
                        <div class="info-content flex flex-col">
                            <p class="info-title text-neutral-300">COIN SYMBOL</p>
                            <p class="info-value font-semibold">IPI</p>
                        </div>
                    </div>
                    <div class="info-box flex items-center px-3 py-3">
                        <div class="info-line red"></div>
                        <div class="info-content flex flex-col">
                            <p class="info-title text-neutral-300">MINING START</p>
                            <p class="info-value font-semibold">1 January, 2025</p>
                        </div>
                    </div>
                    <div class="info-box flex items-center px-3 py-3">
                        <div class="info-line blue"></div>
                        <div class="info-content flex flex-col">
                            <p class="info-title text-neutral-300">COINS OFFERED</p>
                            <p class="info-value font-semibold">6.5M</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>

<style scoped>

.max-w-xl{
    max-width:600px;
}

/* Pie chart container */
.pie-chart {
    position: relative;
    width: 200px;
    height: 200px;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    transform: rotate(-90deg);
}

/* Base slice style */
.slice {
    position: absolute;
    width: 100%;
    height: 100%;
    clip-path: polygon(50% 50%, 100% 0, 100% 100%, 60% 100%);
    background-color: rgba(255, 255, 255, 0.1);
    transition: background-color 0.3s ease, transform 0.3s ease;
}

/* Visible part of the slice */
.slice::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    clip-path: polygon(50% 50%, 100% 0, 100% 100%, 50% 100%);
    background-color: inherit;
    transition: background-color 0.3s ease;
}

.slice-1 {
    background-color: #f5475d; /* Color for Public Coin Sale */
    transform: rotate(15deg); 
}

.slice-2 {
    background-color: #aa80ff; /* Color for Team Incentive */
    transform: rotate(40deg);
}

.slice-3 {
    background-color: #22a1f2; /* Color for Marketing */
    transform: rotate(255deg);
}

.slice-4 {
    background-color: #ffca28; /* Color for Reserve Fund */
    transform: rotate(180deg);
}

.slice-5 {
    background-color: #5f6d82; /* Color for Bug Bounty */
    transform: rotate(60deg);
}

.slice:hover::before {
    background-color: rgba(255, 0, 0, 1.0)
}

.grid-column{
    grid-column: 1/2;
}

.info-line {
    width: 4px;
    height: 100%;
    margin-right: 10px;
    border-radius: 2px;
}

.purple {
    background-color: #8e44ad;
}

.orange {
    background-color: #f39c12;
}

.red {
    background-color: #e74c3c;
}

.blue {
    background-color: #3498db;
}

</style>