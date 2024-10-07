<script setup>



</script>

<template>

<section class="section mt-32 mb-96" id="advantages">
            <div id="dev-table" style="display: none;">
              <div class="comparison-table-wrapper">
                <table class="comparison-table">
                  <thead>
                  <tr>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="IPI" title="IPI"></div>
                      <div class="name">IPI</div>
                      <div class="symbol">IPI</div>
                      <div class="score"><span style="width: 100.0%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="BTC" title="Bitcoin (BTC)"></div>
                      <div class="name">Bitcoin (BTC)</div>
                      <div class="symbol">BTC</div>
                      <div class="score"><span style="width: 0.0%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="ETH" title="Ethereum (ETH)"></div>
                      <div class="name">Ethereum (ETH)</div>
                      <div class="symbol">ETH</div>
                      <div class="score"><span style="width: 13.3%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="BNB" title="Binance Smart Chain (BNB)"></div>
                      <div class="name">Binance Smart Chain (BNB)</div>
                      <div class="symbol">BNB</div>
                      <div class="score"><span style="width: 20.0%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="XRP" title="Ripple (XRP)"></div>
                      <div class="name">Ripple (XRP)</div>
                      <div class="symbol">XRP</div>
                      <div class="score"><span style="width: 6.7%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="ADA" title="Cardano (ADA)"></div>
                      <div class="name">Cardano (ADA)</div>
                      <div class="symbol">ADA</div>
                      <div class="score"><span style="width: 6.7%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="SOL" title="Solana (SOL)"></div>
                      <div class="name">Solana (SOL)</div>
                      <div class="symbol">SOL</div>
                      <div class="score"><span style="width: 40.0%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="TRX" title="Tron (TRX)"></div>
                      <div class="name">Tron (TRX)</div>
                      <div class="symbol">TRX</div>
                      <div class="score"><span style="width: 6.7%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="DOT" title="Polkadot (DOT)"></div>
                      <div class="name">Polkadot (DOT)</div>
                      <div class="symbol">DOT</div>
                      <div class="score"><span style="width: 20.0%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="ALGO" title="Algorand (ALGO)"></div>
                      <div class="name">Algorand (ALGO)</div>
                      <div class="symbol">ALGO</div>
                      <div class="score"><span style="width: 53.3%"></span></div>
                    </th>
                  </tr>
                  </thead>
                  <tbody>
                  <tr>
                    <th colspan="10">Consensus / Decentralization Level</th>
                  </tr>
                  <tr>
                    <td class="plus2"> Proof of Network / Very High</td>
                    <td class="plus2"> Proof of Work / Very High</td>
                    <td class="plus1"> Proof of Stake / High with censorship*</td>
                    <td class="minus1"> Proof of Authority / Moderate</td>
                    <td class="minus1"> XRP Ledger Consensus Protocol (XRP LCP) / Low</td>
                    <td class="plus1"> Ouroboros Praos (Proof of Stake) / High</td>
                    <td class="minus1"> Proof of History (PoH) &amp; Tower BFT (Finality) / Moderate</td>
                    <td class="minus1"> Delegated Proof-of-Stake (DPoS) / Moderate</td>
                    <td class="plus1"> BABE (Block Proposal) &amp; GRANDPA (Finality) / High</td>
                    <td class="plus2"> Pure Proof of Stake / Very High</td>
                  </tr>
                  <tr>
                    <th colspan="10">TPS** Range</th>
                  </tr>
                  <tr>
                    <td class="plus2">96k-123k</td>
                    <td class="minus1">4-7</td>
                    <td class="minus1">15-45</td>
                    <td class="minus1">100-200 (on-chain)</td>
                    <td class="mid">1500</td>
                    <td class="minus1">200-250</td>
                    <td class="plus2">50k-65k</td>
                    <td class="mid">700-2000</td>
                    <td class="mid">1k-2k</td>
                    <td class="plus2"> 1k-46k</td>
                  </tr>
                  <tr>
                    <th colspan="10">Smart Contracts/Speed</th>
                  </tr>
                  <tr>
                    <td class="plus2">Yes, fastest</td>
                    <td class="minus1">No</td>
                    <td class="plus1">Yes</td>
                    <td class="plus1">Yes, fast</td>
                    <td class="minus1">No</td>
                    <td class="plus1">Yes</td>
                    <td class="plus1">Yes,fast</td>
                    <td class="plus1">Yes</td>
                    <td class="plus1">Yes</td>
                    <td class="plus1"> Yes , fast</td>
                  </tr>
                  <tr>
                    <th colspan="10">Smart Contract Language</th>
                  </tr>
                  <tr>
                    <td class="plus2">AssemblyScript (TypeScript Dialect), Rust, Go, Python, C, C++</td>
                    <td class="minus1">N/A</td>
                    <td class="mid"> Solidity</td>
                    <td class="mid">Solidity</td>
                    <td class="minus1">N/A</td>
                    <td class="minus1"> Plutus</td>
                    <td class="mid">Rust</td>
                    <td class="mid">Solidity</td>
                    <td class="minus1"> Ink! (Rust-based)</td>
                    <td class="minus1"> TEAL</td>
                  </tr>
                  <tr>
                    <th colspan="10">No-Code Smart Contracts with AI</th>
                  </tr>
                  <tr>
                    <td class="plus2">Yes</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1"> No</td>
                  </tr>
                  <tr>
                    <th colspan="10">Approx. Finality Time</th>
                  </tr>
                  <tr>
                    <td class="plus2">2.5-4.5 seconds</td>
                    <td class="minus1">60 minutes (6 confirmations)</td>
                    <td class="minus1"> ~6 minutes (12-32 slots for finality)</td>
                    <td class="plus2">~5 seconds</td>
                    <td class="plus2">~3-5 seconds</td>
                    <td class="minus1">~20 minutes</td>
                    <td class="plus2">~0.4 seconds</td>
                    <td class="minus1"> Every 6 hours (27 Super Representatives rotate)</td>
                    <td class="mid"> ~2 minutes</td>
                    <td class="plus2"> 2.5-4.5 seconds</td>
                  </tr>
                  </tbody>
                </table>
                <p>* - according to <a href="https://www.mevwatch.info/">https://www.mevwatch.info/</a> </p>
                <p>** - Transactions Per Second (TPS) is highly dependent on the specific implementation and network conditions, and these numbers are rough estimates only.</p>
              </div>
            </div>
            <div id="inv-table" style="display: block;">
              <div class="comparison-table-wrapper">
                <table class="comparison-table">
                  <thead>
                  <tr>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="IPI" title="IPI"></div>
                      <div class="name">IPI</div>
                      <div class="symbol">IPI</div>
                      <div class="score"><span style="width: 100.0%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="BTC" title="Bitcoin (BTC)"></div>
                      <div class="name">Bitcoin (BTC)</div>
                      <div class="symbol">BTC</div>
                      <div class="score"><span style="width: 64.3%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="ETH" title="Ethereum (ETH)"></div>
                      <div class="name">Ethereum (ETH)</div>
                      <div class="symbol">ETH</div>
                      <div class="score"><span style="width: 14.3%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="BNB" title="Binance Smart Chain (BNB)"></div>
                      <div class="name">Binance Smart Chain (BNB)</div>
                      <div class="symbol">BNB</div>
                      <div class="score"><span style="width: 14.3%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="XRP" title="Ripple (XRP)"></div>
                      <div class="name">Ripple (XRP)</div>
                      <div class="symbol">XRP</div>
                      <div class="score"><span style="width: 0.0%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="ADA" title="Cardano (ADA)"></div>
                      <div class="name">Cardano (ADA)</div>
                      <div class="symbol">ADA</div>
                      <div class="score"><span style="width: 28.6%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="SOL" title="Solana (SOL)"></div>
                      <div class="name">Solana (SOL)</div>
                      <div class="symbol">SOL</div>
                      <div class="score"><span style="width: 21.4%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="TRX" title="Tron (TRX)"></div>
                      <div class="name">Tron (TRX)</div>
                      <div class="symbol">TRX</div>
                      <div class="score"><span style="width: 14.3%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="DOT" title="Polkadot (DOT)"></div>
                      <div class="name">Polkadot (DOT)</div>
                      <div class="symbol">DOT</div>
                      <div class="score"><span style="width: 28.6%"></span></div>
                    </th>
                    <th>
                      <div class="icon-wrapper"><img src="../assets/vue.svg" alt="ALGO" title="Algorand (ALGO)"></div>
                      <div class="name">Algorand (ALGO)</div>
                      <div class="symbol">ALGO</div>
                      <div class="score"><span style="width: 35.7%"></span></div>
                    </th>
                  </tr>
                  </thead>
                  <tbody>
                  <tr>
                    <th colspan="10">Consensus / Decentralization Level</th>
                  </tr>
                  <tr>
                    <td class="plus2"> Proof of Network / Very High</td>
                    <td class="plus2"> Proof of Work / Very High</td>
                    <td class="plus1"> Proof of Stake / High with censorship*</td>
                    <td class="minus1"> Proof of Authority / Moderate</td>
                    <td class="minus1"> XRP Ledger Consensus Protocol (XRP LCP) / Low</td>
                    <td class="plus1"> Ouroboros Praos (Proof of Stake) / High</td>
                    <td class="minus1"> Proof of History (PoH) &amp; Tower BFT (Finality) / Moderate</td>
                    <td class="minus1"> Delegated Proof-of-Stake (DPoS) / Moderate</td>
                    <td class="plus1"> BABE (Block Proposal) &amp;GRANDPA (Finality) / High</td>
                    <td class="plus2"> Pure Proof of Stake / Very High</td>
                  </tr>
                  <tr>
                    <th colspan="10">Max Supply</th>
                  </tr>
                  <tr>
                    <td class="plus2"> 100M</td>
                    <td class="plus2"> 21M</td>
                    <td class="minus1">∞</td>
                    <td class="plus1">200M</td>
                    <td class="minus1">100B</td>
                    <td class="minus1">45B</td>
                    <td class="minus1">∞</td>
                    <td class="minus1">∞</td>
                    <td class="minus1">∞</td>
                    <td class="minus1">10B</td>
                  </tr>
                  <tr>
                    <th colspan="10">Instamine</th>
                  </tr>
                  <tr>
                    <td class="plus2"> 0**</td>
                    <td class="plus2"> 0</td>
                    <td class="mid"> 72M</td>
                    <td class="minus1">200M</td>
                    <td class="minus1">100B</td>
                    <td class="minus1">45B</td>
                    <td class="mid">500K</td>
                    <td class="minus1">100B</td>
                    <td class="minus1">Yes</td>
                    <td class="minus1">2.5B</td>
                  </tr>
                  <tr>
                    <th colspan="10">Halving/Period</th>
                  </tr>
                  <tr>
                    <td class="plus2"> Yes/~4Y</td>
                    <td class="plus2"> Yes/~4Y</td>
                    <td class="minus1"> No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1"> No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                    <td class="minus1">No</td>
                  </tr>
                  <tr>
                    <th colspan="10">Network Speed/Gas price</th>
                  </tr>
                  <tr>
                    <td class="plus2"> Very fast/Very cheap</td>
                    <td class="minus1"> Very Slow/Regular</td>
                    <td class="minus1">Fast/Expensive</td>
                    <td class="plus2">Fast/Cheap</td>
                    <td class="plus2">Fast/Cheap</td>
                    <td class="plus2">Fast/Cheap</td>
                    <td class="plus2">Fast/Cheap</td>
                    <td class="plus2">Fast/Cheap</td>
                    <td class="plus2">Fast/Cheap</td>
                    <td class="plus2">Fast/Cheap</td>
                  </tr>
                  <tr>
                    <th colspan="10">Native Wallet &amp; Scanner</th>
                  </tr>
                  <tr>
                    <td class="plus2"> Yes</td>
                    <td class="mid">Wallet only</td>
                    <td class="plus2"> Yes</td>
                    <td class="mid">Scanner only</td>
                    <td class="mid">Scanner only</td>
                    <td class="plus2"> Yes</td>
                    <td class="plus2"> Yes</td>
                    <td class="plus2"> Yes</td>
                    <td class="plus2"> Yes</td>
                    <td class="plus2"> Yes</td>
                  </tr>
                  </tbody>
                </table>
                <p>* - according to <a href="https://www.mevwatch.info/">https://www.mevwatch.info/</a></p>
                <p>** -- First IPI is mined from staking 1 BTC to avoid SEC investigation </p>
              </div>
            </div>
          </section>

