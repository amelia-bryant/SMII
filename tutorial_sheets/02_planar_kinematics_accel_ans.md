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


# Tutorial Sheet 2: Planar Kinematics with Acceleration Answers 

**Topics covered are**
- Acceleration in 2D 
- Relative accelerations

**Tips**
- The questions start tp get quite wordy. Drawing it all out helps!
- Because we are dealing with 2D planar motion, it does not matter which relative acceleration formula we use - the one using $\omega\times\omega$ or $\omega^2$. When expanding to 3D, only $\omega\times\omega$ works, but for the moment $\omega^2$ is faster. 

<br>

## Question 1 

The rigid body rotates about the z axis with counterclockwise angular velocity ω = 4 rad/s and counterclockwise angular acceleration α = 2 rad/s $^2$. The distance $r_{A/B}$ = 0.6m.  

**(a)** What are the rigid body’s angular velocity and angular acceleration vectors? <br> 
**(b)** Determine the acceleration of point A relative to point B.

<img src = "figs\02_planar_kinematics_accel\Q1.jpg" width="50%"> <br>

### Answer

**(a)** Using the thumb rule, both are positive hence 

$$ \omega = 4k \\ \alpha = 2k $$

**(b)** 

$$a_{A/B}=a_B+\alpha\times r_{A/B}+\omega\times(\omega\times r_{A/B}) \\ a_{A/B}=0+2k\times 0.6i+4k\times(4k\times 0.6i) \\ a_{A/B} = -9.6i+1.2j \text{ m/s}^2 $$

or 

$$a_{A/B}=a_B+\alpha\times r_{A/B}-\omega^2 r_{A/B} \\ a_{A/B}=0+2k\times 0.6i - 4^2. 0.6i \\ a_{A/B} = -9.6i+1.2j \text{ m/s}^2 $$

## Question 2

The helicopter is in planar motion in the xy plane. At the instant shown, the position of its center of mass G is x=2 m, y=2.5 m, its velocity is $v_G$ = 12i + 4j m/s, and its acceleration is $a_G$ = 2i + 3j m/s $^2$. The position of point T where the tail rotor is mounted is x=-3.5 m, y=4.5 m. The helicopter’s angular velocity is 0.2 rad/s clockwise, and its angular acceleration is 0.1 rad/s $^2$ counter-clockwise.

What is the acceleration of point T?

<img src = "figs\02_planar_kinematics_accel\Q2.jpg" width="50%"> <br>

### Answer

Draw it out

<img src = "figs\02_planar_kinematics_accel\Q2ans.jpg" width="50%"> <br>

It then follows

$$ a_{T}=a_G+\alpha\times r_{T/G}-\omega^2 r_{T/G} \\ 
a_{T}=2i+3j+\begin{vmatrix}
i & j & k\\
0 & 0 & 0.1 \\
-5.5 & 2 & 0
\end{vmatrix} -0.2^2(-5.5i+2j) \\ a_T= 2.02i+2.37j \text{ m/s}^2$$

## Question 3

The bar rotates with a counterclockwise angular velocity of 5 rad/s and a counterclockwise angular acceleration of 30 rad/s $^2$. Determine the acceleration of A using $ a_{A}=a_B+\alpha\times r_{A/B}+\omega\times(\omega\times r_{A/B}) $.

<img src = "figs\02_planar_kinematics_accel\Q3.jpg" width="50%"> <br>

### Answer

For this question, you use the full expansion version of the equation meaning a lot of cross products! 

Assuming B as the axis of rotation

$$ a_{A}=a_B+\alpha\times r_{A/B}+\omega\times(\omega\times r_{A/B})  \\
a_A = \begin{vmatrix}
i & j & k\\
0 & 0 & 30 \\
2\cos(30) & 2\sin(30) & 0
\end{vmatrix} + 5k\times 
\begin{vmatrix}
i & j & k\\
0 & 0 & 5 \\
2\cos(30) & 2\sin(30) & 0
\end{vmatrix} \\
= -30i+52j+ \begin{vmatrix}
i & j & k\\
0 & 0 & 5 \\
-5 & 8.66 & 0
\end{vmatrix} \\
= -73.3i+27j \text{ m/s}^2
$$

## Question 4

