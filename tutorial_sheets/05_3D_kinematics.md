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
- Notation: $\Omega$ is the angular velocity of the secondary (xyz) reference frame, $\omega_{rel}$ is a body's angular velocity relative to that frame, and $\omega = \Omega + \omega_{rel}$ is the body's angular velocity relative to the primary (earth-fixed) reference frame.
- Cross products get much larger in 3D. Keep the vectors in the right order ($\omega \times r$, not $r \times \omega$), and work out $\omega \times (\omega \times r)$ from the inside out.
- Use the full acceleration equations: in 3D, $\omega \times (\omega \times r)$ equals $-\omega^2 r$ only when $r$ is perpendicular to $\omega$.
- A vector whose components are constant in a turning frame still changes, at the rate $\Omega \times$ (the vector). This is why a body can have an angular acceleration even when every rate is constant (Q4, Q8 and Q9).
- Mechanisms are now in 3D, so practise visualising the actual movements to avoid mistakes.
- Some will like to use column vectors; write it however works best for you!

<br>

## Question 1 

The aeroplane’s angular velocity vector relative to an earth-fixed reference frame, expressed in terms of the body-fixed coordinate system shown, is $\omega$ = 0.62i+0.45j−0.23k rad/s. The origin of the coordinate system is at the aeroplane’s centre of mass G. The coordinates of point A of the aeroplane are (3.6, 0.8, −1.2) m. What is the velocity of point A relative to the centre of mass, $v_A - v_G$?

<img src = "figs\05_3D_kinematics\Q1.jpg" width="50%"> <br>

### Answer

$$ v_A - v_G = -0.356i-0.084j-1.12k \text{ m/s}$$

## Question 2 

The angular velocity of the cube relative to the primary reference frame, expressed in terms of the body-fixed coordinate system shown, is $\omega$=−6.4i+8.2j+12k rad/s. The velocity of the centre of mass G of the cube relative to the primary reference frame at the instant shown is $v_G$=26i+14j+32k m/s. What is the velocity of point A of the cube relative to the primary reference frame at the instant shown?

<img src = "figs\05_3D_kinematics\Q2.jpg" width="50%"> <br>

### Answer

$$ v_A = 22.2i+32.4j+17.4k \text{ m/s}$$


## Question 3

Using the cube in Q2, the coordinate system shown is fixed with respect to the cube. The angular velocity of the cube relative to the primary reference frame, $\omega$=−6.4i+8.2j+12k rad/s, is constant. The acceleration of the centre of mass G of the cube relative to the primary reference frame at the instant shown is $a_G$=136i+76j−48k m/s². What is the acceleration of point A of the cube relative to the primary reference frame at the instant shown?

### Answer

$$
a_A = -204.5i-63.0j-134.6k \text{ m/s}^2
$$

## Question 4

The origin of the secondary coordinate system shown is fixed to the centre of mass G of the cube. The velocity of the centre of mass G of the cube relative to the primary reference frame at the instant shown is $v_G$=26i+14j+32k m/s. The cube is rotating relative to the secondary coordinate system with angular velocity $\omega_{rel}$=4.8i+6j−2.4k rad/s. The secondary coordinate system is rotating relative to the primary reference frame with angular velocity $\Omega$=−1.6i+3j+5.2k rad/s. Both vectors are expressed in terms of the secondary coordinate system.

**(a)** What is the velocity of point A of the cube relative to the primary reference frame at the instant shown? <br>
**(b)** If the components of $\omega_{rel}$ and $\Omega$ in the secondary coordinate system are constant, what is the cube’s angular acceleration relative to the primary reference frame?

<img src = "figs\05_3D_kinematics\Q2.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ v_A = 32.2i+13.6j+26.2k \text{ m/s}$$

**(b)**

$$ \alpha = -38.4i+21.1j-24.0k \text{ rad/s}^2$$ 


## Question 5

Relative to an earth-fixed reference frame, points A and B of the rigid parallelepiped are fixed and it rotates about the axis AB with an angular velocity of 30 rad/s, in the direction shown (anticlockwise when viewed from B looking towards A). Determine the velocities of points C and D relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q5.jpg" width="50%"> <br>

### Answer

$$ v_C = 4i+4k \text{ m/s}, \quad v_D = 4i-8j \text{ m/s} $$

## Question 6

