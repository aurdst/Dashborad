<template>
    <div>
        <b-card no-body>
            <b-card-header header-tag="nav">
                <b-nav card-header tabs>
                    <b-nav-item
                        v-for="(item, index) in companyData"
                        :key="index"
                        :active="index === activeTabIndex"
                        @click="activeTabIndex = index"
                    >
                        {{ item.name }}
                    </b-nav-item>
                </b-nav>
            </b-card-header>

            <b-card-body class="text-center">
                <b-card-title>{{ companyData[activeTabIndex].name }}</b-card-title>

                <b-card-text>
                    {{ companyData[activeTabIndex].present }}
                </b-card-text>

                <b-button variant="primary">Edit</b-button>
            </b-card-body>
        </b-card>
    </div>
</template>

<script>
    export default {
        name: 'companyData',
        data() {
            return {
                companyData: [
                    {
                        name: 'Apple',
                        present:
                            'Apple Inc est une entreprise multinationale américaine qui crée et commercialise des produits électroniques grand public, des ordinateurs personnels et des logiciels.',
                    },
                    {
                        name: 'About us',
                        present:
                            'Apple commercialise des produits électroniques grand public, des ordinateurs personnels et des logiciels.',
                    },
                    {
                        name: 'WebSite',
                        present:
                            'https://www.apple.com/fr',
                    },
                    // Ajoutez d'autres données d'entreprise ici
                ],
                activeTabIndex: 0, // Indice de l'onglet actif
    };
        }
    }
</script>