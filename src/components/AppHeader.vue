<script>
export default {
    data() {
        return {
            navItems: [
                {
                    title: "CHARACTERS",
                    isActive: false,
                },
                {
                    title: "COMICS",
                    isActive: true,
                },
                {
                    title: "MOVIES",
                    isActive: false,
                },
                {
                    title: "TV",
                    isActive: false,
                },
                {
                    title: "GAMES",
                    isActive: false,
                },
                {
                    title: "COLLECTIBLES",
                    isActive: false,
                },
                {
                    title: "VIDEOS",
                    isActive: false,
                },
                {
                    title: "FANS",
                    isActive: false,
                },
                {
                    title: "NEWS",
                    isActive: false,
                },
                {
                    title: "SHOP",
                    isActive: false,
                },
            ],
        };
    },
};
</script>

<template>
    <div class="container">
        <header>
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="Logo DC">
            </div>
            <nav>
                <ul>
                    <li v-for="item in navItems" :key="item.title"><a :class="{ 'active': item.isActive }" href="">{{ item.title }}</a></li>
                </ul>
            </nav>
        </header>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;


header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem;

    .logo {
        text-align: center;

        img {
            width: 80px;
        }
    }

    ul {
        @include flex();
        list-style: none;
        gap: 1rem;
        font-size: 0.8rem;

        a {
            text-decoration: none;
            color: black;
            padding: 1rem;
            padding-bottom: 3rem;

            &:hover {
                color: $primary;
                border-bottom: 4px solid $primary;
            }

            &.active {
                color: $primary;
                border-bottom: 4px solid $primary;
            }
        }
    }
}
</style>
