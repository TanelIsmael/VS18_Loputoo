<template>
    <footer>
            <div class="footer-item">
                <p class="footer-item__heading">Aadress</p>
                <p>Tartu Kutsehariduskeskus</p>
                <p>Kopli 1, 50115 Tartu</p>
            </div>


            <div class="footer-item">
                <p class="footer-item__heading">Kontakt</p>
                <p><a href="#">Tel: +372 736 1842</a></p>
                <p><a href="#">E-post: hellika.ivanov@khk.ee</a></p>
                <p>Tööruum: Kopli 1 A-412</p>
            </div>

            <div class="footer-item">
                <p class="footer-item__heading">Lingid</p>
                <p><a href="#">Tartu Kutsehariduskeskus</a></p>
            </div>
    </footer>
</template>

<style lang="scss" scoped>

    footer {
        // position: absolute;
        // left: 0;
        // bottom: 0;
        display: flex;
        justify-content: center;
        background: #2e2e2e;
        padding: 20px 0;
        height: 200px;
        width: 100%;
        // margin-top: 202px;

        .footer-item {
            padding: 0 100px;

            .footer-item__heading {
                font-family: 'Open Sans', sans-serif;
                font-weight: 700;
                font-size: 1rem;
                margin-bottom: 20px;
            }

            p {
                color: #ffffff;
                margin: 5px 0;

                a {
                    color: #ffffff;
                    text-decoration: none;

                    &:hover {
                        color: #0054a6;
                    }
                }
            }
        }
    }
</style>