Using the parallelepiped in Q5, relative to the xyz coordinate system shown, points A and B of the rigid parallelepiped are fixed and the parallelepiped rotates about the axis AB with an angular velocity of 30 rad/s, in the direction shown. Relative to an earth-fixed reference frame, point A is fixed and the xyz coordinate system rotates with angular velocity $\Omega$=−5i+8j+6k rad/s. Determine the velocities of points C and D relative to the earth-fixed reference frame.

### Answer

$$ 
v_C = 2.8i+3k \text{ m/s}, \quad v_D = 2.8i-5.6j-4.2k \text{ m/s}
$$

## Question 7

Relative to an earth-fixed reference frame, the vertical shaft rotates about its axis with angular velocity $\omega_O$=4 rad/s. The secondary xyz coordinate system is fixed with respect to the shaft, and its origin O, at the centre of the disc, is stationary. Relative to the secondary coordinate system, the disc (radius 8 cm) rotates with constant angular velocity $\omega_d$=6 rad/s. At the instant shown, determine the velocity of point A:

**(a)** relative to the secondary coordinate system;<br>
**(b)** relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q7.jpg" width="50%"> <br>

### Answer

**(a)**

$$ v_{Arel} = -33.9j+33.9k \text{ cm/s} $$

**(b)**

$$ v_A = 22.6i-33.9j+33.9k \text{ cm/s} $$

## Question 8 
The object in figure (a) is supported by bearings at A and B in figure (b), which are fixed to the horizontal circular disc. The disc is supported by a vertical shaft that rotates with constant angular velocity $\omega_O$=6 rad/s. The horizontal bar rotates relative to the disc with constant angular velocity $\omega_b$=10 rad/s. The xyz coordinate system is fixed to the disc. At the instant shown:

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

The point of the spinning top remains at a fixed point on the floor, which is the origin O of the secondary reference frame shown. The top’s angular velocity vector relative to the secondary reference frame, $\omega_{rel}$=50k rad/s, is constant. The angular velocity vector of the secondary reference frame relative to an earth-fixed primary reference frame is $\Omega$=2j+5.6k rad/s. The components of this vector are constant. (Notice that it is expressed in terms of the secondary reference frame.) Point A of the top has coordinates (0, 20, 30) mm.

**(a)** Determine the velocity of point A relative to the earth-fixed reference frame. <br>
**(b)** What is the top’s angular acceleration vector relative to the earth-fixed reference frame? <br>
**(c)** Determine the acceleration of point A relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q9.jpg" width="50%"> <br>

### Answer

**(a)**

$$ v_A = -1.05i \text{ m/s} $$

**(b)**

$$ \alpha = 100i \text{ rad/s}^2 $$

**(c)**

$$ a_A = -61.5j+4.10k \text{ m/s}^2 $$

## Question 10

The radius of the circular disc is R=0.2 m, and b=0.3 m. The disc rotates with angular velocity $\omega_d$=6 rad/s relative to the horizontal bar. The bar is pinned to the top of the vertical shaft and rotates relative to the shaft about the pin (the z axis) with angular velocity $\omega_b$=4 rad/s, and the vertical shaft rotates with angular velocity $\omega_O$=2 rad/s relative to an earth-fixed reference frame. Assume that the secondary reference frame shown is fixed with respect to the horizontal bar.

**(a)** What is the angular velocity vector $\omega_{rel}$ of the disc relative to the secondary reference frame? <br>
**(b)** At the instant shown, determine the velocity relative to the earth-fixed reference frame of point P, which is the uppermost point of the disc.

<img src = "figs\05_3D_kinematics\Q10.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ \omega_{rel} =  6i \text{ rad/s}$$

**(b)** 

$$ v_P = -0.8i+1.2j+0.6k \text{ m/s} $$

## Question 11

A small collar P slides up the vertical bar of the object in Q8, towards C, at a constant speed of 0.2 m/s relative to the bar. At the instant shown the collar is halfway up the vertical bar. The disc and the bar turn at the constant rates given in Q8. Determine:

**(a)** the velocity of the collar relative to an earth-fixed reference frame; <br>
**(b)** the acceleration of the collar relative to an earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q8.jpg" width="50%"> <br>

### Answer

**(a)**

$$ v_P = 0.2j-0.1k \text{ m/s} $$

**(b)**

$$ a_P = 2.4i-5j+4k \text{ m/s}^2 $$

<br><br>

