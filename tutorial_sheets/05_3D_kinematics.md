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


# Tutorial Sheet 5: 3D Kinematics 

**Topics covered are:**
- 3D velocity and acceleration
- Reference frames

**Tips**
- Cross products will get much larger - the order of calculation matters, and you will need to use the full version of the acceleration equations.
- Mechanisms are now in 3D, so practice visualisiing the actual movements to avoid mistakes.
- Some will like to use column vectors, write it how you feel works best for you!

<br>

## Question 1 

The aeroplane’s angular velocity vector relative to an earth-fixed reference frame, expressed in terms of the body-fixed coordinate system shown, is $\omega$ = 0.62i+0.45j−0.23k rad/s. The coordinates of point A of the airplane are (3.6, 0.8, −1.2) m. What is the velocity of point A relative to the velocity of the aeroplane’s center of mass?

<img src = "figs\05_3D_kinematics\Q1.jpg" width="50%"> <br>

### Answer

$$ -0.356i-0.084j-1.12k \text{ m/s}$$

## Question 2 

The angular velocity of the cube relative to the primary reference frame, expressed in terms of the body-fixed coordinate system shown is $\omega$=−6.4i+8.2j+12k rad/s.The velocity of the center of mass G of the cube relative to the primary reference frame at the instant shown is $v_G$=26i+14j+32k m/s. What is the velocity of point A of the cube relative to the primary reference frame at the instant shown?

<img src = "figs\05_3D_kinematics\Q2.jpg" width="50%"> <br>

### Answer

v_A = 22.2i+32.4j+17.4k \text{ m/s}$$


## Question 3

Using the cube in Q2, the coordinate system shown is fixed with respect to the cube. The angular velocity of the cube relative to the primary reference frame, $\omega$=−6.4i+8.2j+12k rad/s, is constant.The acceleration of the center of mass G of the cube relative to the primary reference frame at the instant shown is $a_G$=136i+76j−48k m/s $^2$. What is the acceleration of point A of the cube relative to the primary reference frame at the instant shown?

### Answer

$$
v_A = -204.5i-63.04j-125k \text{ m/s}
$$

## Question 4

The origin of the secondary coordinate system shown is fixed to the center of mass G of the cube. The velocity of the center of mass G of the cube relative to the primary reference frame at the instant shown is $v_G$=26i+14j+32 m/s. The cube is rotating relative to the secondary coordinate system with  angular velocity $\omega_{rel}$ =6.2i−5j+8.8k rad/s. The secondary coordinate system is rotating relative to the primary reference frame with angular velocity 2.2i+4j−3.6k rad/s.

**(a)** What is the velocity of point A of the cube relative to the primary reference frame at the instant shown? <br>
**(b)** If the components of the vectors $\omega_{rel}$ and are constant, what is the cube’s angular acceleration relative to the primary reference frame?

<img src = "figs\05_3D_kinematics\Q2.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ v_A = 19.8i+10.8j+41.4k \text{ m/s}$$

**(b)**

$$ \alpha = 17.2i-41.7j-35.8k \text{ rad/s}^2$$ 


## Question 5

Relative to an earth-fixed reference frame, points A and B of the rigid parallelepiped are fixed and it rotates about the axis AB with an angular velocity of 30 rad/s. Determine the velocities of points C and D relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q5.jpg" width="50%"> <br>

### Answer

$$ v_C = 4i+4k, v_D = 4i-8j $$

## Question 6

Using the parallelepiped in Q5, relative to the xyz coordinate system shown, points A and B of the rigid parallelepiped are fixed and the parallelepiped rotates about the axis AB with an angular velocity of 30 rad/s. Relative to an earth fixed reference frame, point A is fixed and the xyz coordinate system rotates with angular velocity −5i+8j+6k rad/s. Determine the velocities of points C and D relative to the earth-fixed reference frame.

### Answer

$$ 
v_C = 2.8i+3k, v_D = 2.8i-5.6j-4.2k
$$

## Question 7

Relative to an earth-fixed reference frame, the vertical shaft rotates about its axis with angular velocity $\omega_O$=4 rad/s. The secondary xyz coordinate system is fixed with respect to the shaft and its origin is stationary. Relative to the secondary coordinate system, the disk (radius 8 cm) rotates with constant angular velocity $\omega_d$=6 rad/s. At the instant shown, determine the velocity of point A

**(a)** Relative to the secondary reference frame.<br>
**(b)** Relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q7.jpg" width="50%"> <br>

### Answer

**(a)**

$$ v_A = -33.9j+33.9k \text{ cm/s} $$

**(b)**

$$ v_A = 22.6i-33.9j+33.9k \text{ cm/s} $$

## Question 8 
The object in figure (a) is supported by bearings at A and B in figure (b). The horizontal circular disk is supported by a vertical shaft that rotates with angular velocity $\omega_O$=6 rad/s. The horizontal bar rotates with angular velocity $\omega$=10 rad/s. At the instant shown,

**(a)** What is the velocity relative to an earth-fixed reference frame of the end C of the vertical bar? <br>
**(b)** What is the angular acceleration vector of the object relative to an earth-fixed reference frame? <br>
**(c)** What is the acceleration relative to an earth-fixed reference frame of the end C of the vertical bar?

<img src = "figs\05_3D_kinematics\Q8.jpg" width="50%"> <br>

### Answer

**(a)**

$$ v_C = 0.4k \text{ m/s} $$

**(b)**

$$ \alpha = -60k \text{ rad/s}^2 $$

**(c)**

$$ a_C = 8.4i-10j \text{ m/s}^2 $$

## Question 9 

The point of the spinning top remains at a fixed point on the floor, which is the origin O of the secondary reference frame shown. The top’s angular velocity vector relative to the secondary reference frame, $\omega_{rel}$=50k rad/s, is constant. The angular velocity vector of the secondary reference frame relative to an earth-fixed primary reference frame is $\omega$=2j+5.6k rad/s. The components of this vector are constant. (Notice that it is expressed in terms of the secondary reference frame.) 

**(a)** Determine the velocity relative to the earth-fixed reference frame of the point of the top with coordinates (0, 20, 30) mm. <br>
**(b)** What is the top’s angular acceleration vector relative to the earth-fixed reference frame <br>
**(c)** Determine the acceleration relative to the earth fixed reference frame of the point of the top with coordinates (0, 20, 30) mm

<img src = "figs\05_3D_kinematics\Q9.jpg" width="50%"> <br>

### Answer

**(a)**

$$ v_A = -1.05i \text{ m/s} $$

**(b)**

$$ \alpha = 100i \text{ rad/s}^2 $$

**(c)**

$$ a_C = -61.4j+4.1k \text{ m/s}^2 $$

## Question 10

The radius of the circular disk is R=0.2 m, and b=0.3 m. The disk rotates with angular velocity $\omega_d$=6 rad/s relative to the horizontal bar. The horizontal bar rotates with angular velocity $\omega_b$=4 rad/s relative to the vertical shaft, and the vertical shaft rotates with angular velocity $\omega_O$=2 rad/s relative to an earth-fixed reference frame. Assume that the secondary reference frame shown is fixed with respect to the horizontal bar.

**(a)** What is the angular velocity vector $\omega_{rel}$ of the disk relative to the secondary reference frame? <br>
**(b)** Determine the velocity relative to the earth-fixed reference frame of point P, which is the uppermost point of the disk.

<img src = "figs\05_3D_kinematics\Q10.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ \omega_{rel} =  6i \text{ rad/s}$$

**(b)** 

$$ v_P = -0.8i+1.2j+0.6k \text{ m/s} $$

<br><br>

