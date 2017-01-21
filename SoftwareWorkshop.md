#Software Workshop

##Threading

* Look on https://gitlab.com for recommended reading (`/mhe/SWW`)
* Uses scheduler to organise threads
..* If multiple programmes want to run simultaneously it designates the processor between them
* In Java, if we want to use threading we need to implements Runnable or Extends Thread
* A Master class runs slave classes and can interrupt them
* Emacs is shit

###Java Commands
```java
public class Slave implements Runnable{
   @Overrides
   run(){
   }
}
```
Master can use `Slave.interupt();` to end the thread
`Thread.sleep()` to pause the thread (Thread is used inside the Slave, Slave is
used inside the Master class test 

###Real world applications

In networking a server is connected to multiple clients. In this case a server
can be used with threading to control its clients attached to it. (Will come
back to this)

###Races

When 2 or more Threads want to change the same data there can be a situation if they
access and change it at the same time, causing an incorrect value

In order to fix this use synchronise


##Dead locks

When 2 or more threads are waiting for the others to complete, causing them to
never complete.

`Thread.join()` only ends once the thread has ended

In order to prevent this a Lock is used to show whether or not the memory is
being accessed.

Alternatively synchronized can be used which creates a lock in the _Object_
(can't use static with sync)

You have to use synchronize on the method call in order to create a lock on the
method to all Objects accessing it. To avoid a deadlock with multiple methods
use nested syncing to create a double lock.

##Sockets

###Client

```java
Socket s = new Socket("Machine name", int PortNumber);
```

To get input from the sever we require an input stream:

###Server

```java
ServerSocket s = new ServerSocket(PortNumber);
```
We also need to create a listener for the client to connect to the server.
```java
Socket listen = s.accept();
```

Note: all of these throw exceptions but I'm too lazy here to write them out.

###I/O

For gathering input:

```java
DataInputstream input = new DataInputStream(s.getIputStream());
```

For sending output;

```java
DataOutputStream output = new DataOutStream(s.getOutputStream());
```


