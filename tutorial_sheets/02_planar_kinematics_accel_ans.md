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
- The questions start to get quite wordy. Drawing it all out helps!
- Counterclockwise is taken as positive (the +k direction). All vectors on this sheet are written with all three components, e.g. $\omega = 0i + 0j + 2k \;\;\text{rad/s}$ rather than $2k \;\;\text{rad/s}$, so every cross product can be set up as a determinant.
- In 2D planar motion $\omega$ is always perpendicular to $r$, so $\omega\times(\omega\times r) = -\omega^2 r$ and it does not matter which form of the relative acceleration equation we use. When expanding to 3D, only $\omega\times(\omega\times r)$ works, but for the moment $-\omega^2 r$ is faster. 

<br>

## Question 1 

The rigid body rotates about the z axis with counterclockwise angular velocity ω = 4 rad/s and counterclockwise angular acceleration α = 2 rad/s $^2$. Point B lies on the axis of rotation and the distance $r_{A/B}$ = 0.6 m.  

**(a)** What are the rigid body’s angular velocity and angular acceleration vectors? <br> 
**(b)** Determine the acceleration of point A relative to point B.

<img src = "figs\02_planar_kinematics_accel\Q1.jpg" width="50%"> <br>

### Answer

**(a)** Both are counterclockwise, so by the right-hand rule both point in the +z direction

$$ \omega = 0i + 0j + 4k \quad \text{rad/s} \\ \alpha = 0i + 0j + 2k \quad \text{rad/s}^2 $$

**(b)** The acceleration of A relative to B is

$$ a_{A/B} = a_A - a_B = \alpha\times r_{A/B}+\omega\times(\omega\times r_{A/B}) $$

with $r_{A/B} = 0.6i + 0j + 0k \;\;\text{m}$. Taking each term in turn

$$ \alpha\times r_{A/B} = \begin{vmatrix}
i & j & k\\
0 & 0 & 2 \\
0.6 & 0 & 0
\end{vmatrix} \\
= i[(0)(0)-(2)(0)] - j[(0)(0)-(2)(0.6)] + k[(0)(0)-(0)(0.6)] \\
= 0i + 1.2j + 0k $$

$$ \omega\times r_{A/B} = \begin{vmatrix}
i & j & k\\
0 & 0 & 4 \\
0.6 & 0 & 0
\end{vmatrix} = 0i + 2.4j + 0k \\
\omega\times(\omega\times r_{A/B}) = \begin{vmatrix}
i & j & k\\
0 & 0 & 4 \\
0 & 2.4 & 0
\end{vmatrix} = -9.6i + 0j + 0k $$

Adding them

$$ a_{A/B} = -9.6i+1.2j+0k \quad \text{m/s}^2 $$

or, using the planar form,

$$ a_{A/B} = \alpha\times r_{A/B}-\omega^2 r_{A/B} \\ a_{A/B} = (0i + 1.2j + 0k) - 4^2(0.6i + 0j + 0k) \\ a_{A/B} = -9.6i+1.2j+0k \quad \text{m/s}^2 $$

Because B is on the axis of rotation, $a_B = 0$, so this is also the acceleration of A.

## Question 2

The helicopter is in planar motion in the xy plane. At the instant shown, the position of its center of mass G is x = 2 m, y = 2.5 m, its velocity is $v_G = 12i + 4j + 0k \;\;\text{m/s}$, and its acceleration is $a_G = 2i + 3j + 0k \;\;\text{m/s}^2$. The position of point T where the tail rotor is mounted is x = -3.5 m, y = 4.5 m. The helicopter’s angular velocity is 0.2 rad/s clockwise, and its angular acceleration is 0.1 rad/s $^2$ counterclockwise.

What is the acceleration of point T?

<img src = "figs\02_planar_kinematics_accel\Q2.jpg" width="50%"> <br>

### Answer

Draw it out

<img src = "figs\02_planar_kinematics_accel\Q2ans.jpg" width="50%"> <br>

Writing the vectors in full

