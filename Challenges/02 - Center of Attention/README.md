# Center of Attention

## Robots

- **R1** - sample.SittingDuck

## Objective

Kill **R1**. You are only allowed to fire if you are parked in the center of the battlefield.

## Enhancements

- Move to the center of the battlefield in a single movement.
- Do not turn more than 90&deg; between movements.
- Do not fire more bullets than necessary to kill **R1**.

## Useful Methods / Constants

### `robocode.Robot`

- `void ahead(double distance)`
- `void turnLeft(double degrees)`
- `void turnRadarRight(double degrees)`
- `void turnGunRight(double degrees)`
- `void fire(double power)`
- `void doNothing()`
- `double getX()`
- `double getBattleFieldWidth()`
- `double getY()`
- `double getBattleFieldHeight()`
- `double getGunHeat()`

#### Overrides

- `void run()`
- `void onScannedRobot(ScannedRobotEvent event)`

### `robocode.ScannedRobotEvent`

- `double getBearing()`
- `double getEnergy()`

### `robocode.Rules`

- `static double getBulletDamage(double bulletPower)`
- `static final double MAX_BULLET_POWER`

### `robocode.util.Utils`

- `static double normalRelativeAngleDegrees(double angle)`

### `java.lang.Math`

- `static double sqrt(double a)`
- `static double atan(double a)`
- `static double toDegrees(double angrad)`
- `static double abs(double a)`
- `static double signum(double d)`