<template>
    <span id="home"></span>
    <WeddingHeader></WeddingHeader>
    
    <!--img alt="Vue logo" src="./assets/logo.png" /-->

    <section class="start">
        <div class="box white branches">
            <h1> Namn & Namn </h1>
            <p>bjuder in till bröllop</p>
            <p>29 Juli - 31 Juli 2022</p>
        </div>
    </section>
    
    <section id="about">
        <div class="box white">

            <h1>Vi gifter oss!</h1>
            <p>Vårt bröllop kommer hållas på slottet Castello di Montalto i vackra Toscana, Italien. Tillsammans med er gäster vill vi spendera en underbar helg omgivna av vinodlingar och fantastiska vyer.</p>
            <p>Vigseln sker på lördagen den 30 juli, men bröllopsfirandet pågår under hela helgen. 
                Firandet inleds med att alla gäster checkar in på fredag eftermiddag för att sedan samlas för en gemensam middag. 
                Vi fortsätter med vigsel och bröllopsfest på lördagen och en härlig söndag som avslutas med en middag.</p>
            <p>Vi älskar också er barn men den här helgen vill vi bara fira tillsammans med er vuxna. Vi vet att det är lång hela vägen till Italien, därför kommer vi göra vårt bästa för att erbjuda en magisk helg med god mat, gemenskap och aktiviteter. Det här blir en semester att minnas!</p>
            <p>Vi önskar oss inga presenter då vår största glädje är att du kan och vill komma och fira med oss!</p>

        </div>
    </section>

    <section id="program">
        <div class="box white">
            <h1>Program</h1>
            <div style="display: flex;justify-content: space-between;">
                <div style="text-align: left">
                    <h4>Dag1</h4>
                    <i>Fredag 29 Juli</i>
                    <p>16:00 Checkin</p>
                    <p>17:00 Välkomstdrink</p>
                    <p>19:00 Middag</p>
                </div>
                <div style="text-align: left">
                    <h4>Dag2</h4>
                    <i>Lördag 30 Juli</i>
                    <p>9:00 Frukost</p>
                    <p>12:00 Vigsel</p>
                    <p>19:00 Middag</p>
                </div>
                <div style="text-align: left">
                    <h4>Dag3</h4>
                    <i>Söndag 31 Juli</i>
                    <p>09:00 Frukost</p>
                    <p>10:00 Poolparty</p>
                    <p>13:00 Lunch</p>
                </div>
                
            </div>
            <!--div>
                    <h4>Bröllopsdagen</h4>
                    <h5>Tidslinje</h5>

                </div-->
        </div>
        
    </section>

    <section class="green" id="accommodation" >
        <div class="box">
            <h1>Boende</h1>
            <p>Vi vill umgås med er så mycket som möjligt och därför kommer alla gäster att bo tillsammans med oss på slottet under hela helgen! 
                Vi har hela slottsområdet för oss själva från fredag till söndag.</p>
            <p>Kostnaden för boendet är x kr per person för hela vistelsen. Mat och dryck till alla måltider under hela helgen står vi för. Ni bokar boende genom oss</p>
            <p>Skulle det vara något ni funderar över så tveka inte att höra av er. Skicka din betalning senast 1 Juli.</p>
            <p>karta</p>
            <h1>Transport</h1>
            <p>Tips är att boka flyg så tidigt som möjligt!</p>
            <p>Närmaste flygplats : Peretolas, Florens. Närmaste tågstation: Siena</p>
            <p></p>
            <h3>Slottet</h3>
        
            <wedding-slider 
                :width="castle.width" 
                :height="castle.height"
                :images="castle.images"
            ></wedding-slider>

        </div>
        
    </section>

    <section class="white" id="clothing">
        <div class="widebox">
           
            <div class="widebox-content">
                <h2>Klädsel</h2>
                <p>Det kommer vara varmt, vi menar jättevarmt, så vi föreslår att kläderna ni bär är ljusa, lätta och är av ett material som släpper in luft. Under fredagen och söndagen är det helt fritt fram att ha på sig vad man vill, glöm inte att packa badkläder! Under lördagen, från ceremonin och framåt önskar vi att man klär upp sig extra fint – för nu är det fest!</p>
                <img src="./assets/branch.png" alt="" style="">
                <p>Vad innebär extra fint? Vi skippar shorts och håller oss till långbyxor och klänningar, inga krav finns på kavaj, slips, fluga etc. Vi kan rekommendera att inte ha stilettklackar då vi kommer gå på både grus och gräs.</p>
        
            </div>
            <div class="widebox-content">
               
                <wedding-slider 
                    :width="clothing.width" 
                    :height="clothing.height"
                    :images="clothing.images"
                ></wedding-slider>
        
            </div>
            
        </div>
        
    </section>

    <section>
        <div class="box white" id="osa">
            <h2>OSA</h2>
            <p>Senast imorgon, {{ tomorrow }}</p>
            <p>Skicka mejl till <a mailto="weregettingmarried@finally.com" style="cursor: pointer">weregettingmarried@finally.com</a></p>     
        </div>
        
    </section>
 
    <WeddingFooter>
        <a href="https://www.bluestripes.se"> Created by Blue Stripes </a>
        <a href='https://www.freepik.com/photos/background'>Background photo created by freepic.diller - www.freepik.com</a>
    </WeddingFooter>