$$ r_{T/G} = (-3.5-2)i + (4.5-2.5)j + 0k = -5.5i + 2j + 0k \quad \text{m} \\
\omega = 0i + 0j - 0.2k \quad \text{rad/s} \\
\alpha = 0i + 0j + 0.1k \quad \text{rad/s}^2 $$

It then follows

$$ a_{T}=a_G+\alpha\times r_{T/G}-\omega^2 r_{T/G} \\ 
a_{T}=(2i+3j+0k)+\begin{vmatrix}
i & j & k\\
0 & 0 & 0.1 \\
-5.5 & 2 & 0
\end{vmatrix} -0.2^2(-5.5i+2j+0k) \\
a_T = (2i+3j+0k) + (-0.2i-0.55j+0k) + (0.22i-0.08j+0k) \\
a_T= 2.02i+2.37j+0k \quad \text{m/s}^2$$

Note that $v_G$ is not needed: the acceleration of T only depends on $a_G$, $\alpha$ and $\omega$.

## Question 3

The bar rotates about the fixed pin B at its lower end with a counterclockwise angular velocity of 5 rad/s and a counterclockwise angular acceleration of 30 rad/s $^2$. Determine the acceleration of the end A using $ a_{A}=a_B+\alpha\times r_{A/B}+\omega\times(\omega\times r_{A/B}) $.

<img src = "figs\02_planar_kinematics_accel\Q3.jpg" width="50%"> <br>

### Answer

For this question, you use the full expansion version of the equation meaning a lot of cross products! 

B is a fixed pin, so $a_B = 0i + 0j + 0k$. The other vectors are

$$ r_{A/B} = 2\cos(30)i + 2\sin(30)j + 0k = 1.732i + 1j + 0k \quad \text{m} \\
\omega = 0i + 0j + 5k \quad \text{rad/s} \\
\alpha = 0i + 0j + 30k \quad \text{rad/s}^2 $$

Then

$$ a_{A}=a_B+\alpha\times r_{A/B}+\omega\times(\omega\times r_{A/B})  \\
a_A = 0 + \begin{vmatrix}
i & j & k\\
0 & 0 & 30 \\
1.732 & 1 & 0
\end{vmatrix} + (0i+0j+5k)\times 
\begin{vmatrix}
i & j & k\\
0 & 0 & 5 \\
1.732 & 1 & 0
\end{vmatrix} \\
= (-30i+51.96j+0k) + \begin{vmatrix}
i & j & k\\
0 & 0 & 5 \\
-5 & 8.66 & 0
\end{vmatrix} \\
= (-30i+51.96j+0k) + (-43.3i-25j+0k) \\
= -73.3i+27.0j+0k \quad \text{m/s}^2
$$

## Question 4

The body of the excavator is stationary, so point A is fixed. If $\omega_{AB}$ = 2 rad/s, $\alpha_{AB}$ = 2 rad/s $^2$, $\omega_{BC}$ = −1 rad/s, and $\alpha_{BC}$ = −4 rad/s $^2$ (counterclockwise positive), what is the acceleration of point C where the scoop of the excavator is attached?

<img src = "figs\02_planar_kinematics_accel\Q4.jpg" width="50%"> <br>

### Answer

Reading the positions from the figure, A = (4, 1.6) m, B = (7, 5.5) m and C = (9.3, 5) m, so

$$ r_{B/A} = 3i + 3.9j + 0k \quad \text{m} \\
r_{C/B} = 2.3i - 0.5j + 0k \quad \text{m} $$

and, with counterclockwise positive,

$$ \omega_{AB} = 0i + 0j + 2k \quad \text{rad/s}, \quad \alpha_{AB} = 0i + 0j + 2k \quad \text{rad/s}^2 \\
\omega_{BC} = 0i + 0j - 1k \quad \text{rad/s}, \quad \alpha_{BC} = 0i + 0j - 4k \quad \text{rad/s}^2 $$

A is fixed, so the acceleration of B is

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\
a_B = 0+\begin{vmatrix}
i & j & k\\
0 & 0 & 2 \\
3 & 3.9 & 0
\end{vmatrix} - 2^2(3i+3.9j+0k) \\
a_B = (-7.8i+6j+0k) - (12i+15.6j+0k) \\
a_B = -19.8i-9.6j+0k \quad \text{m/s}^2 $$

