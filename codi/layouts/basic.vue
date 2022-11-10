<template>
    <v-app>
      <Capsalira 
      color="blue"
      marca="Ferrari"
      ></Capsalira>
        <v-main>
            <v-container>
                <v-row>
                    <v-col
                        cols="12"
                        md="8"
                    >
                        <nuxt/>
                    </v-col>
                    <v-col
                        cols="12"
                        md="4">
                        <v-img src="https://images.pexels.com/photos/4066147/pexels-photo-4066147.jpeg?cs=srgb&dl=pexels-erik-mclean-4066147.jpg&fm=jpg&_gl=1*1nsdsra*_ga*NTY2NzMyNzgyLjE2NjgwOTg4MDA.*_ga_8JE65Q40S6*MTY2ODA5ODgyMy4xLjEuMTY2ODA5OTMyOC4wLjAuMA." 
                        height="100vh">Ciel</v-img>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>

            <v-footer>
                <v-container>
                    <v-row>
                        <v-col align="center">
                            Tots els drets reservats Jordi Gasau 2022
                        </v-col>
                    </v-row>
                </v-container>
            </v-footer>
    </v-app>
</template>