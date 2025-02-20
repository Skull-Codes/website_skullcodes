<script setup>
    defineProps({
        project: Object,
    });
</script>

<template>
    <div class="card">
        <div class="card-header">
            <img :src="'/src/assets/project_logos/' + project.logo" :alt="project.name" />
        </div> 
        <h3>{{project.name}}</h3>
        <ul>
            <li>Lenguaje: {{project.language}}</li>
            <li>Framework: {{project.framework}}</li>
            <li>Arquitectura: {{project.architecture}}</li>
            <li>Motor base de datos: {{project.database}}</li>
        </ul>

        <div class="card-footer">
            <img src="/src/assets/gitlab-logo.png" alt="gitlab">
            <div class="card-links">
                <a :href="project.gitlab_repo" target="_blank">Repo</a>
                <a :href="project.gitlab_wiki" target="_blank">Wiki</a>
            </div>

            <img src="/src/assets/github-logo.png" alt="github">
            <div class="card-links">
                <a :href="project.github_repo" target="_blank">Repo</a>
                <a :href="project.github_wiki" target="_blank">Wiki</a>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .card {
        border: 2px solid blue;
        border-radius: 15px;
        width: 300px;
        min-height: 630px;
        margin: 20px;
        overflow: hidden;
        box-shadow: 2px 2px 10px black;
        background:rgb(35, 35, 35);
    }
        .card h3{
            text-align: center;
            margin-bottom: 10px;
        }
        .card-header{
            border-radius: 150px;
            box-shadow: 5px 5px 10px black;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 15px;
        }
            .card-header img{
                width: 275px;
            }

        .card-footer {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            border-top: 2px solid blue;
            margin: 10px;
            padding-top: 15px;
        }
            .card-footer img{
                height: 50px;
            }
            .card-footer a{
                padding: 5px 15px;
            }
</style>