Then using B as the reference point

$$ a_{C}=a_B+\alpha_{BC}\times r_{C/B}-\omega_{BC}^2 r_{C/B} \\ 
a_C = (-19.8i-9.6j+0k) +\begin{vmatrix}
i & j & k\\
0 & 0 & -4 \\
2.3 & -0.5 & 0
\end{vmatrix} - (-1)^2(2.3i-0.5j+0k) \\
a_C = (-19.8i-9.6j+0k) + (-2i-9.2j+0k) + (-2.3i+0.5j+0k) \\
a_C = -24.1i-18.3j+0k \quad \text{m/s}^2 $$

## Question 5

The bar has length L = 4 m and makes an angle θ = 30° with the wall. Its upper end slides down the vertical wall and its lower end slides along the floor, and both ends stay in contact with these surfaces throughout the motion. At the instant shown, the bar’s angular velocity is ω = 1.8 rad/s and its angular acceleration is α = 6 rad/s $^2$, both counterclockwise. Determine the acceleration of the midpoint G.

<img src = "figs\02_planar_kinematics_accel\Q5.jpg" width="50%"> <br>

### Answer

Drawing and labelling the situation calling the top point A and bottom B

<img src = "figs\02_planar_kinematics_accel\Q5ans.jpg" width="50%"> <br>

Because the ends stay in contact with the surfaces, A can only move vertically and B can only move horizontally

$$ a_A = 0i + a_A j + 0k \\ a_B = a_B i + 0j + 0k $$

B is at (4 sin30, 0) = (2, 0) m and A is at (0, 4 cos30) = (0, 3.464) m, so

$$ r_{A/B} = -4\cos(60)i + 4\sin(60)j + 0k = -2i + 3.464j + 0k \quad \text{m} \\
\omega = 0i + 0j + 1.8k \quad \text{rad/s}, \quad \alpha = 0i + 0j + 6k \quad \text{rad/s}^2 $$

Relating A and B

$$ a_{A}=a_B+\alpha\times r_{A/B}-\omega^2 r_{A/B} \\
0i + a_A j + 0k = (a_B i + 0j + 0k) + \begin{vmatrix}
i & j & k\\
0 & 0 & 6 \\
-2 & 3.464 & 0
\end{vmatrix} - 1.8^2(-2i+3.464j+0k) \\
0i + a_A j + 0k = (a_B i + 0j + 0k) + (-20.78i-12j+0k) + (6.48i-11.22j+0k) \\
0i + a_A j + 0k = (a_B - 14.30)i - 23.22j + 0k $$

Equating components

$$ (i) \quad 0 = a_B -14.30 \rightarrow a_B=14.30 \text{ m/s}^2 \\ 
(j) \quad a_A = -23.22 \text{ m/s}^2 $$

A is accelerating down the wall. Now we can use either point to work out G; using A, with $r_{G/A} = 1i - 1.732j + 0k \;\;\text{m}$

$$ a_{G}=a_A+\alpha\times r_{G/A}-\omega^2 r_{G/A} \\
a_G= (0i-23.22j+0k) + \begin{vmatrix}
i & j & k\\
0 & 0 & 6 \\
1 & -1.732 & 0
\end{vmatrix} - 1.8^2(1i-1.732j+0k) \\
a_G = (0i-23.22j+0k) + (10.39i+6j+0k) + (-3.24i+5.61j+0k) \\
a_G = 7.15i-11.6j+0k \quad \text{m/s}^2 $$


## Question 6

Bar AB rotates about the fixed pin A with a clockwise angular velocity of magnitude $\omega_{AB}$ = 6 rad/s, and the slider C moves horizontally in its guide. If the acceleration of the slider C is zero at the instant shown, what is the angular acceleration $\alpha_{AB}$?

<img src = "figs\02_planar_kinematics_accel\Q6.jpg" width="50%"> <br>

### Answer

From the figure (converting cm to m)

$$ r_{B/A} = 0.04i + 0.04j + 0k \quad \text{m} \\
r_{C/B} = 0.1i - 0.07j + 0k \quad \text{m} \\
\omega_{AB} = 0i + 0j - 6k \quad \text{rad/s} $$