</template>

<style scoped>

.comparison-table-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    width: 100%;
    box-sizing: border-box;
    padding-left: 1em;
    padding-right: 1em;
}

.comparison-table {
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 20px;
    width: 100%;
    border-collapse: collapse;
    border-spacing: 0;
    margin-bottom: 1rem;
    margin-top: 1rem;
    color: #eef3fc;
    overflow: hidden;
    margin: 2em 2rem;
    max-width: 1140px;
}

.comparison-table thead th {
    width: 10%;
    font-size: 0.8em;
    padding-bottom: 1em;
}

th {
    text-align: inherit;
}

.comparison-table thead th .icon-wrapper {
    height: 2px;
    margin-top: 5em;
    margin-bottom: 3em;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}

.comparison-table thead th .icon-wrapper img {
    position: absolute;
    /* transform: scale(0.4); */
    max-width: 40%;
}

.comparison-table thead .name {
    height: 4em;
    text-align: center;
    font-weight: 400;
}

.comparison-table thead th .symbol {
    display: none;
}

.comparison-table thead .score {
    height: 4px;
    background: #7fa3cdff;
    position: relative;
    margin-left: 2em;
    margin-right: 2em;
}

.comparison-table tbody tr:nth-child(4n+1), .comparison-table tbody tr:nth-child(4n+2) {
    background-color: #202B47;
}

.comparison-table tbody th {
    text-align: center;
    padding-top: 0.7em;
    padding-bottom: 0.7em;
}

.comparison-table tbody tr:nth-child(4n+1), .comparison-table tbody tr:nth-child(4n+2) {
    background-color: #202B47;
}

.comparison-table tbody td {
    vertical-align: top;
    font-size: 0.7em;
}

.comparison-table td {
    text-align: center;
    padding: 0.5rem 1rem;
}

.comparison-table td:before {
    display: block;
    content: ' ';
    background-repeat: no-repeat;
    background-size: contain;
    background-position: 50% 50%;
    height: 2.3em;
    margin-bottom: 1em;
}

.comparison-table td.minus1:before {
    background-image: url(../assets/minus.svg);
}
.comparison-table td.mid:before {
    background-image: url(../assets/mid.svg);
}
.comparison-table td.plus2:before {
    background-image: url(../assets/plus2.svg);
}
.comparison-table td.plus1:before {
    background-image: url(../assets/plus.svg);
}

</style>