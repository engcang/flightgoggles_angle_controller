# Flightgoggles angle controller
+ [FlightGoggles simulator](http://flightgoggles.mit.edu/) Controller using [PS4 joystick](https://asia.playstation.com/ko-kr/accessories/dualshock4/)
+ simply used P(Proportional) controller to control the angles of vehicle by rates
+ Easier to manually control than one provided by developer
<br>

### ● Wireless application of joystick controller for turtlebots, [here](https://github.com/engcang/PS4_Joystick_teleop_Mobile_Robots_ROS_Python)

<br>

## Execution
+ launch file edition Recommended :
~~~xml
    < !-- node name="universal_teleop" pkg="universal_teleop" type="universal_teleop" output="screen">
      <rosparam file="$(find universal_teleop)/launch/example_input_map.yml"/>
      <remap from="output/rateThrust" to="/uav/input/rateThrust"/>
      <remap from="output/takeoff" to="/uav/input/takeoff"/>
      <remap from="output/land" to="/uav/input/land"/>
      <remap from="output/reset" to="/uav/input/reset"/>
    </node -- >
~~~
flightgoggles/launch/teleopExample.launch's original teleop node should be commented using "!-- --"

<br>
+ Then launch the roslaunch and run [python file](https://github.com/engcang/flightgoggles_angle_controller/blob/master/simple_angle_controller.py)
~~~shell
    $ roslaunch flightgoggles teleopExample.launch
    $ python simple_angle_controller.py
~~~