To find the acceleration, we first need all the angular velocities. A is fixed, so

$$ v_B = v_A + \omega_{AB} \times r_{B/A} \\
= 0 + \begin{vmatrix}
i & j & k\\
0 & 0 & -6 \\
0.04 & 0.04 & 0
\end{vmatrix} \\
= i[(0)(0)-(-6)(0.04)] - j[(0)(0)-(-6)(0.04)] + k[(0)(0.04)-(0)(0.04)] \\
= 0.24i-0.24j+0k \quad \text{m/s} $$

Taking $\omega_{BC} = 0i + 0j + \omega_{BC}k$

$$ v_C = v_B + \omega_{BC} \times r_{C/B} \\
= (0.24i-0.24j+0k) + \begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{BC} \\
0.1 & -0.07 & 0
\end{vmatrix} \\
= (0.24+0.07\omega_{BC})i+(-0.24+0.1\omega_{BC})j+0k $$

Component analysis (remember C can only move horizontally, so it has no j velocity)

$$ (j) \quad 0 = -0.24 + 0.1\omega_{BC} \rightarrow \omega_{BC}=2.4 \text{ rad/s}$$

so BC rotates counterclockwise, $\omega_{BC} = 0i + 0j + 2.4k \;\;\text{rad/s}$.

From here we can find the acceleration by finding two different expressions for the acceleration of B, one from A and one from C. Because of the diagram we take $\alpha_{AB}$ as clockwise, $0i + 0j - \alpha_{AB}k$ (if $\alpha_{AB}$ comes out negative, the assumed direction was wrong), and let $\alpha_{BC} = 0i + 0j + \alpha_{BC}k$.

From A ($a_A = 0$)

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\ 
= 0 + \begin{vmatrix}
i & j & k\\
0 & 0 & -\alpha_{AB} \\
0.04 & 0.04 & 0
\end{vmatrix} - 6^2(0.04i+0.04j+0k) \\
= (0.04\alpha_{AB}i - 0.04\alpha_{AB}j + 0k) + (-1.44i-1.44j+0k) \\
a_{B}= (0.04 \alpha_{AB}-1.44)i+(-0.04\alpha_{AB}-1.44)j+0k $$

From C ($a_C = 0$, $r_{B/C} = -0.1i + 0.07j + 0k \;\;\text{m}$)

$$ a_{B}=a_C+\alpha_{BC}\times r_{B/C}-\omega_{BC}^2 r_{B/C} \\ 
= 0 + \begin{vmatrix}
i & j & k\\
0 & 0 & \alpha_{BC} \\
-0.1 & 0.07 & 0
\end{vmatrix} - 2.4^2(-0.1i+0.07j+0k) \\
= (-0.07\alpha_{BC}i - 0.1\alpha_{BC}j + 0k) + (0.576i-0.403j+0k) \\
a_{B}= (-0.07\alpha_{BC}+0.576)i+(-0.1\alpha_{BC}-0.403)j+0k $$

Set components equal

$$ (i) \quad 0.04 \alpha_{AB}-1.44 = -0.07\alpha_{BC}+0.576 \rightarrow 0.04\alpha_{AB}+0.07\alpha_{BC}=2.016 \\
(j) \quad -0.04\alpha_{AB}-1.44 = -0.1\alpha_{BC}-0.403 \rightarrow -0.04\alpha_{AB}+0.1\alpha_{BC}=1.037 $$

Via simultaneous equations (adding them gives $0.17\alpha_{BC} = 3.053$)

$$ \alpha_{BC} = 17.96 \text{ rad/s}^2, \quad \alpha_{AB}=19.0 \text{ rad/s}^2 $$

$\alpha_{AB}$ is positive, so the assumed clockwise direction is correct

$$ \alpha_{AB} = 0i + 0j - 19.0k \quad \text{rad/s}^2 $$

i.e. 19.0 rad/s $^2$ clockwise.

## Question 7