If $\omega_{AB}$=2rad/s, $\alpha_{AB}$=2rad/s $^2$, $\omega_{BC}$=−1rad/s, and $\alpha_{BC}$=−4rad/s $^2$, what is the acceleration of point C where the scoop of the excavator is attached?

<img src = "figs\02_planar_kinematics_accel\Q4.jpg" width="50%"> <br>

### Answer

The acceleration of B is

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\
0+\begin{vmatrix}
i & j & k\\
0 & 0 & 2 \\
3 & 3.9 & 0
\end{vmatrix} - 2^(3i+3.9j) \\\ = -19.8i-9.6j \text{ m/s} ^2 $$


$$ a_{C}=a_B+\alpha_{BC}\times r_{C/B}-\omega_{BC}^2 r_{C/B} \\ 
-19.8i-9.6j +\begin{vmatrix}
i & j & k\\
0 & 0 & -4 \\
2.3 & -0.5 & 0
\end{vmatrix} - 1^2(2.3i-0.5j) \\\ = -24.1i-18.3j \text{ m/s} ^2 $$

## Question 5

The length of the bar is L = 4 m and the angle $\theta$ = 30°. The bar’s angular velocity is $\omega$ = 1.8 rad/s and its angular acceleration is $\alpha$ = 6 rad/s $^2$. The endpoints of the bar slide on the plane surfaces. Determine the acceleration of the midpoint G.

<img src = "figs\02_planar_kinematics_accel\Q5.jpg" width="50%"> <br>

### Answer

Drawing and labelling the situation calling the top point A and bottom B

<img src = "figs\02_planar_kinematics_accel\Q5ans.jpg" width="50%"> <br>

Solve, taking into account the constraints of the movements imparted by the walls and floor

$$ a_{A}=a_B+\alpha\times r_{A/B}-\omega^2 r_{A/B} \\ = a_B + \begin{vmatrix}
i & j & k\\
0 & 0 & 6 \\
-4\cos(60) & 4\sin(60) & 0
\end{vmatrix} - 1.8^2(-4\cos(60)i+ 4\sin(60)j) \\ a_Aj = a_Bi - 14.28i -23.21j $$

Equating components

$$ (i) 0 = a_B -14.28 \rightarrow a_B=14.28 \text{ m/s} ^2\\ 
(j) a_A = -23.21 \rightarrow a_A=-23.21 \text{ m/s} ^2 $$

Now we can use either points to work out G

$$ a_{G}=a_A+\alpha\times r_{G/A}-\omega^2 r_{G/A} \\ a_G= -23.21j + \begin{vmatrix}
i & j & k\\
0 & 0 & 6 \\
2\cos(60) & -2\sin(60) & 0
\end{vmatrix} - 1.8^2(2\cos(60)i-2\sin(60)j) \\ a_G = 7.15i-11.6 \text{ m/s} ^2 $$


## Question 6

The angular velocity's magnitude $\omega_{AB}$ = 6 rad/s. If the acceleration of the slider C is zero at the instant shown, what is the angular acceleration $\alpha_{AB}$?

<img src = "figs\02_planar_kinematics_accel\Q6.jpg" width="50%"> <br>

### Answer

To find the acceleration, we need to know all angular velocities

$$ v_B = v_A + \omega_{AB} \times r_{B/A} \\ = 0+ -6k\times(0.04i+0.04j)\\=0.24i-0.24j$$

$$ v_C = v_B + \omega_{BC} \times r_{C/B} \\ = 0.24i-0.24j + \omega_{BC} k\times(0.1i-0.07j)\\= (0.24+0.07\omega_{BC})i+(0.24+0.1\omega_{BC})j$$

Component analysis (remember C cannot move in i)

$$ (j) 0 = 0.24 + 0.1\omega_{BC} \rightarrow \omega_{BC}=-2.4 \text{ m/s}$$

From here we can find the acceleration by finding two different expressions for the movement of B; note becuase of the diagram we have put $\alpha_{AB}$ as negative

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\ 
= 0- \alpha_{AB}k\times(0.04i+0.04j)-6^2(0.04i+0.04j) \\ a_{B}= (0.04 \alpha_{AB}-1.44)i+(-0.04\alpha_{AB}-1.44)j $$

