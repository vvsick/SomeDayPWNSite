<template>
        <div class="box">
            <div class="media">
                <article class="media-left">
                    <figure class="image is-128x128 is-flex">
                        <img :src="require('../assets/fotki/' + participant.image)" 
                        :alt="participant.imageAlt">
                    </figure>
                    <div id="links" class="mt-2">
                        <a :href=participant.gitLink class="mr-1 hoverable-link icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="" class="bi bi-github" viewBox="0 0 16 16">
                                <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"/>
                            </svg>
                        </a>
                        <a :href=participant.vkLink class="mr-1 hoverable-link icon">
                            <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="" viewBox="0 0 448 512">
                                <path d="M31.4907 63.4907C0 94.9813 0 145.671 0 247.04V264.96C0 366.329 0 417.019 31.4907 448.509C62.9813 480 113.671 480 215.04 480H232.96C334.329 480 385.019 480 416.509 448.509C448 417.019 448 366.329 448 264.96V247.04C448 145.671 448 94.9813 416.509 63.4907C385.019 32 334.329 32 232.96 32H215.04C113.671 32 62.9813 32 31.4907 63.4907ZM75.6 168.267H126.747C128.427 253.76 166.133 289.973 196 297.44V168.267H244.16V242C273.653 238.827 304.64 205.227 315.093 168.267H363.253C359.313 187.435 351.46 205.583 340.186 221.579C328.913 237.574 314.461 251.071 297.733 261.227C316.41 270.499 332.907 283.63 346.132 299.751C359.357 315.873 369.01 334.618 374.453 354.747H321.44C316.555 337.262 306.614 321.61 292.865 309.754C279.117 297.899 262.173 290.368 244.16 288.107V354.747H238.373C136.267 354.747 78.0267 284.747 75.6 168.267Z"/>
                            </svg>
                        </a>
                        <a class="hoverable-link icon" :href=participant.telegramLink>
                            <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="" class="bi bi-telegram" viewBox="0 0 16 16">
                                <path d="M16 8A8 8 0 1 1 0 8a8 8 0 0 1 16 0zM8.287 5.906c-.778.324-2.334.994-4.666 2.01-.378.15-.577.298-.595.442-.03.243.275.339.69.47l.175.055c.408.133.958.288 1.243.294.26.006.549-.1.868-.32 2.179-1.471 3.304-2.214 3.374-2.23.05-.012.12-.026.166.016.047.041.042.12.037.141-.03.129-1.227 1.241-1.846 1.817-.193.18-.33.307-.358.336a8.154 8.154 0 0 1-.188.186c-.38.366-.664.64.015 1.088.327.216.589.393.85.571.284.194.568.387.936.629.093.06.183.125.27.187.331.236.63.448.997.414.214-.02.435-.22.547-.82.265-1.417.786-4.486.906-5.751a1.426 1.426 0 0 0-.013-.315.337.337 0 0 0-.114-.217.526.526 0 0 0-.31-.093c-.3.005-.763.166-2.984 1.09z"/>
                            </svg>
                        </a>
                    </div>
                </article>
                <div class="media-content has-text-left">
                    <div class="content">
                        <p class="nickname mr-2"> <strong class="has-text-white-ter">{{participant.nickname}}</strong> </p>
                        <div class="participant-skills has-text-white-ter mr-2" 
                        v-for="(skill, index) in participant.skills"
                        :key="index"
                        >
                            <p class="mx-1">{{skill}}</p>
                        </div>
                    </div>
                    <div class="description">
                        <p class="has-text-grey-lighter">{{participant.ruDescription}}</p>
                        <p class="has-text-grey-lighter pt-1">{{participant.enDescription}}</p>
                    </div>
                </div>
            </div>
        </div>
</template>

<script>
    export default {
        props: {
            participant: {
                type: Object,
                default: () => ({})
            }
        },
    }
</script>

<style scoped>
    .participant-skills {
        display: inline-block;
        border: 2px solid #33614a;
        width: max-content;
        border-radius: 8px;
        background-color: #33614a;
    }
    .nickname {
        display: inline-block;
        margin-bottom: 0 !important;
    }
</style>