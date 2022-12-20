<template>
    <div id="content" class="site-content">
        <div id="blog-wrapper">
            <div class="blog-holder center-relative">
                <article class="blog-item-holder featured-post">
                    <div class="entry-content relative">
                        <div class="content-1170 center-relative">
                            <div class="cat-links">
                                <ul>
                                    <li>
                                        <a href="#">Crafting</a>
                                    </li>
                                </ul>
                            </div>
                            <div class="entry-date published">February 12, 2016</div>
                            <h2 class="entry-title">
                                <a href="single.html">Whatever is begun in anger ends in shame</a>
                            </h2>
                            <div class="excerpt">
                                Now when I had mastered the language of this water and had come to know every trifling
                                feature that bordered the great river as familiarly as I knew the letters of the
                                alphabet, I had made a valuable acquisition. I still keep in mind a certain wonderful
                                sunset which I witnessed when and steamboating<a class="read-more"
                                    href="single.html"></a>
                            </div>
                            <div class="clear"></div>
                        </div>
                    </div>
                </article>
                <article class="blog-item-holder" v-for="post in posts">
                    <div class="entry-content relative">
                        <div class="content-1170 center-relative">
                            <h2 class="entry-title">
                                <a href="#">{{ post.heading }}</a>
                            </h2>
                            <div class="cat-links">
                                <ul>
                                    <li>
                                        <a href="#">{{ post.categories }}</a>
                                    </li>
                                </ul>
                            </div>
                            <div class="entry-date published">{{ post.created_at }}</div>
                            <div class="clear"></div>
                        </div>
                    </div>
                </article>
            </div>
            <div class="clear"></div>
            <div class="block load-more-holder">LOAD MORE ENTRIES</div>
        </div>
        <div class="featured-image-holder">
            <!-- <div class="featured-post-image" style="background-image: url(demo-images/featured-image.jpg)"></div> -->
        </div>
        <div class="clear"></div>
    </div>
</template>

<script setup lang="ts">
const posts = [
    {
        post_id: 1,
        created_at: 12192022,
        heading: 'Whatever is begun in anger ends in shame',
        categories: 'art',
        synopsis: 'Now when I had mastered the language of this water and had come to know every trifling feature that bordered the great river as familiarly as I knew the letters of the alphabet, I had made a valuable acquisition. I still keep in mind a certain wonderful sunset which I witnessed when and steamboating'
    },
    {
        post_id: 2,
        created_at: 12192022,
        heading: 'I like to reinvent myself',
        categories: 'science',
        synopsis: ''
    },
    {
        post_id: 3,
        created_at: 12192022,
        heading: 'It’s all about experience',
        categories: 'coding',
        synosis: ''
    },
    {
        post_id: 4,
        created_at: 12192020,
        heading: 'This is not my code',
        categories: 'coding',
        synosis: ''
    },
    {
        post_id: 5,
        created_at: 12192020,
        heading: 'Support human activity',
        categories: 'coding',
        synosis: ''
    },

]

</script>


<style lang="scss" scoped>
li {
    list-style-type: none;
}

.site-content {
    padding: 100px 62px;
}
</style>