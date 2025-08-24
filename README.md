# ROS 2 Vector3 Publisher & Subscriber Example

This project demonstrates a simple ROS 2 node written in Python using `rclpy`.  
The node publishes a `geometry_msgs/Vector3` message and simultaneously subscribes to the same topic to receive its own messages.

# How It Works
- The node creates:
  - A **publisher** on the topic `vector_topic` (`geometry_msgs/msg/Vector3`).
  - A **subscriber** on the same topic to listen for incoming messages.
  - A **timer** that publishes a new `Vector3` message every second.
- The message has fixed coordinates:
  - `x = -1.5`
  - `y = 2.5`
  - `z = 7.0`
- Every published message is also received back by the subscriber, and both sending and receiving are logged in the console.

# Code Structure
- `GeometryNode`  
  The main ROS 2 node that initializes the publisher, subscriber, and timer.  
- `timer_callback`  
  Publishes a new `Vector3` message once per second.  
- `listener_callback`  
  Receives and logs the message from the topic.  
