# Modules Reference: Estimator

## airspeed_estimator
Source: [modules/airspeed_selector](https://github.com/PX4/Firmware/tree/master/src/modules/airspeed_selector)


### Description
This module provides a single airspeed_validated topic, containing an indicated (IAS),
equivalend (EAS), true airspeed (TAS) and the information if the estimation currently
is invalid and if based sensor readings or on groundspeed minus windspeed.
Supporting the input of multiple "raw" airspeed inputs, this module automatically switches
to a valid sensor in case of failure detection. For failure detection as well as for
the estimation of a scale factor from IAS to EAS, it runs several wind estimators
and also publishes those.


### Usage {#airspeed_estimator_usage}
```
airspeed_estimator <command> [arguments...]
 Commands:
   start

   stop

   status        print status info
```
## ekf2
Source: [modules/ekf2](https://github.com/PX4/Firmware/tree/master/src/modules/ekf2)


### Description
Attitude and position estimator using an Extended Kalman Filter. It is used for Multirotors and Fixed-Wing.

The documentation can be found on the [ECL/EKF Overview & Tuning](https://docs.px4.io/en/advanced_config/tuning_the_ecl_ekf.html) page.

ekf2 can be started in replay mode (`-r`): in this mode it does not access the system time, but only uses the
timestamps from the sensor topics.


### Usage {#ekf2_usage}
```
ekf2 <command> [arguments...]
 Commands:
   start
     [-r]        Enable replay mode

   stop

   status        print status info
```
## local_position_estimator
Source: [modules/local_position_estimator](https://github.com/PX4/Firmware/tree/master/src/modules/local_position_estimator)


### Description
Attitude and position estimator using an Extended Kalman Filter.


### Usage {#local_position_estimator_usage}
```
local_position_estimator <command> [arguments...]
 Commands:
   start

   stop

   status        print status info
```
