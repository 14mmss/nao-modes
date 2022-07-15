# Bachelor Thesis: Human Perception of Responsive Robot Body Movement
## Marina Marques Souza dos Santos
### Artificial Intelligence Vrije Universiteit

## Setting up
The only dependency on this repository is the **NAOqi package** developed by SoftBank Robotics.

Here is the [official installation guide](http://doc.aldebaran.com/2-5/dev/python/install_guide.html)

In summary:
1. Double check the version of your Python to be 2.7 (if it's not, download it from the [official site](https://www.python.org/download/releases/2.7/))
2. Follow the instructions in the Softbank Robotics documentation as linked above for your machine.

For MAC users:
It can be necessary to add a few more environment variables than the Softbank Robotics website suggests.
In **my case** I needed to use the following:

`export PYTHONPATH=${PYTHONPATH}:/path-to-sdk/pynaoqi-python2.7-2.5.7.1-mac64/lib/python2.7/site-packages`

`export DYLD_LIBRARY_PATH=${DYLD_LIBRARY_PATH}:/path-to-sdk/pynaoqi-python2.7-2.5.7.1-mac64/lib`

`export DYLD_FRAMEWORK_PATH=${DYLD_FRAMEWORK_PATH}:/path-to-sdk/pynaoqi-python2.7-2.5.7.1-mac64`

`export QI_SDK_PREFIX=/path/to/python-sdk`

Good luck!

## Utilization

As explained in the code itself, the code provided here works optimally when given artificial input. When using real-time input, I would recommend to change the robot input function from the already in place `angleInterpolation` to `setAngle`. The `setAngle` function takes slightly different input, lacking time, thus, making it faster. To do this, make sure that you are only passing one name/angle at a time to the robot for optimal results and fewer errors :)

Other than that, there is one main variable called `moveType` that determines the type of input that the robot will use. For example, if it is set for "Normal" the robot will move normally and so on.

Hope you enjoy the repo provided!
