# BaselineCode2027
Swerve drive code for the 2026-2027 FRC

Swerve module info:
so far we are pretty sure that the swerve modules on 4293(Komodo, the one with the two falcons on top) is from swerve drive specialties and is the MK4(not a submodule like MK4i) layout drawing assembly guide assembly video

we think that the modules on 4293 are most likely the MK4i from swerve drive specialties layout drawing assembly guide assembly video


The main difficulty in swerve is not getting the motors or telling the what to do, it the figuring out how to get field relative steering (pushing forward always moves the robot to the other end of the field regardless of orientation)

In order to do this we will need a gyro and a good pose estimation(the pose estimation will just be so we know where we are)
we can use the built in SwerveDriveOdometry(or SwerveDrivePoseEstimator if we want to include vision data) witch will be VERY helpful. We will only need vendor libraries if the encoder is connected to the rio through CAN wires
for the gyroscope, there is one inside of the navx 2, for which we can use the Kauai Labs navX FRC RoboRIO library

Basic Development steps:
change all variables and constants from tank to swerve
develop basic field oriented movement and rotation
simultaneous rotation and movement
migrate from roborio to systemcore
basic vision and autos
complex vision and autos (using pose and path planner)

so we only technically need a gyro for field oriented driving, but if we want good autos, we should just combine it with enccoders to get a full odometry

Helpful sites: zero to robot