</template>

<script setup>
import WeddingHeader from './components/WeddingHeader.vue'
import WeddingFooter from './components/WeddingFooter.vue'
import WeddingSlider from './components/WeddingSlider.vue'

import { defineProps, reactive } from 'vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md


</script>

<script>
export default {
    data() {
        return {
            castle: { 
                width: '550px',
                height: '350px',
                images:[
                    '/src/assets/slider/1.jpg',
                    '/src/assets/slider/2.jpg',
                    '/src/assets/slider/3.jpg',
                    '/src/assets/slider/4.jpg',
                    '/src/assets/slider/5.jpg',
                    '/src/assets/slider/6.jpg'
                ],
            },
            clothing : {
                width: '200px',
                height: '400px',
                images: [
                    '/src/assets/clothing/1.png',
                    '/src/assets/clothing/2.png',
                    '/src/assets/clothing/3.png',
                    '/src/assets/clothing/4.png',
                    '/src/assets/clothing/5.png',
                    '/src/assets/clothing/6.png',
                    '/src/assets/clothing/7.png',
                    '/src/assets/clothing/8.png',
                    '/src/assets/clothing/9.png',
                ]
            }
        }
    },

    computed : {
        tomorrow: function () {
            const today = new Date()
            const tomorrow = new Date(today)
            tomorrow.setDate(tomorrow.getDate() + 1)
            const dd = String(tomorrow.getDate()).padStart(2, '0');
            const mm = String(tomorrow.getMonth() + 1).padStart(2, '0'); //January is 0!
            const yyyy = tomorrow.getFullYear();
            return yyyy + '-' + mm + '-' + dd;
        }
    }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: silver;
  background-image: url("assets/italian-wedding.jpg");
  background-repeat: no-repeat;
  background-attachment: fixed;
  

}
html, body {
    margin: 0;  
}
a { color: var(--link-color); text-decoration: none;}
a:hover { color: var(--link-color-hover);}
:root {
    --header: 70px;
    --padding: 72px;
    --transparent: rgba(255,255,255,1);
    --link-color: #df98a8;
    --link-color-hover: #cc6777;
    --green: #5b7760;
    --white: #ffffff;
    --offwhite: #f8f8f8;
    --pink: #bb6975;
}

/* Page design */
section {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    
}

section.start {
    min-height: calc( 100vh - var(--header) - 50px);
}

section.green {
    background-color: var(--green);
    color: var(--white);
}

section.green a {
    color: var(--white);
}
section.green a:hover {
    color: var(--link-color);
}

section.white {
    background-color: var(--offwhite);
}

.box.branches {
    background-image: url(./assets/wedding-border-left.png), url(./assets/wedding-border-right.png);
    background-position: left top, right bottom;
    background-repeat: no-repeat, no-repeat;
    background-origin: 100px, 10px;
}

.box {
    width: 700px;
    border-radius: 10px;
    box-sizing: border-box;
    padding: var(--padding)
}

.box.white {
    background-color: var(--transparent);
}

.widebox {
    width: 1400px;
    box-sizing: border-box;
    padding: var(--padding);
    display: flex;
    flex-wrap: wrap;
}
.widebox-content {
        width: 50%;
}

footer a {
    background: var(--offwhite);
    padding: 2px;
    border-radius: 4px;
    margin: 0 2px; 
}

h1, h2, h3, h4, h5 {
    font-family: 'Tangerine', cursive;
    font-weight: 400;
    font-style: normal;
    line-height: 1;
    margin: 12px 0 24px 0;
}
h1 { font-size: 4rem;}
h2 { font-size: 3.5rem}
h3 { font-size: 3rem}
h4 { font-size: 2.5rem}
h5 { font-size: 2rem}

p {
    font-family: 'Open Sans', sans-serif;
}


</style>