<template>
     <header class="header container">
        <div class="header__top">
            <HeaderBlock />
            <!-- <a href="index.html" class="logo"><img :src="logo" alt="logo"></a>
            <nav class="nav">
                <ul class="nav__list">
                    <li><a href="index.html">Home</a></li>
                    <li><a href="#">Project</a></li>
                    <li><a href="blog.html">Blog</a></li>
                </ul>
            </nav> -->
        </div>
    </header>

    <div class="banner banner__blogdetails">
    </div>

    <section class="blogdetails container" >
        <div class="blogdetails__content">
            <div v-for="item in this.temp" :key="item.id">
                <h1 class="blogdetails__title">{{ item.title }}</h1>
                <img class="blogdetails__img-main" :src="item.imgMain" alt="blog details img11">
                <div class="blogdetails__info">
                    <div class="blogdetails__info_data">{{ item.data }}</div>
                    <div class="blogdetails__info_breadcrumbs">
                        {{ item.breadcrumbs }}
                    </div>
                </div>
                <div class="blogdetails__text_first">
                {{ item.textFirst }}
                </div>

                <article class="article__block">
                    <svg width="74" height="56" viewBox="0 0 74 56" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M58.2516 0.600003C62.6516 0.600003 66.2516 2.06667 69.0516 5C71.7182 7.93334 73.0516 11.8667 73.0516 16.8C73.0516 25.4667 70.1849 33 64.4516 39.4C58.5849 45.8 51.5849 51.0667 43.4516 55.2L41.4516 51.8C44.7849 49.6667 47.9182 46.9333 50.8516 43.6C53.6516 40.2667 55.8516 36.6667 57.4516 32.8L51.8516 28.6C49.5849 27.1333 47.7182 25.1333 46.2516 22.6C44.7849 20.2 44.0516 17.8667 44.0516 15.6C44.0516 11.3333 45.3849 7.73334 48.0516 4.8C50.5849 2 53.9849 0.600002 58.2516 0.600003ZM17.0516 0.599999C21.4516 0.6 25.0516 2.06667 27.8516 5C30.5182 7.93333 31.8516 11.8667 31.8516 16.8C31.8516 25.4667 28.9849 33 23.2516 39.4C17.3849 45.8 10.3849 51.0667 2.25155 55.2L0.251554 51.8C3.58489 49.6667 6.71822 46.9333 9.65155 43.6C12.4516 40.2667 14.6516 36.6667 16.2516 32.8L10.6516 28.6C8.38489 27.1333 6.51822 25.1333 5.05155 22.6C3.58489 20.2 2.85156 17.8667 2.85156 15.6C2.85156 11.3333 4.18489 7.73333 6.85156 4.8C9.38489 2 12.7849 0.599999 17.0516 0.599999Z" fill="#CDA274"/>
                    </svg>
                    <div class="article__block_descr">{{ item.articleDescr }}</div>
                </article>

                <h2 class="blogdetails__subtitle">{{ item.subtitle }}</h2>
                <div class="blogdetails__text_second">
                    {{ item.textSecond }}
                </div>
                <ul class="blogdetails__list">
                    <div class="blogdetails__list_item">
                        <span>1</span><li>{{ item.listItem }}</li>
                    </div>
                    <div class="blogdetails__list_item">
                        <span>2</span><li>{{ item.listItem }}</li>
                    </div>
                    <div class="blogdetails__list_item">
                        <span>3</span><li>{{ item.listItem }}</li>
                    </div>
                                
                </ul>

                <img class="blogdetails__img" :src="item.img" alt="blog details img11">

                <div class="blogdetails__text_third">
                {{ item.textThird }}
                </div>

            </div>
        </div>
        <div class="blogdetails__sidebar">
            <h2 class="blogdetails__sidebar_title">Tags</h2>
            <div class="blogdetails__sidebar_tags">
                <button class="blogdetails__sidebar_tag" @click="showNews('Kitchen')">Kitchen</button>
                <button class="blogdetails__sidebar_tag" @click="showNews('Bedroom')">Bedroom</button>
                <button class="blogdetails__sidebar_tag" @click="showNews('Building')">Building</button>
                <button class="blogdetails__sidebar_tag" @click="showNews('Architecture')">Architecture</button>
                <button class="blogdetails__sidebar_tag" @click="showNews('Kitchen-planning')">Kitchen Planning</button>
                <button class="blogdetails__sidebar_tag" @click="showNews('Bathroom')">Bathroom</button>
                
            </div>
        </div>
    </section>


    <footer class="footer  container">
        <FooterBlock />
        <!-- <div class="footer__info">
            <a href="#" class="logo"><img :src="logo" alt="logo"></a>
            <div class="footer__descr">It is a long established fact that a reader will be distracted lookings.</div>
            <div class="footer__social">
                <a class="footer__social_twitter" href="#">
                    <svg fill="#000000" viewBox="0 0 32 32" version="1.1" xmlns="http://www.w3.org/2000/svg"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <title>twitter</title> <path d="M30.917 6.728c-1.026 0.465-2.217 0.805-3.464 0.961l-0.061 0.006c1.268-0.771 2.222-1.952 2.687-3.354l0.013-0.044c-1.124 0.667-2.431 1.179-3.82 1.464l-0.082 0.014c-1.123-1.199-2.717-1.946-4.485-1.946-3.391 0-6.14 2.749-6.14 6.14 0 0.496 0.059 0.979 0.17 1.441l-0.008-0.042c-5.113-0.254-9.613-2.68-12.629-6.366l-0.025-0.031c-0.522 0.873-0.831 1.926-0.831 3.052 0 0.013 0 0.026 0 0.039v-0.002c0 0.001 0 0.003 0 0.005 0 2.12 1.075 3.989 2.709 5.093l0.022 0.014c-1.026-0.034-1.979-0.315-2.811-0.785l0.031 0.016v0.075c0 0.001 0 0.002 0 0.002 0 2.961 2.095 5.434 4.884 6.014l0.040 0.007c-0.484 0.135-1.040 0.212-1.614 0.212-0.406 0-0.802-0.039-1.186-0.113l0.039 0.006c0.813 2.459 3.068 4.212 5.739 4.264l0.006 0c-2.072 1.638-4.721 2.627-7.602 2.627-0.005 0-0.009 0-0.014 0h0.001c-0.515-0.001-1.022-0.031-1.521-0.089l0.061 0.006c2.663 1.729 5.92 2.757 9.418 2.757 0.005 0 0.009 0 0.014 0h-0.001c0.037 0 0.082 0 0.126 0 9.578 0 17.343-7.765 17.343-17.343 0-0.039-0-0.077-0-0.116l0 0.006c0-0.262 0-0.524-0.019-0.786 1.21-0.878 2.229-1.931 3.042-3.136l0.028-0.044z"></path></g></svg></a>
                <a class="footer__social_linkedin" href="#">
                    <svg fill="#000000" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 0 512 512" xml:space="preserve"><g id="SVGRepo_bgCarrier" stroke-width="0"></g><g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g><g id="SVGRepo_iconCarrier"> <g id="7935ec95c421cee6d86eb22ecd125aef"> <path style="display: inline; fill-rule: evenodd; clip-rule: evenodd;" d="M116.504,500.219V170.654H6.975v329.564H116.504 L116.504,500.219z M61.751,125.674c38.183,0,61.968-25.328,61.968-56.953c-0.722-32.328-23.785-56.941-61.252-56.941 C24.994,11.781,0.5,36.394,0.5,68.722c0,31.625,23.772,56.953,60.53,56.953H61.751L61.751,125.674z M177.124,500.219 c0,0,1.437-298.643,0-329.564H286.67v47.794h-0.727c14.404-22.49,40.354-55.533,99.44-55.533 c72.085,0,126.116,47.103,126.116,148.333v188.971H401.971V323.912c0-44.301-15.848-74.531-55.497-74.531 c-30.254,0-48.284,20.38-56.202,40.08c-2.897,7.012-3.602,16.861-3.602,26.711v184.047H177.124L177.124,500.219z"> </path> </g> </g></svg>
                </a>
            </div>
        </div>
        <div class="footer__pages">
            <h3 class="footer__title">Pages</h3>
            <nav class="nav__footer">
                <ul class="nav__list_footer">
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Project</a></li>
                    <li><a href="#">Blog</a></li>
                </ul>
            </nav>
        </div>
        <div class="footer__contact">
            <h3 class="footer__title">Contact</h3>
            <div class="footer__contact_adress">55 East Birchwood Ave. Brooklyn, New York 11201</div>
            <a class="footer__contact_email">contact@interno.com</a>
            <a class="footer__contact_tel" href="tel:1234567890">(123) 456 - 7890</a>

        </div> -->
    </footer>
