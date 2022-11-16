<template>
    <div class="wrapper">
        <div class="tile is-child box">
            <div class="media">
                <article class="media-left">
                    <figure class="image is-128x128">
                        <img :src="require('../assets/achievs/' + event.image)" 
                        :alt="event.imgAlt">
                    </figure>
                </article>
                <div class="media-content has-text-left">
                    <div class="content">
                        <div class="content">
                            <a :href=event.link class="hoverable-link has-text-white-ter nickname">
                                <strong>{{event.title}}</strong>
                            </a>
                        </div>
                        <div class="event-format description_events mb-3">
                            <p class="mx-1 has-text-white-ter">{{event.format}}</p>
                        </div>
                        <div class="description_events mb-3">
                            <p class="has-text-grey-lighter">{{event.description}}</p>
                        </div>
                        <div class="description_events has-text-white-ter">
                            <p>
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-calendar3 mr-2" >
                                    <path d="M14 0H2a2 2 0 0 0-2 2v12a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V2a2 2 0 0 0-2-2zM1 3.857C1 3.384 1.448 3 2 3h12c.552 0 1 .384 1 .857v10.286c0 .473-.448.857-1 .857H2c-.552 0-1-.384-1-.857V3.857z"/>
                                    <path d="M6.5 7a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm-9 3a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2zm3 0a1 1 0 1 0 0-2 1 1 0 0 0 0 2z"/>
                                </svg>{{event.date}}
                            </p>
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

<style scoped>
    .content {
      margin: 0 !important;  
    }
    .event-format{
        border: 2px solid #33614a;
        width: max-content;
        border-radius: 8px;
        background-color: #33614a;
    }
</style>