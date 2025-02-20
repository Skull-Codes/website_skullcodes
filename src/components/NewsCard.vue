<script setup>
    defineProps({
        news: Object,
    });
</script>

<template>
    <div class="new-card">
        <div class="left-side">
            <img :src="'/src/assets/' + news.image" :alt="news.title" />
            <small>{{news.date}}</small>
        </div>
        <div class="right-side">
            <h2>{{news.title}}</h2>
            <hr/>
            <p>{{news.description}}</p>
        </div>
    </div>
</template>

<style scoped>
    .new-card {
        border: 2px solid #101010;
        min-height: 200px;
        display: flex;
        flex-direction: row;
    }
        .left-side {
            width: 200px;
            display: flex;
            justify-content: flex-start;
            align-items: center;
            flex-direction: column;
            text-align: center;
        }
            .left-side img{
                width: 150px;
                margin-top: 15px;
            }

        .right-side {
            width: 75%;
            padding-right: 20px;
        }
            .right-side h2 {
                padding-top: 12px;
            }

    @media (max-width: 1024px) {
        .new-card {
            flex-direction: column;
        }

            .left-side, .right-side {
                width: 100%;
            }

            .right-side {
                padding: 15px;
            }
                .right-side h2 {
                    padding-top: 0px;
                }
    }
</style>