# Monkey in the Middle

## Robots

- **R1** - sample.SittingDuck
- **R2** - sample.SittingDuck

## Objective

Kill **R1** and **R2**. You are only allowed to fire if you are parked at the midpoint between **R1** and **R2**.

## Enhancements

- Kill **R1** and **R2** as close to the same time as possible. Try to kill them within 15 turns of each other. <sup>[1]</sup>

## Useful Methods / Constants

### `robocode.Robot`

- `void ahead(double distance)`
- `void turnLeft(double degrees)`
- `void turnRadarRight(double degrees)`
- `void turnGunRight(double degrees)`
- `void fire(double power)`
- `void doNothing()`
- `double getX()`
- `double getY()`
- `double getHeading()`
- `double getGunHeat()`

#### Overrides

- `void run()`
- `void onScannedRobot(ScannedRobotEvent event)`
- `void onRobotDeath(RobotDeathEvent event)`

### `robocode.ScannedRobotEvent`

- `String getName()`
- `double getDistance()`
- `double getBearing()`

### `robocode.RobotDeathEvent`
- `long getTime()`

### `robocode.Rules`

- `static final double MIN_BULLET_POWER`

### `java.lang.Math`

- `static double abs(double a)`
- `static double toRadians(double angdeg)`
- `static double sin(double a)`
- `static double cos(double a)`

## Footnotes

**[1]** You can determine the time a robot dies by overriding `robocode.Robot.onRobotDeath` and calling the `RobotDeathEvent`'s `getTime()` method.