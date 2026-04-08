# Collision-Detection Stop

Sodero controllers include a collision-detection stop safety function.

If the robot detects a collision during motion, the servo power is turned off and the robot stops.

This behavior is intended to stop motion immediately when unexpected contact occurs.

## What Happens After a Collision

After a collision-detection stop, the robot does not resume motion automatically.

The operator must confirm that the collision condition has been cleared before restarting the robot.

## Restart Procedure

1. check the robot and surrounding area to confirm that the collision condition is removed
2. open the `Jog` interface
3. turn `Servo On` again
4. confirm that the robot is ready before continuing operation

## Operator Note

If a collision stop occurs repeatedly, the operator should not continue normal operation until the cause of interference is identified and removed.
