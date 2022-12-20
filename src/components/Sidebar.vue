<template>
    <div id="sidebar" class="sidebar">
        <div class="menu-left-part" tabindex="0" style="overflow: hidden; outline: none; width: 320px;"
            v-if="toggleSidebarValue">
            <div class="search-holder">
                <label>
                    <input type="search" class="search-field" placeholder="Type here to search..." value="" name="s"
                        title="Search for:">
                </label>
            </div>
            <div class="site-info-holder">
                <h1 class="site-title">Suppablog</h1>
                <p class="site-description">
                    Suppablog is simple and yet cool wordpress theme to lorem ipsum dolor sit.
                </p>
            </div>
            <nav id="header-main-menu">
                <ul class="main-menu">
                    <li><a href="index.html" class="current">Home</a></li>
                    <li><a href="about.html">About</a></li>
                    <li><a href="scroll.html">Scroll</a></li>
                    <li><a href="contact.html">Contact</a></li>
                </ul>
            </nav>
            <footer>
                <div class="footer-info">
                    © 2018 SUPPABLOG. <br> CLONE WITH <i class="fa fa-heart"></i> DESIGN BY <a
                        href="https://colorlib.com">COLORLIB</a>.
                </div>
            </footer>
        </div>
        <div class="menu-right-part">
            <div class="logo-holder">
                <a href="#">
                    <img src="../assets/images/logo.png.webp" alt="Suppablog WP">
                </a>
            </div>
            <div class="toggle-holder" @click="toggleSidebar">
                <i class="fa-solid fa-xmark" v-if="toggleSidebarValue"></i>
                <i class="fa-solid fa-bars" v-else></i>
            </div>
            <div class="social-holder">
                <div class="social-list">
                    <a href="#"><i class="fa-brands fa-twitter"></i></a>
                    <a href="#"><i class="fa-brands fa-youtube"></i></a>
                    <a href="#"><i class="fa-brands fa-facebook"></i></a>
                    <a href="#"><i class="fa-brands fa-vimeo"></i></a>
                    <a href="#"><i class="fa-brands fa-behance"></i></a>
                    <a href="#"><i class="fa-solid fa-rss"></i></a>
                </div>
            </div>
            <div class="fixed scroll-top"><i class="fa fa-caret-square-o-up" aria-hidden="true"></i></div>
        </div>
        <div class="clear"></div>
        <div id="ascrail2001" class="nicescroll-rails nicescroll-rails-vr"
            style="width: 12px; z-index: 3; cursor: default; position: absolute; top: 0px; left: 308px; height: 430px; touch-action: none; opacity: 0; display: none;">
            <div class="nicescroll-cursors"
                style="position: relative; top: 0px; float: right; width: 12px; height: 0px; background-color: rgb(91, 91, 91); border: none; background-clip: padding-box; border-radius: 0px; touch-action: none;">
            </div>
        </div>
        <div id="ascrail2001-hr" class="nicescroll-rails nicescroll-rails-hr"
            style="height: 12px; z-index: 3; top: 418px; left: 0px; position: absolute; cursor: default; display: none; width: 308px; opacity: 0;">
            <div class="nicescroll-cursors"
                style="position: absolute; top: 0px; height: 12px; width: 0px; background-color: rgb(91, 91, 91); border: none; background-clip: padding-box; border-radius: 0px; left: 0px;">
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

let toggleSidebarValue = ref<boolean>(false)

const toggleSidebar = () => {
    toggleSidebarValue.value = !toggleSidebarValue.value
    // console.log(toggleSidebarValue.value);
}

</script>

<style lang="scss" scoped>
.sidebar {
    display: flex;
    min-height: 1349px;
    width: auto;

    .menu-left-part {
        max-width: 320px;
        background-color: #404040;

        .search-holder {
            input {
                background: none;
                outline: none;
                border: none;
                width: 100%;
                padding: 42.5px;
                background-color: #2D2D2D;
            }
        }

        .site-info-holder {
            padding: 42.5px;

            h1 {
                color: #fff;
                margin-bottom: 12px;
            }

            p {
                color: #848484;
                font-size: 15px;
            }
        }

        nav {
            padding: 80px 42.5px;
            color: #fff;

            .main-menu {
                list-style-type: none;

                li {
                    padding: 13px 0;
                }

                a {
                    color: #fff;
                    font-size: 18px;

                    &:hover {
                        color: #848484;
                    }
                }
            }
        }

        footer {
            padding: 42.5px;

            .footer-info {
                font-size: 10px;
                color: #fff;
                letter-spacing: 3px;

                i {
                    color: #d8588c;
                    animation: beat .25s infinite alternate;
                    transform-origin: center;

                    @keyframes beat {
                        to {
                            transform: scale(1.4);
                        }
                    }
                }
            }
        }
    }

    .menu-right-part {
        max-width: 100px;
        background-color: #2D2D2D;
        display: flex;
        flex-direction: column;
        transition: 0.1s ease-in-out;

        .logo-holder {
            height: 100px;
        }

        .toggle-holder {
            height: 100px;
            padding-top: 33.33px;
            text-align: center;
            font-size: 20px;
            text-align: center;
            background-color: #404040;
        }

        .social-holder {
            width: 100%;

            .social-list {
                display: flex;
                flex-direction: column;


                a {
                    width: 100%;
                    height: 100px;
                    font-size: 20px;
                    text-align: center;
                    padding-top: 33.33px;
                }
            }
        }


    }
}
</style>