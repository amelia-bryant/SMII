<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>

<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
<script type="text/javascript" src="tutorialSheetScripts.js"> </script>
<link rel="stylesheet" type="text/css" media="all" href="styles.css">


# Tutorial Sheet 2: Planar Kinematics with Acceleration 

**Topics covered are**
- Acceleration in 2D 
- Relative accelerations

**Tips**
- The questions start to get quite wordy. Drawing it all out helps!
- Counterclockwise is taken as positive (the +k direction). All vectors on this sheet are written with all three components, e.g. $\omega = 0i + 0j + 2k$ rad/s rather than $2k$ rad/s, so every cross product can be set up as a determinant.
- In 2D planar motion $\omega$ is always perpendicular to $r$, so $\omega\times(\omega\times r) = -\omega^2 r$ and it does not matter which form of the relative acceleration equation we use. When expanding to 3D, only $\omega\times(\omega\times r)$ works, but for the moment $-\omega^2 r$ is faster. 

<br>

## Question 1 

The rigid body rotates about the z axis with counterclockwise angular velocity ω = 4 rad/s and counterclockwise angular acceleration α = 2 rad/s $^2$. Point B lies on the axis of rotation and the distance $r_{A/B}$ = 0.6 m.  

**(a)** What are the rigid body’s angular velocity and angular acceleration vectors? <br> 
**(b)** Determine the acceleration of point A relative to point B.

<img src = "figs\02_planar_kinematics_accel\Q1.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ \omega = 0i + 0j + 4k \text{ rad/s} \\ \alpha = 0i + 0j + 2k \text{ rad/s}^2 $$

**(b)** 

$$ a_{A/B} = -9.6i+1.2j+0k \text{ m/s}^2 $$


## Question 2

The helicopter is in planar motion in the xy plane. At the instant shown, the position of its center of mass G is x = 2 m, y = 2.5 m, its velocity is $v_G = 12i + 4j + 0k$ m/s, and its acceleration is $a_G = 2i + 3j + 0k$ m/s $^2$. The position of point T where the tail rotor is mounted is x = -3.5 m, y = 4.5 m. The helicopter’s angular velocity is 0.2 rad/s clockwise, and its angular acceleration is 0.1 rad/s $^2$ counterclockwise.

What is the acceleration of point T?

<img src = "figs\02_planar_kinematics_accel\Q2.jpg" width="50%"> <br>

### Answer

$$ a_T= 2.02i+2.37j+0k \text{ m/s}^2 $$


## Question 3

The bar rotates about the fixed pin B at its lower end with a counterclockwise angular velocity of 5 rad/s and a counterclockwise angular acceleration of 30 rad/s $^2$. Determine the acceleration of the end A using $ a_{A}=a_B+\alpha\times r_{A/B}+\omega\times(\omega\times r_{A/B}) $.

<img src = "figs\02_planar_kinematics_accel\Q3.jpg" width="50%"> <br>

### Answer

$$ a_A = -73.3i+27.0j+0k \text{ m/s}^2 $$

## Question 4

The body of the excavator is stationary, so point A is fixed. If $\omega_{AB}$ = 2 rad/s, $\alpha_{AB}$ = 2 rad/s $^2$, $\omega_{BC}$ = −1 rad/s, and $\alpha_{BC}$ = −4 rad/s $^2$ (counterclockwise positive), what is the acceleration of point C where the scoop of the excavator is attached?

<img src = "figs\02_planar_kinematics_accel\Q4.jpg" width="50%"> <br>

### Answer

$$ a_C = -24.1i-18.3j+0k \text{ m/s}^2 $$

## Question 5

The bar has length L = 4 m and makes an angle θ = 30° with the wall. Its upper end slides down the vertical wall and its lower end slides along the floor, and both ends stay in contact with these surfaces throughout the motion. At the instant shown, the bar’s angular velocity is ω = 1.8 rad/s and its angular acceleration is α = 6 rad/s $^2$, both counterclockwise. Determine the acceleration of the midpoint G.

<img src = "figs\02_planar_kinematics_accel\Q5.jpg" width="50%"> <br>

### Answer

$$ a_G = 7.15i-11.6j+0k \text{ m/s}^2 $$

## Question 6

Bar AB rotates about the fixed pin A with a clockwise angular velocity of magnitude $\omega_{AB}$ = 6 rad/s, and the slider C moves horizontally in its guide. If the acceleration of the slider C is zero at the instant shown, what is the angular acceleration $\alpha_{AB}$?

<img src = "figs\02_planar_kinematics_accel\Q6.jpg" width="50%"> <br>

### Answer

$$ \alpha_{AB} = 0i + 0j - 19.0k \text{ rad/s}^2 $$

i.e. 19.0 rad/s $^2$ clockwise.

## Question 7

The crank AB rotates about the fixed point A (A does not move), and the piston C slides horizontally along the x axis. At the instant shown, the piston’s velocity and acceleration are $v_C = -14i + 0j + 0k$ m/s and $a_C = -2200i + 0j + 0k$ m/s $^2$. What is the angular acceleration of the crank AB?

<img src = "figs\02_planar_kinematics_accel\Q7.jpg" width="50%"> <br>

### Answer

$$ \alpha_{AB} = 0i + 0j - 3530k \text{ rad/s}^2 $$

i.e. 3530 rad/s $^2$ clockwise.

## Question 8

The robotic arm moves in the xy plane, and A is a fixed pivot. Arm AB has a constant clockwise angular velocity of 0.8 rad/s, arm BC has a constant counterclockwise angular velocity of 0.2 rad/s, and arm CD remains vertical. What is the acceleration of part D?

<img src = "figs\02_planar_kinematics_accel\Q8.jpg" width="50%"> <br>

### Answer

$$ a_D = -0.135i-0.144j+0k \text{ m/s}^2 $$


## Question 9

The disk of radius 300 mm rolls without slipping on the flat surface. Its centre A is moving toward the right and accelerating toward the right. The magnitude of the velocity of point C is 2 m/s, and the magnitude of the acceleration of point C is 14 m/s $^2$. Determine the angular acceleration of the disk.

<img src = "figs\02_planar_kinematics_accel\Q9.jpg" width="50%"> <br>

### Answer 

$$ 0i + 0j - 20.0k \text{ rad/s}^2 $$

i.e. 20.0 rad/s $^2$ clockwise.

## Question 10

The disk of radius 0.4 m rolls without slipping on the fixed circular surface of radius 1.2 m, with a constant clockwise angular velocity of 1 rad/s. What are the accelerations of points A and B?

<img src = "figs\02_planar_kinematics_accel\Q10.jpg" width="50%"> <br>

### Answer

$$ a_A=0i-0.5j+0k\text{ m/s}^2  $$

$$ a_B=0i+0.3j+0k\text{ m/s}^2  $$

<br><br>

