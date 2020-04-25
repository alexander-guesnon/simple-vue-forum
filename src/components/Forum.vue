<script>
    import db from '@/db/data.json'

    console.log(db)
    export default {
        name: 'Forum',
        data(){
            return{
            threads: db.threads,
                posts: db.posts,
                users: db.users,
                categories: db.categories,
                forums: db.forums,
                moderators:db.moderators,
                stats: db.stats
            }
        },
        computed: {

            title: function () {
                return this.$slots.default[0].text
            }
        }
    }
</script>
<template>
    <div class="hello">
        <h1>{{ title }}</h1>
        <div v-for="(thread, i) in threads" :key="`thread-${i}`">
            <h2>{{thread.title}}</h2>
            <div v-for="(postId, j) in thread.posts" :key="`post-${j}`">
                <p>{{users[posts[postId].userId].name}}</p>
                <p>{{posts[postId].text}}</p>
            </div>
        </div>
    </div>
</template>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