$$ a_{B}=a_C+\alpha_{BC}\times r_{B/C}-\omega_{BC}^2 r_{B/C} \\ 
= 0- \alpha_{BC}k\times(-0.1i+0.07j)-(-2.4)^2(-0.1+0.07j) \\ a_{B}= (-0.07\alpha_{BC}+0.576)i+(-0.1\alpha_{BC}-0.4)j $$

Set components equal

$$ (i) 0.04 \alpha_{AB}-1.44 = -0.07\alpha_{BC}+0.576 \\ 0.04\alpha_{AB}+0.07\alpha_{BC}=2.016 \\ (j) -0.04\alpha_{AB}-1.44 = -0.1\alpha_{BC}-0.4 \\ -0.04\alpha_{AB}+0.1\alpha_{BC}=1.037 $$

Via simultaneous equations

$$ \alpha_{AB}=19 \text{ m/s} ^2 \text{ clockwise}$$

## Question 7

At the instant shown, the piston’s velocity and acceleration are $v_C$ =−14i m/s and $a_C$ = −2200i m/s $^2$. What is the angular acceleration of the crank AB?

<img src = "figs\02_planar_kinematics_accel\Q7.jpg" width="50%"> <br>

### Answer

Similar to the last question, we can use the fact C can only move in i and that we need to solve for $\omega $ first

$$ v_B=v_A +\omega_{AB} \times r_{B/A} \\ 0+\omega_{AB}k \times (0.05i+0.05j) \\ = -0.05 \omega_{AB}i + 0.05 \omega_{AB}j$$

$$v_B=v_C +\omega_{BC} \times r_{B/C} \\ -14i+\omega_{BC}k \times (0.175i-0.05j) \\ = -14i -0.05 \omega_{BC}i -0.175 \omega_{BC}j$$

Then analyse looking at each component of velocity

$$(i) -0.05 \omega_{AB}+0.05 \omega_{BC} =-14 \\ (j) 0.05 \omega_{AB}=-0.175 \omega_{BC} $$ 

And using simultaneous equations

$$ \omega_{AB}=218 \text{ rad/s, } \omega_{BC}=-62.2 \text{ rad/s} $$

This time I will solve it in a slightly different way, instead of finding two expressions for $a_B$, finding $a_B$ and using it as the reference point to find $a_C$. Both ways work so use whichever is most intuitive to you!

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\ = 0+\alpha_{AB}k\times(0.05i+0.05j)-218^2(0.05i+0.05j) \\ = (-0.05\alpha_{AB}-2376)i+(0.05\alpha_{AB}-2376)j $$

Then using this as the reference point to find C

$$ a_{C}=a_B+\alpha_{BC}\times r_{C/B}-\omega_{BC}^2 r_{C/B} \\
-2200i = (-0.05\alpha_{AB}-2376)i+(0.05\alpha_{AB}-2376)j+ \alpha_{BC}k\times(0.175i-0.05j)-(-62.2)^2(0.175i-0.05j) \\ 
-2200i= (-0.05\alpha_{AB}-2376 + 0.05\alpha_{BC}-678)i+(0.05\alpha_{AB}-2376+0.175\alpha_{BC}+193)j $$

Equating components

$$ (i) -2200=-0.05\alpha_{AB}+ 0.05\alpha_{BC}-3054\\ (j) 0= 0.05\alpha_{AB}+0.175\alpha_{BC}-2183 $$

Solving we find

$$ \alpha_{AB}=-3580 \text{ rad/s}^2 $$

Hence AB rotates 3580 rad/s $^2 $ clockwise.

## Question 8

If arm AB has a constant clockwise angular velocity of 0.8 rad/s, arm BC has a constant angular velocity of 0.2 rad/s, and arm CD remains vertical, what is the acceleration of part D?

<img src = "figs\02_planar_kinematics_accel\Q8.jpg" width="50%"> <br>

### Answer

Because both AB and BC have constant angular velocity, $\alpha = 0$ for both. 

Acceleration of B can be expressed as

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\ 
= 0+0\times (0.3\cos(50)i+0.3\sin(50)) - 0.8^2(0.3\cos(50)i+0.3\sin(50)j) \\
= 0.123i-0.147j $$