The crank AB rotates about the fixed point A, and the piston C slides horizontally along the x axis. At the instant shown, the piston’s velocity and acceleration are $v_C = -14i + 0j + 0k \;\;\text{m/s}$ and $a_C = -2200i + 0j + 0k \;\;\text{m/s}^2$. What is the angular acceleration of the crank AB?

<img src = "figs\02_planar_kinematics_accel\Q7.jpg" width="50%"> <br>

### Answer

From the figure (converting mm to m)

$$ r_{B/A} = 0.05i + 0.05j + 0k \quad \text{m} \\
r_{C/B} = 0.175i - 0.05j + 0k \quad \text{m} $$

Similar to the last question, A is fixed, C can only move in i, and we need to solve for the angular velocities first. Let $\omega_{AB} = 0i + 0j + \omega_{AB}k$ and $\omega_{BC} = 0i + 0j + \omega_{BC}k$.

$$ v_B=v_A +\omega_{AB} \times r_{B/A} \\
= 0+\begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{AB} \\
0.05 & 0.05 & 0
\end{vmatrix} \\
= -0.05 \omega_{AB}i + 0.05 \omega_{AB}j + 0k $$

$$ v_B=v_C +\omega_{BC} \times r_{B/C} \\
= (-14i+0j+0k)+\begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{BC} \\
-0.175 & 0.05 & 0
\end{vmatrix} \\
= (-14 -0.05 \omega_{BC})i -0.175 \omega_{BC}j + 0k $$

Then analyse looking at each component of velocity

$$(i) \quad -0.05 \omega_{AB}+0.05 \omega_{BC} =-14 \\ (j) \quad 0.05 \omega_{AB}=-0.175 \omega_{BC} $$ 

And using simultaneous equations

$$ \omega_{AB}=217.78 \text{ rad/s, } \omega_{BC}=-62.22 \text{ rad/s} $$

This time I will solve it in a slightly different way, instead of finding two expressions for $a_B$, finding $a_B$ and using it as the reference point to find $a_C$. Both ways work so use whichever is most intuitive to you!

Carry unrounded values through this part. The answer comes from the difference of some large numbers, so rounding $\omega_{AB}$ to 218 rad/s before squaring it shifts the final answer by around 50 rad/s $^2$.

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\
= 0+\begin{vmatrix}
i & j & k\\
0 & 0 & \alpha_{AB} \\
0.05 & 0.05 & 0
\end{vmatrix}-217.78^2(0.05i+0.05j+0k) \\
= (-0.05\alpha_{AB}-2371.4)i+(0.05\alpha_{AB}-2371.4)j+0k $$

Then using this as the reference point to find C

$$ a_{C}=a_B+\alpha_{BC}\times r_{C/B}-\omega_{BC}^2 r_{C/B} \\
-2200i+0j+0k = a_B + \begin{vmatrix}
i & j & k\\
0 & 0 & \alpha_{BC} \\
0.175 & -0.05 & 0
\end{vmatrix} -(-62.22)^2(0.175i-0.05j+0k) \\ 
-2200i+0j+0k = a_B + (0.05\alpha_{BC}i+0.175\alpha_{BC}j+0k) + (-677.5i+193.6j+0k) $$

Substituting $a_B$ from above

$$ -2200i+0j+0k = (-0.05\alpha_{AB}-2371.4 + 0.05\alpha_{BC}-677.5)i \\
+(0.05\alpha_{AB}-2371.4+0.175\alpha_{BC}+193.6)j+0k $$

Equating components

$$ (i) \quad -2200=-0.05\alpha_{AB}+ 0.05\alpha_{BC}-3048.9 \rightarrow -0.05\alpha_{AB}+0.05\alpha_{BC}=848.9 \\
(j) \quad 0= 0.05\alpha_{AB}+0.175\alpha_{BC}-2177.8 \rightarrow 0.05\alpha_{AB}+0.175\alpha_{BC}=2177.8 $$

Solving (adding them gives $0.225\alpha_{BC} = 3026.7$) we find

$$ \alpha_{BC} = 13450 \text{ rad/s}^2, \quad \alpha_{AB}=-3530 \text{ rad/s}^2 \\
\alpha_{AB} = 0i + 0j - 3530k \quad \text{rad/s}^2 $$

