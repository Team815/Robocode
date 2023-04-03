# Up Close and Personal

## Robots

- **R1** - sample.SittingDuck

## Objective

Kill **R1**. You are only allowed to fire if you are within 150 pixels of **R1**.

## Enhancements

- Do not turn more than 180&deg; to face **R1**.
- Do not drive forward/backward if you start within 150 pixels of **R1**.
- Do not fire more bullets than necessary to kill **R1**. <sup>[1]</sup>

## Useful Methods / Constants

### `robocode.Robot`

- `void ahead(double distance)`
- `void turnRight(double degrees)`
- `void turnRadarRight(double degrees)`
- `void fire(double power)`

#### Overrides

- `void run()`
- `void onScannedRobot(ScannedRobotEvent event)`
- `void onRobotDeath(RobotDeathEvent event)`

### `robocode.ScannedRobotEvent`

- `double getDistance()`
- `double getBearing()`

### `robocode.Rules`

- `static final double MAX_BULLET_POWER`

### `robocode.util.Utils`

- `static double normalRelativeAngleDegrees(double angle)`

### `java.lang.Math`

- `public static double max(double a, double b)`

## Footnotes

**[1]** If you fire within a range of 150 pixels at `MAX_BULLET_POWER`, your fire rate should be slow enough such that each bullet will hit **R1** before the next is fired. This is not guaranteed for smaller bullet powers which have higher fire rates.