Acceleration of C can be expressed as

$$ a_{C}=a_B+\alpha_{BC}\times r_{C/B}-\omega_{BC}^2 r_{C/B} \\ 
= 0.123i-0.147j + 0\times (0.3\cos(15)i+0.3\sin(15)) - 0.8^2(0.3\cos(15)i+0.3\sin(15)j) \\ = -0.135i-0.144j $$

Given CD remains vertical, it is just translating the same as point D 

$$ \alpha_C=\alpha_D= -0.135i-0.144j \text{ m/s}^2$$

## Question 9

Point A of the rolling disk is moving toward the right and accelerating toward the right. The magnitude of the velocity of point C is 2 m/s, and the magnitude of the acceleration of point C is 14 m/s $^2$. Determine the angular acceleration of the disk.

<img src = "figs\02_planar_kinematics_accel\Q9.jpg" width="50%"> <br>

### Answer 

<img src = "figs\02_planar_kinematics_accel\Q9ans.jpg" width="50%"> <br>

First find the velocity of the centre of the disk. because it is rolling, it only has i component, hence

$$ v_a=r\omega i $$

Next find velocity of C. Intruitivley this must only have j velocity component meaning the velocity must be 

$$ v_C = r\omega i + r\omega j$$

But we can prove it mathematically with

$$
v_C = v_A + r\times\omega \\ = r\omega i + \begin{vmatrix}
i & j & k\\
0 & 0 & -\omega \\
-0.3 & 0 & 0
\end{vmatrix}  = r\omega i + r\omega j
$$

From here, we know the magnitude of velocity of C is 2 so we can calculate the angular velocity using basic absolute value vector calculations


$$ 2=  \sqrt{(r\omega)^2+(r\omega)^2} \\ 4= r^2 \omega^2+r^2 \omega^2 \\ 4 = 2r^2\omega^2 \\ 4 = 0.18\omega^2 \\ \omega = 4.71 \text{ rad/s} $$

Then use a similar method to find angular acceleration

$$ a_{C}=a_A+\alpha\times r_{C/A}-\omega^2 r_{C/A} \\
a_{C}=0.3\alpha i+\begin{vmatrix}
i & j & k\\
0 & 0 & -\alpha \\
-0.3 & 0 & 0
\end{vmatrix}-|4.71|^2 (-0.3) \\ 
a_C = 0.3\alpha i +  6.66 i + 0.3\alpha j$$

Now for the magnitude

$$ 14 =  \sqrt{(0.3\alpha+6.6)^2+0.3\alpha^2} $$

Expanding and solving the equation

$$ \alpha = 20 \text{ m/s}^2 \text { in the negative direction} $$

## Question 10

The disk rolls on the circular surface with a constant clockwise angular velocity of 1 rad/s. What are the accelerations of points A and B?

<img src = "figs\02_planar_kinematics_accel\Q10.jpg" width="50%"> <br>

### Answer

First find the acceleration of the center of the disk (call it O). There is an instantaneous center where the circle meets the ground so 

$$ v_B=0 \\ 
v_0=v_B+\omega k \times r_{O/B} = -1k \times 0.4j \\ v_O = 0.4i$$

The speed of the disk along the circular path is not changing. Remember O is moving on a circular path with radius 1.6 m total. We can use the normal acceleration formula from the centre of the system.

$$ a_O = \frac{v_O^2}{r} = \frac{-0.16}{0.4+1.2} \\ = -0.1\text{ m/s}^2 \text{ in the j direction}$$

We don't use $a_n=r\omega$ in this situation as this is used for calculating normal acceleration at the rim due to a disk's angular velocity (essentially projecting a different frame and center) whereas we are finding simply the linear velocity along a circular path.

Then A can be found with 

$$ a_A = a_O+\alpha\times r_{A/O}-\omega^2 r_{A/O} \\  
a_A = -0.1j+0-1^2(0.4j) \\ a_A=-0.5j\text{ m/s}^2  $$

And B

$$ a_B = a_O+\alpha\times r_{B/O}-\omega^2 r_{B/O} \\  
a_A = -0.1j+0-1^2(-0.4j) \\ a_A=0.3j\text{ m/s}^2  $$

<br><br>



