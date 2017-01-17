Robot

#Lecture 2

##Programs used

* leJOS

#Lecture 3

##Touch Sensor

* Touch measures 1 to 100
* Use port number ` new TouchSensorDemo(SensorPort.S1)`
* Use port as final to avoid changing port halfway through
```java
 TouchSensor ts - new TouchSensor(this.port);
 Rate r = new Rate(1);
    while (m_run){
       if(ts.isPressed()){
          Sound.beepSequence();
       }
       r.sleep()}
    }
```
* Use event driven programming: Event listening - `this.port.addSensorPortListener(aListener);`
..* A condition checks until it notifies listeners
..* The listeners then activate handlers which hold the code
