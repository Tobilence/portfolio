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
                            <p>born on June 10th, 2002</p>
                            <p>Austria, Maria Enzersdorf</p>
                            <p>tobiasfurtlehner@hotmail.com</p>
                        </v-card-text>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>

        <!-- Education -->
        <v-parallax src="/education.jpg" class="section" height="800">
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
        <v-parallax src="/work.jpg" class="section" height="800">
            <h1 class="lax display-4 text-center educationheadline black--text" data-lax-preset="fadeIn">Work Experience
            </h1>
            <v-layout row wrap justify-space-around class="lax" data-lax-preset="rightToLeft-.05">
                <v-flex xs12 md3>
                    <v-card shaped>
                        <v-card-title class="headline">
                            ms.gis
                        </v-card-title>
                        <v-card-subtitle>
                            Developing Geodata Game
                        </v-card-subtitle>
                        <v-card-text>
                            July, 2016
                        </v-card-text>
                    </v-card>
                </v-flex>
                <v-flex xs12 md3>
                    <v-card shaped>
                        <v-card-title class="headline">
                            ms.gis
                        </v-card-title>
                        <v-card-subtitle>
                            Redesigning Database Access
                        </v-card-subtitle>
                        <v-card-text>
                            July, 2017
                        </v-card-text>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-parallax>

        <!-- International Experiences Header-->
        <v-container>
            <h1 class="lax display-4 text-center educationheadline black--text" data-lax-preset="fadeIn">
                International
                Experiences
            </h1>
        </v-container>

        <!-- America -->
        <v-parallax src="/international-experience.jpeg" class="section" height="800">
            <v-layout row wrap justify-space-around>
                <v-flex xs12 md6>
                    <h1 class="lax display-2 exchangeyeartext text--center white--text" data-lax-preset="fadeIn">
                        Exchangeyear <br /> in <br /> America
                    </h1>
                </v-flex>
                <!-- Placeholder to align the text above to the left-->
                <v-flex md6>

                </v-flex>
            </v-layout>
            <v-layout row wrap justify-space-around>
                <v-flex xs12 md5>
                    <v-card shaped elevation-50>
                        <v-card-title class="headline">
                            Birmingham Community Charter High School
                        </v-card-title>
                        <v-card-subtitle class="subtitle-2">
                            Los Angeles, California
                        </v-card-subtitle>
                        <v-card-text>
                            <p>Lived with a host family</p>
                            <p>Graduated with a 3.9 GPA</p>
                            <p>Went to Playoffs in Boys Volleyball</p>
                            <p>Achieved perfect Attendence</p>
                        </v-card-text>
                    </v-card>
                </v-flex>
                <v-flex xs12 md6>
                    <v-img class="lax graduation-pic" data-lax-preset="rightToLeft-1.35 blurInOut fadeInOut"
                        src="/graduation.jpeg" width="400pt" height="250pt">

                    </v-img>
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

    .exchangeyeartext {
        margin-top: 60pt;
        text-align: center;
    }

    .profile-pic {
        box-shadow: 3px 3px 5px 1px rgba(99, 99, 99, 0.7);
        border-radius: 2pt;
        height: 400pt;
        width: 250pt;
        margin: auto;
    }

    .graduation-pic {
        margin-left: 600pt;
        box-shadow: 3px 3px 10px 1px rgba(99, 99, 99, 0.7);
        border-radius: 5pt;
    }
</style>