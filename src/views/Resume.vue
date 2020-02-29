<template>
    <div class="resume">
        <!-- Basic Information -->
        <v-container class="section">
            <v-layout row wrap justify-space-around>
                <v-flex xs 12 md5 lg4>
                    <v-img class=" profile-pic" src="/profile-picture.png">
                    </v-img>
                </v-flex>
                <v-flex xs12 md7>
                    <v-card flat text-xs-center>
                        <v-card-title class="display-2 font-weight-light">
                            Tobias Furtlehner
                        </v-card-title>
                        <v-card-text class="body-1">
                            <p>born on June 6th, 2002</p>
                            <p>Austria, Maria Enzersdorf</p>
                            <p>tobiasfurtlehner@hotmail.com</p>
                        </v-card-text>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>

        <!-- Education -->
        <v-parallax src="/classroom2.jpg" class="section" height="800">
            <h1 class="lax display-4 text-center educationheadline" data-lax-preset="fadeIn">Education</h1>
            <v-layout row wrap justify-space-around class="lax" data-lax-preset="rightToLeft-.05">
                <v-flex xs12 md3>
                    <v-card shaped>
                        <v-card-title class="headline">
                            BG/BRG Keimgasse
                        </v-card-title>
                        <v-card-subtitle>
                            Modellklasse
                        </v-card-subtitle>
                        <v-card-text>
                            09-2012 - 06/2015
                        </v-card-text>
                    </v-card>
                </v-flex>
                <v-flex xs12 md3>
                    <v-card shaped>
                        <v-card-title class="headline">
                            HTBLVA Spengergasse
                        </v-card-title>
                        <v-card-subtitle>
                            IT Department
                        </v-card-subtitle>
                        <v-card-text>
                            since September 2015
                        </v-card-text>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-parallax>

        <!-- Work Experience -->
        <v-parallax src="/work6.jpg" class="section" height="800">
            <h1 class="lax display-4 text-center educationheadline black--text" data-lax-preset="fadeIn">Work Experience
            </h1>
            <v-layout row wrap justify-space-around class="lax" data-lax-preset="rightToLeft-.05">
                <v-flex xs12 md3>
                    <v-card shaped>
                        <v-card-title class="headline">
                            BG/BRG Keimgasse
                        </v-card-title>
                        <v-card-subtitle>
                            Modellklasse
                        </v-card-subtitle>
                        <v-card-text>
                            09-2012 - 06/2015
                        </v-card-text>
                    </v-card>
                </v-flex>
                <v-flex xs12 md3>
                    <v-card shaped>
                        <v-card-title class="headline">
                            HTBLVA Spengergasse
                        </v-card-title>
                        <v-card-subtitle>
                            IT Department
                        </v-card-subtitle>
                        <v-card-text>
                            since September 2015
                        </v-card-text>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-parallax>

        <div class="section"></div>
        <div class="section"></div>
    </div>
</template>

<script>
    import lax from 'lax.js'
    export default {
        mounted() {
            lax.setup()
            lax.addElement(this.$el)
            let laxxScript = document.createElement('script')
            laxxScript.setAttribute('src', 'lib/lax.min.js')
            const updateLax = () => {
                lax.update(window.scrollY)
                window.requestAnimationFrame(updateLax)
            }
            window.requestAnimationFrame(updateLax)
        }
    }
</script>

<style>
    .resume {
        padding-top: 5pt;
    }

    .section {
        height: 100vh;
    }

    .educationheadline {
        margin-top: 115pt;
        margin-bottom: 115pt;
    }

    .profile-pic {
        box-shadow: 3px 3px 5px 1px rgba(99, 99, 99, 0.7);
        border-radius: 2pt;
        height: 400pt;
        width: 250pt;
        margin: auto;
    }

    .parallax-mirror,
    #vurtUnderlay {
        height: auto !important;
        width: 100% !important;
        padding: 45% 0 0;
    }

    .parallax-mirror img {
        width: 100% !important;
        height: 100% !important
    }
</style>