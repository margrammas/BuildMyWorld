
### Directory Structure
```
    .BuildMyWorld                      # project lab main folder 
    ├───model
    │   ├── Building
    │   │   ├── model.config
    │   │   ├── model.sdf
    │   ├── MyRover                    # Model and Structure required for Project .1
    │   │   ├── model.config
    │   │   ├── model.sdf
    ├── script                         # Gazebo World plugin C++ script      
    │   ├── hello.cpp
    ├── world                          # Gazebo project World scene
    │   ├── MyRobotWorld
    ├── CMakeLists.txt                 # Link libraries 
    └──                              
```

### Steps to launch the simulation

#### Step 1 Update and upgrade the Workspace image
```sh
$ sudo apt-get update
$ sudo apt-get upgrade -y
```

#### Step 2 Compile the code
```sh
$ cd /home/workspace/BuildMyWorld
$ mkdir build
$ cd build/
$ cmake ../
$ make
```

#### Step 3 Add the library path to the Gazebo plugin path  
```sh
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/BuildMyWorld/build
```

#### Step 4 Run the Gazebo World file  
```sh
$ cd /home/workspace/BuildMyWorld/world/
$ gazebo MyRobotWorld
```

### Output
The "Hello Marco's RoboWorld'" message along with the World required for "BuildMyWorld" project should be visible.

    
 