</template>

<script>
import HeaderBlock from './HeaderBlock.vue';
import FooterBlock from './FooterBlock.vue';

    export default {
        components: {HeaderBlock, FooterBlock},
        data() {
            const articles = [
                { 
                    id: 1,  tag: 'Kitchen',
                    title: 'Let’s Get Solution for Building Construction Work',
                    imgMain: require('@/assets/images/blog__details_img11.png'),
                    data: '26 December,2022',
                    breadcrumbs: 'Interior / Home / Decore',
                    textFirst: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which do not look even slightly believable. Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.',
                    articleDescr: 'The details are not the details. They make the design.',
                    subtitle: 'Design sprints are great',
                    textSecond: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    listItem: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    img: require('@/assets/images/blog__details_img12.png'),
                    textThird: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                },
                { 
                    id: 2, tag: 'Bedroom',
                    title: 'Let’s Get Solution for Building Construction Work',
                    imgMain: 'https://i.pinimg.com/originals/46/38/76/4638769a530e7c844e6671cd8af80936.jpg',
                    data: '30 December,2022',
                    breadcrumbs: 'Interior / Home / Decore',
                    textFirst: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which do not look even slightly believable. <br><br> Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.',
                    articleDescr: 'The details are not the details. They make the design.',
                    subtitle: 'Design sprints are great',
                    textSecond: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    listItem: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    img: require('@/assets/images/blog__details_img12.png'),
                    textThird: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                },
                { 
                    id: 3, tag: 'Building',
                    title: 'Let’s Get Solution for Building Construction Work',
                    imgMain: 'https://avatars.mds.yandex.net/i?id=ab513bbbe3123058188308e65b0503b33c2900f5-5008890-images-thumbs&n=13.jpg',
                    data: '30 December,2022',
                    breadcrumbs: 'Interior / Home / Decore',
                    textFirst: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which do not look even slightly believable. <br><br> Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.',
                    articleDescr: 'The details are not the details. They make the design.',
                    subtitle: 'Design sprints are great',
                    textSecond: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    listItem: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    img: require('@/assets/images/blog__details_img12.png'),
                    textThird: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                },
                { 
                    id: 4, tag: 'Architecture',
                    title: 'Let’s Get Solution for Building Construction Work',
                    imgMain: 'https://svgsilh.com/png-512/2028243.png',
                    data: '30 December,2022',
                    breadcrumbs: 'Interior / Home / Decore',
                    textFirst: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which do not look even slightly believable. <br><br> Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.',
                    articleDescr: 'The details are not the details. They make the design.',
                    subtitle: 'Design sprints are great',
                    textSecond: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    listItem: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    img: require('@/assets/images/blog__details_img12.png'),
                    textThird: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                },
                { 
                    id: 5,  tag: 'Kitchen-planning',
                    title: 'Let’s Get Solution for Building Construction Work',
                    imgMain: 'https://i.pinimg.com/736x/24/1e/8b/241e8b43f75c3cbf0e60109c923ba389.jpg',
                    data: '30 December,2022',
                    breadcrumbs: 'Interior / Home / Decore',
                    textFirst: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which do not look even slightly believable. <br><br> Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.',
                    articleDescr: 'The details are not the details. They make the design.',
                    subtitle: 'Design sprints are great',
                    textSecond: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    listItem: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    img: require('@/assets/images/blog__details_img12.png'),
                    textThird: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                },
                { 
                    id: 6, tag: 'Bathroom',
                    title: 'Let’s Get Solution for Building Construction Work',
                    imgMain: 'https://vvanna.ru/upload/iblock/d93/d9339c419c14947654d29e811aaf4f4f.jpg',
                    data: '30 December,2022',
                    breadcrumbs: 'Interior / Home / Decore',
                    textFirst: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injecthumour, or randomised words which do not look even slightly believable. <br><br> Embarrassing hidden in the middle of text. All the Lorem Ipsum generators on the Internet tend to repeat predefined chunks as necessary.',
                    articleDescr: 'The details are not the details. They make the design.',
                    subtitle: 'Design sprints are great',
                    textSecond: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    listItem: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                    img: require('@/assets/images/blog__details_img12.png'),
                    textThird: 'Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpmaximus.posuere in.Contrary to popular belief.There are many variations of passages of Lorem Ipsum available, but the majority have suffered.',
                },
            ]
            return {
                articles: articles,
                temp: articles,
                logo: require('@/assets/images/logo__img.svg'),
            }  
        },
        methods: {
            showNews(tag){
                this.temp = this.articles.filter((item) => item.tag === tag);
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>