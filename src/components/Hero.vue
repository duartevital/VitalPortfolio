<template>
    <main>
        <div class="hero-text">
            <h1 ref="greeting">Hi I'm</h1>
            <h2 ref="name">Duarte.</h2>
            <div ref="profession" @click="goToMe" class="title-wrapper">
                <h3>Software Engineer</h3>
            </div>
            <div>
                <ul>
                    <li>
                        <img class="icon" src="../assets/icons/net-core.svg" alt="netcore" />
                    </li>
                    <li>
                        <img class="icon" src="../assets/icons/csharp.svg" alt="csharp" />
                    </li>
                    <li>
                        <img class="icon" src="../assets/icons/vue.svg" alt="vuejs" />
                    </li>
                    <li>
                        <img class="icon" src="../assets/icons/typescript.svg" alt="typescript" />
                    </li>
                    <li>
                        <img class="icon" src="../assets/icons/sql.svg" alt="sql" />
                    </li>
                </ul>
            </div>
        </div>
        <aside class="hero-image">
            <!--@mouseenter="imagePopup"
                @mouseleave="imagePopdown"-->
            <img
                class="portrait"
                ref="img"
                src="../assets/images/home-portrait.jpg"
                alt="Portrait photo of Duarte"
            />
        </aside>
    </main>
</template>

<script>
export default {
  name: "Hero",
  methods: {
    goToMe() {
      document.getElementById("me").scrollIntoView({ behavior: "smooth" });
    },
  }
}
</script>

<style scoped>
    main {
        display: flex;
        flex-flow: row wrap-reverse;
        justify-content: space-between;
        width: 100%;
    }
    h1 {
        margin: 0;
        font-weight: 300;
        font-size: clamp(32px, 4vw, 52px);
    }
    h2 {
        margin: 0;
        font-size: clamp(62px, 8vw, 140px);
        font-weight: 900;
    }
    h3 {
        text-align: center;
        font-size: clamp(20px, 2.8vw, 44px);
        margin: 0;
        font-weight: 700;
    }
    .portrait {
        border: 10px solid white;
        border-radius: 20%;
        width: clamp(200px, 20vw, 20vw);
    }    
    ul {
        margin-top: clamp(3em, 3vw, 4vw);
        list-style-type: none;
        display: flex;
        justify-content: space-between;
    }
    .icon {
        height: 30px;
        filter: grayscale();
        transition: filter 0.2s ease-in-out;        
    }
    .icon:hover {
        filter: none;
    }
    .title-wrapper {
        cursor: pointer;
        margin-top: 1.4em;
        padding: 1em;
        width: 100%;
        background-color: white;
        color: #1c1c1c;
        transition: all 0.2s ease-in-out;
        z-index: 2;
        border-radius: 20px;
    }
    .title-wrapper:hover {
        background-color: var(--primary-color);
    }

    @media (max-width: 700px) {
        main {
            justify-content: center;
            width: 100%;
        }
        img {
            margin-bottom: 2em;
        }
    }
</style>