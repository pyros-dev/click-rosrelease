cmake_minimum_required(VERSION 2.8.3)
project(click)

# Minimal Python module setup - catkin is assumed preinstalled along with ROS
# This assume catkin is installed along with a minimal ROS system.
find_package(catkin REQUIRED COMPONENTS
    catkin_pip
)

# defining current package as a package that should be managed by pip (not catkin - even though we make it usable with workspaces)
catkin_pip_package(click)

## Unit tests
if (CATKIN_ENABLE_TESTING)

    ############
    # Nose Tests
    ############

    catkin_add_pytests(tests)

endif()
