<template>
    <header id="header">
        <span id="LogoName"></span>
        <i @click="isActiveMenu = !isActiveMenu" id="MenuBarIcon" class="fa-solid fa-bars"></i>
        <nav :class="{ active: isActiveMenu }" ref="Navbar" id="navbar">
            <ul>
                <li>
                    <a href="#">login</a>
                    /
                    <a href="#">register</a>
                </li>

                <li>
                    <a href="/settings">settings</a>
                </li>
                <li>
                    <a href="/about">about us</a>
                </li>
                <li><a href="/contact">contact us</a></li>

            </ul>

        </nav>
    </header>

    <div id="storiesSection">

        <!-- the first story will your story -->
        <div class="story">
            <i class="fa fa-plus"></i>
            
        </div>
        <!-- the first story will your story -->

    </div>
</template>

<script>
export default {
    data() {
        return {
            isActiveMenu: false,
        };
    },
}
</script>

<style>
#storiesSection {
    display: flex;
    max-width: 100vw;
    overflow: auto;
    /* scrollbar-width: none; */
    box-shadow: 1px 1px 3px #464646;
}

.story {
    background: url('../assets/images/profile12.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    padding: 10px;
    border-image: radial-gradient(circle farthest-corner, #FF0000 0%, #FFFFFF 100%) 20;
    border-radius: 50%;
    width: 100px;
    height: 100px;
    /* display: inline-bloc; */
}

.story img {
    border-radius: 50%;

}

#LogoName {
    display: inline-block;
    padding: 10px 5px;
    background-image: url('../assets/MySocialLogo.png');
    background-size: cover;
    width: 95px;
    height: auto;
    justify-content: flex-start;
}

#header {
    padding: 20px;
    display: flex;
    justify-content: space-between;
    background-color: #0C2840;
}



#header #MenuBarIcon {
    display: none;
}

#navbar ul li a {
    color: #fff;
}

@media only screen and (max-width: 980px) {
    #header #MenuBarIcon {
        display: block;
        justify-content: flex-end;
        cursor: pointer;
        color: white;

    }

    #navbar {
        height: auto;
        width: 60vw;
        background-color: #0C2840;
        opacity: 80%;
        position: absolute;
        right: -60vw;
        display: none;
        transition: 2s;
        box-shadow: 2px 2px 5px #000;
        border-radius: 15px;
        margin: 50px 10px;
    }

    #navbar.active {
        right: 0;
        display: block;
    }

    #navbar ul {
        display: flex;
        flex-direction: column;
        text-align: center;
    }

    #navbar ul li {
        line-height: 30px;
        padding: 10px 0;
        display: block;
    }
    #storiesSection{
        scrollbar-width: none;
    }
    #storiesSection::-webkit-scrollbar {
        display: none;
    }

}

@media only screen and (min-width: 980px) {
    #header {
        display: flex;
    }

    #navbar ul {
        display: flex;
        flex-direction: row-reverse;
    }

    #navbar ul li {
        justify-content: space-between;
        margin: 0 20px;
    }
}</style>