<template>


<app-navigator> </app-navigator>

</template>

<script>
import {createStackNavigator} from "react-navigation-stack";
import {createAppContainer} from "react-navigation";


import * as Permissions from 'expo-permissions';
import { Camera } from 'expo-camera';

import * as Location from "expo-location";
import { Accelerometer } from "expo-sensors";




import homescreen from "./App/screens/homescreen";
import accelescreen from "./App/screens/accelescreen";
import gpsscreen from "./App/screens/gpsscreen";
import camerascreen from "./App/screens/camerascreen";




const StackNavigator = createStackNavigator(
 
 {
    Home:homescreen,
    Camera: camerascreen,
    Gps: gpsscreen,
    Accele:accelescreen,
    
},
 {
    initialRouteName: 'Home',
  }
)

const AppNavigator = createAppContainer(StackNavigator);
export default{
  components: {AppNavigator},
}
</script>

<style>
  
  .statusbar{
    background-color: blue;
    height: 50px;
  }


</style>