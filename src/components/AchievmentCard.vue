<template>
    <div class="wrapper">
        <div class="tile is-child box has-background-grey-dark">
            <div class="media">
                <article class="media-left">
                    <figure class="image is-128x128">
                        <img :src="require('../assets/achievs/' + event.image)" 
                        :alt="event.imgAlt">
                    </figure>
                    <div id="links" class="mt-2">
                        <a :href=event.link class="mr-1">
                            <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="#dddddd" class="bi bi-link-45deg" viewBox="0 0 16 16">
                                <path d="M4.715 6.542 3.343 7.914a3 3 0 1 0 4.243 4.243l1.828-1.829A3 3 0 0 0 8.586 5.5L8 6.086a1.002 1.002 0 0 0-.154.199 2 2 0 0 1 .861 3.337L6.88 11.45a2 2 0 1 1-2.83-2.83l.793-.792a4.018 4.018 0 0 1-.128-1.287z"/>
                                <path d="M6.586 4.672A3 3 0 0 0 7.414 9.5l.775-.776a2 2 0 0 1-.896-3.346L9.12 3.55a2 2 0 1 1 2.83 2.83l-.793.792c.112.42.155.855.128 1.287l1.372-1.372a3 3 0 1 0-4.243-4.243L6.586 4.672z"/>
                            </svg>
                        </a>
                    </div>
                </article>
                <div class="media-content has-text-left">
                    <div class="content has-text-white-ter">
                        <div class="content has-text-white-ter">
                            <p class="nickname">
                                <strong class="has-text-white-ter">{{event.title}}</strong> 
                            </p>
                        </div>
                        <div class="description_events">
                            <p class="has-text-white-ter">{{event.description}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            event: {
                type: Object,
                default: () => ({})
            }
        }
    }
</script>

<style>
    img {
        object-fit: cover;
        border-radius: 5px;
    }
    .description_events {
        line-height: 1.1;
        font-size: 30px;
    }
    .wrapper:last-child {
        grid-column-start: 1;
        grid-column-end: 3;
        justify-self: center;
    }
</style>