Hence AB has an angular acceleration of 3530 rad/s $^2$ clockwise.

## Question 8

The robotic arm moves in the xy plane, and A is a fixed pivot. Arm AB has a constant clockwise angular velocity of 0.8 rad/s, arm BC has a constant counterclockwise angular velocity of 0.2 rad/s, and arm CD remains vertical. What is the acceleration of part D?

<img src = "figs\02_planar_kinematics_accel\Q8.jpg" width="50%"> <br>

### Answer

Because both AB and BC have constant angular velocity, $\alpha = 0$ for both. From the figure (converting mm to m)

$$ r_{B/A} = 0.3\cos(50)i + 0.3\sin(50)j + 0k = 0.1928i + 0.2298j + 0k \quad \text{m} \\
r_{C/B} = 0.3\cos(15)i - 0.3\sin(15)j + 0k = 0.2898i - 0.0776j + 0k \quad \text{m} $$

Note that C is below B, so the j component of $r_{C/B}$ is negative. The angular velocities are $\omega_{AB} = 0i + 0j - 0.8k \;\;\text{rad/s}$ and $\omega_{BC} = 0i + 0j + 0.2k \;\;\text{rad/s}$.

Acceleration of B can be expressed as (A is fixed)

$$ a_{B}=a_A+\alpha_{AB}\times r_{B/A}-\omega_{AB}^2 r_{B/A} \\ 
= 0 + 0 - 0.8^2(0.1928i+0.2298j+0k) \\
= -0.1234i-0.1471j+0k \quad \text{m/s}^2 $$

Acceleration of C can be expressed as

$$ a_{C}=a_B+\alpha_{BC}\times r_{C/B}-\omega_{BC}^2 r_{C/B} \\ 
= (-0.1234i-0.1471j+0k) + 0 - 0.2^2(0.2898i-0.0776j+0k) \\
= (-0.1234i-0.1471j+0k) + (-0.0116i+0.0031j+0k) \\
= -0.1350i-0.1440j+0k \quad \text{m/s}^2 $$

With $\alpha = 0$, $\omega$ only appears squared, so the direction of BC's rotation does not affect the answer.

Given CD remains vertical, it does not rotate ($\omega_{CD} = 0$, $\alpha_{CD} = 0$). It just translates, so every point on it has the same acceleration as C (and the 170 mm length is not needed)

$$ a_D = a_C = -0.135i-0.144j+0k \quad \text{m/s}^2$$

## Question 9

The disk of radius 300 mm rolls without slipping on the flat surface. Its centre A is moving toward the right and accelerating toward the right. The magnitude of the velocity of point C is 2 m/s, and the magnitude of the acceleration of point C is 14 m/s $^2$. Determine the angular acceleration of the disk.

<img src = "figs\02_planar_kinematics_accel\Q9.jpg" width="50%"> <br>

### Answer 

<img src = "figs\02_planar_kinematics_accel\Q9ans.jpg" width="50%"> <br>

As A moves to the right the disk rotates clockwise. Writing $\omega$ and $\alpha$ for the magnitudes, the disk's angular velocity is $0i + 0j - \omega k$ and its angular acceleration is $0i + 0j - \alpha k$. The position of C relative to A is $r_{C/A} = -0.3i + 0j + 0k \;\;\text{m}$.

First find the velocity and acceleration of the centre of the disk. Because it rolls without slipping, A only moves horizontally, with

$$ v_A = 0.3\omega i + 0j + 0k \\ a_A = 0.3\alpha i + 0j + 0k $$

Next find the velocity of C. It has a horizontal component from the motion of the centre and a vertical component from the rotation

$$ v_C = v_A + (0i+0j-\omega k)\times r_{C/A} \\
= (0.3\omega i+0j+0k) + \begin{vmatrix}
i & j & k\\
0 & 0 & -\omega \\
-0.3 & 0 & 0
\end{vmatrix} \\
= 0.3\omega i + 0.3\omega j + 0k $$

From here, we know the magnitude of velocity of C is 2 m/s so we can calculate the angular velocity

