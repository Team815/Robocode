# Square Shooter

## Robots

- **R1** - sample.SittingDuck

## Objective

Kill **R1**. You are only allowed to fire while driving in a 100 &times; 100 pixel square.

## Enhancements

- Drive in an orthogonal square (i.e. no diagonal lines).
- Ensure the robot never bumps into a wall. <sup>[1]</sup>

## Useful Methods / Constants

### `robocode.Robot`

- `void ahead(double distance)`
- `void turnLeft(double degrees)`
- `void fire(double power)`
- `double getX()`
- `double getBattleFieldWidth()`
- `double getY()`
- `double getBattleFieldHeight()`
- `double getHeading()`

#### Overrides

- `void run()`
- `void onScannedRobot(ScannedRobotEvent event)`
- `void onHitWall(HitWallEvent event)`

### `robocode.Rules`

- `static final double MAX_BULLET_POWER`

## Footnotes

**[1]** You can detect wall hits by overriding `robocode.Robot.onHitWall` and printing something if this method is ever called.