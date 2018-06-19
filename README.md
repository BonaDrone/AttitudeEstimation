# AttitudeEstimation
Madgwick AHRS attitude estimation in c++

It basically provides two functions that estimate the attitude (they calculate the quaternion) via Madgwick's AHRS algorithm.

## Usage

Clone or download the repository under the `Arduino/libraries` folder and write `#include <MadgwickAHRS.hpp>` at the top of the file where you want to use the functions.

## Available Functions

### MadgwickAHRSupdate 

Function signature:

```cpp
void MadgwickAHRSupdate(float quat[4], float gx, float gy, float gz, float ax, float ay, float az, float mx, float my, float mz);
```

Parameters:
* `float quat[4]`: length 4 float array where the computed quaternion will be stored.
* `float gx`, `float gy`, `float gz`: Gyrometer readings in rad/s.
* `float ax`, `float ay`, `float az`: Accelerometer readings in g-s.
* `float mx`, `float my`, `float mz`: Magnetometer readings in milliGauss.


### MadgwickAHRSupdateIMU

Function signature:

```cpp
void MadgwickAHRSupdateIMU(float quat[4], float gx, float gy, float gz, float ax, float ay, float az);
```

Parameters:
* `float quat[4]`: length 4 float array where the computed quaternion will be stored.
* `float gx`, `float gy`, `float gz`: Gyrometer readings in rad/s.
* `float ax`, `float ay`, `float az`: Accelerometer readings in g-s.