$$ 2 = \sqrt{(0.3\omega)^2+(0.3\omega)^2} \\ 4 = 0.18\omega^2 \\ \omega = 4.714 \text{ rad/s} $$

Then use a similar method to find the angular acceleration

$$ a_{C}=a_A+(0i+0j-\alpha k)\times r_{C/A}-\omega^2 r_{C/A} \\
a_{C}=(0.3\alpha i+0j+0k)+\begin{vmatrix}
i & j & k\\
0 & 0 & -\alpha \\
-0.3 & 0 & 0
\end{vmatrix}-4.714^2 (-0.3i+0j+0k) \\ 
a_C = (0.3\alpha i+0j+0k) + (0i+0.3\alpha j+0k) + (6.667i+0j+0k) \\
a_C = (0.3\alpha + 6.667)i + 0.3\alpha j + 0k $$

Now for the magnitude

$$ 14 = \sqrt{(0.3\alpha+6.667)^2+(0.3\alpha)^2} \\ 196 = 0.18\alpha^2 + 4\alpha + 44.44 \\ 0 = 0.18\alpha^2 + 4\alpha - 151.56 $$

The quadratic formula gives $\alpha$ = 19.96 or $\alpha$ = −42.18. $\alpha$ is the magnitude of a clockwise angular acceleration and A is accelerating to the right, so it must be positive. The angular acceleration of the disk is therefore

$$ 0i + 0j - 20.0k \quad \text{rad/s}^2 $$

i.e. 20.0 rad/s $^2$ clockwise.

## Question 10

The disk of radius 0.4 m rolls without slipping on the fixed circular surface of radius 1.2 m, with a constant clockwise angular velocity of 1 rad/s. What are the accelerations of points A and B?

<img src = "figs\02_planar_kinematics_accel\Q10.jpg" width="50%"> <br>

### Answer

Call the centre of the disk O. The disk's angular velocity is $\omega = 0i + 0j - 1k \;\;\text{rad/s}$, and since it is constant, $\alpha = 0$.

First find the velocity of O. The disk does not slip, so the contact point B is the instantaneous centre and $v_B = 0$. With $r_{O/B} = 0i + 0.4j + 0k \;\;\text{m}$

$$ v_O=v_B+\omega \times r_{O/B} \\
= 0 + \begin{vmatrix}
i & j & k\\
0 & 0 & -1 \\
0 & 0.4 & 0
\end{vmatrix} \\
v_O = 0.4i+0j+0k \quad \text{m/s} $$

O moves on a circular path of radius R = 1.2 + 0.4 = 1.6 m around the centre of the fixed surface. Its speed is constant, so it has no tangential acceleration, only the normal acceleration $v_O^2/R$ towards the centre of its path (the −j direction)

$$ a_O = -\frac{v_O^2}{R}j = -\frac{0.4^2}{1.6}j \\ a_O = 0i-0.1j+0k \quad \text{m/s}^2 $$

Be careful not to use $R\omega^2$ with the disk's $\omega$ = 1 rad/s here. That is how fast the disk spins, not how fast O goes round its 1.6 m path. The line from the centre of the fixed surface to O turns at $v_O/R$ = 0.25 rad/s, and 1.6 × 0.25 $^2$ = 0.1 m/s $^2$ gives the same answer.

Then A can be found with $r_{A/O} = 0i + 0.4j + 0k \;\;\text{m}$

$$ a_A = a_O+\alpha\times r_{A/O}-\omega^2 r_{A/O} \\  
a_A = (0i-0.1j+0k)+0-1^2(0i+0.4j+0k) \\ a_A=0i-0.5j+0k \quad \text{m/s}^2  $$

And B with $r_{B/O} = 0i - 0.4j + 0k \;\;\text{m}$

$$ a_B = a_O+\alpha\times r_{B/O}-\omega^2 r_{B/O} \\  
a_B = (0i-0.1j+0k)+0-1^2(0i-0.4j+0k) \\ a_B=0i+0.3j+0k \quad \text{m/s}^2  $$

Notice that B has zero velocity (it is the instantaneous centre) but its acceleration is not zero.

<br><br>



