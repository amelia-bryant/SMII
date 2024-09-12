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


# Tutorial Sheet 3: Moving Systems Answers

**Topics covered are**
- Body fixed and moving reference frames
- The concept of sliding contacts
- Cross product in 3D

**Tips**
- Really try to visualise these mechanisms, physically drawing on where each reference frame can help to prevent errors.
- You don't need to include all terms in your expressions if you know they are zero, however in the early questions I have included all terms for completeness.
- Remember unit vectors...

<br>

## Question 1

Sleeve C slides at 1 m/s relative to bar BD. Use the body-fixed coordinate system shown to determine the velocity of C.

<img src = "figs\03_moving_systems\Q1.jpg" width="50%"> <br>


### Answer

Find the velocity of B

$$ v_B = v_A+ \omega_{AB} \times r_{A/B} \\ = 0+\begin{vmatrix}
i & j & k\\
0 & 0 & 2 \\
0.6 & 0.6 & 0
\end{vmatrix} \\ 
= -1.2i+1.2j m/s $$

Then work out the velocity of C, taking into account relative acceleration of C from the new body fixed reference frame (shown in red)

<img src = "figs\03_moving_systems\Q1ans.jpg" width="50%"> <br>

$$ v_C = v_B + v_{Crel} + \omega_{BD} \times r_{C/B} \\ -1.2i+1.2j+1i+\begin{vmatrix}
i & j & k\\
0 & 0 & 4 \\
0.4 & + 0 & 0
\end{vmatrix} \\ 
= -0.2i+2.8j \text{ m/s}
$$

## Question 2

Using the same system as Question 1, the angular accelerations of the two bars are zero and the sleeve C slides at a constant velocity of 1 m/s relative to bar BD. What is the acceleration of C?

### Answer

$$
a_B=a_A+\alpha\times r_{B/A}-\omega^2_{AB}r_{B/A} \\
= 0+0-2^2(0.6i+0.6j) \\ = -2.4i-2.4j \text{ m/s}
$$

$$ a_c = a_B+a_{Crel}+2\omega_{BD}\times v_{Crel}+\alpha\times r_{C/B}-\omega^2_{BD} r_{C/B} \\ 
= -2.4i-2.4j+2\begin{vmatrix}
i & j & k\\
0 & 0 & 4 \\
1 & 0 & 0
\end{vmatrix} +0-4^2(0.4i) \\ 
= -8.8i+5.6j \text{ m/s}^2 $$

## Question 3

Bar AB has an angular velocity of 4 rad/s in the clockwise direction. What is the velocity of pin B relative to the slot?

<img src = "figs\03_moving_systems\Q3.jpg" width="50%"> <br>

### Answer

Begin finding the motion of B

$$ v_B = v_A + v_{Brel}+ \omega_{AB} \times r_{B/A} \\ = 0+0+\begin{vmatrix}
i & j & k\\
0 & 0 & -4 \\
0.115 & 0.06 & 0
\end{vmatrix} \\ 
= 0.24i-0.46j m/s $$

The slot is on the body CB, so to find B relative to the slot, find v relative to CB (a second expression for $v_B$) 

$$ v_B = v_C + v_{Brel} + \omega_{BC} \times r_{B/C} \\ = 0+v_{Brel}+\begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{BC} \\
0.035&  0.06 & 0
\end{vmatrix} \\ 
= v_{Brel}i-0.06\omega_{BC}i + 0.035\omega_{BC}j 
$$

Set expressions equal and do component analysis

$$0.24i-0.46j=v_{Brel}i-0.06\omega_{BC}i + 0.035\omega_{BC}j $$

$$(i)0.24=v_{Brel}-0.06\omega_{BC} \\ (j)-0.46 = 0.035\omega_{BC} \\
\omega_{BC} = -13.14 \text{ rad/s, } v_{Brel}=-0.548\text{ m/s}
$$

## Question 4

The coordinate system is fixed relative to the ship B. At the instant shown, the ship is sailing north at 5 m/s relative to the earth, and its angular velocity is 0.26 rad/s counterclockwise. Using radar, it is determined that the position of the aeroplane is 1080i+1220j+6300k m and its velocity relative to the ship’s coordinate system is 870i−45j−21k m/s. What is the aeroplane's velocity relative to the earth?

<img src = "figs\03_moving_systems\Q4.jpg" width="50%"> <br>

### Answer

This extends vectors into 3D so be careful!

$$ v_A = v_B+v_{Arel}+\omega\times r_{A/B} \\
= 5j+870i-45j-21k + \begin{vmatrix}
i & j & k\\
0 & 0 & 0.26 \\
1080 & 1220 & 6300
\end{vmatrix} \\ = 553i+24j-21k \text{ m/s}$$

## Question 5

The space shuttle is attempting to recover a satellite for repair. At the current time, the satellite’s position relative to a coordinate system fixed to the shuttle is 50i m. The gyroscopes on the shuttle indicate that its current angular velocity is 0.05j+0.03k rad/s. The shuttle pilot measures the velocity of the satellite relative to the body-fixed coordinate system and determines it to be −2i−1.5j+2.5k rad/s. What are the x, y, and z components of the satellite’s velocity relative to a nonrotating coordinate system with its origin fixed to the shuttle’s center of mass?

<img src = "figs\03_moving_systems\Q5.jpg" width="50%"> <br>

### Answer

Also bigger cross product!

$$ v_A = v_B+v_{Arel}+\omega\times r_{A/B} \\
v_A = 0-2i-1.5j+2.5k+ \begin{vmatrix}
i & j & k\\
0 & 0.05 & 0.03 \\
50 & 0 & 0
\end{vmatrix} \\ 
v_A = -2i \text{ m/s}$$

## Question 6

The train on the circular track is traveling at a constant speed of 50 m/s in the direction shown. The train on the straight track is traveling at 20 m/s in the direction shown and is increasing its speed at 2 m/s $^2$. Determine the velocity of passenger A that passenger B observes relative to the given coordinate system, which is fixed to the car in which B is riding.

<img src = "figs\03_moving_systems\Q6.jpg" width="50%"> <br>

### Answer

The angular velocity of B can be found

$$ \omega = \frac{v}{r} = \frac{50}{500} \\ = 0.1 \text{ m/s}$$

Then simply find the velocity using info provided in the question and diagram

$$ v_A = v_B+v_{Arel}+\omega\times r_{A/B} \\
-20j = 50j + v_{Arel} + \begin{vmatrix}
i & j & k\\
0 & 0 & 0.1 \\
500 & 0 & 0
\end{vmatrix} \\
v_{Arel} = -20j-50j-50j \\ 
v_{Arel} = -120j $$

## Question 7 
Suppose that the merry-go-round has counterclockwise angular velocity $\omega$ and counterclockwise angular acceleration $\alpha$. The person A is standing still on the ground. Determine A's acceleration relative to B's reference frame at the instant shown.

<img src = "figs\03_moving_systems\Q7.jpg" width="50%"> <br>

### Answer

Sketch the situation - it makes it much easier to comprehend!

<img src = "figs\03_moving_systems\Q7ans.jpg" width="50%"> <br>

Then the velocity analysis

$$ v_A = v_B+v_{Arel}+\omega\times r_{A/B} \\ 
0 = 0 + v_{Arel} + \begin{vmatrix}
i & j & k\\
0 & 0 & \omega \\
R & 0 & 0
\end{vmatrix} \\
v_{Arel} = -\omega R j $$

Then use this to work out acceleration

$$ a_A = a_B + a_{Arel} + 2\omega \times v_{Arel}+\alpha\times r_{A/B} -\omega^2r_{A/B} \\
0 = 0 +a_{Arel}+2\begin{vmatrix}
i & j & k\\
0 & 0 & \omega \\
0 & -\omega R & 0
\end{vmatrix}  + \begin{vmatrix}
i & j & k\\
0 & 0 & \alpha \\
R & 0 & 0
\end{vmatrix} - \omega^2(Ri) \\ 
0 = a_{Arel} + 2\omega^2Ri + \alpha Rj - \omega^2Ri \\ 
a_{Arel} = - \omega^2Ri - \alpha Rj $$

## Question 8 

The angular velocity $\omega$ AC=5° per second. Determine the angular velocity of the hydraulic actuator BC and the rate at which the actuator is extending. 

<img src = "figs\03_moving_systems\Q8.jpg" width="50%"> <br>

### Answer

First convert degrees/s to rad/s

$$ 5\frac{\pi}{180} = 0.087 rad/s $$

The velocity of C taken from A is

$$ v_C = \omega_{AC}\times r_{C/A} \\ 
= 0 + \begin{vmatrix}
i & j & k\\
0 & 0 & 0.087 \\
2.6 & 2.4 & 0
\end{vmatrix} \\
= 0.21i + 0.2269j $$

Only a certain component ('amount') of the velocity of C will be due to the actuator BC extending. To find the proportion of movement caused by the actuator movement itself, we can use unit vectors. Unit vector BC (call it e) is

$$ e = \frac{1.2i+2.4j}{\sqrt{1.2^2+2.4^2}} = 0.45i+0.89j $$

Velocity fo C in terms of the actuator is then 

$$ v_C = v_B + v_{Crel}e + \omega_{BC}\times r_{C/B} \\
-0.21i+0.227j = 0+v_{Crel}(0.45i+0.89j)+\begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{BC} \\
1.2 & 2.4 & 0
\end{vmatrix} \\
-0.21i+0.227j  = (0.45v_{Crel}-2.4\omega_{BC})i + (0.86v_{Crel}+1.2\omega_{BC})i $$

Equate components and solve as simultaneous equations

$$ (i) -0.21 = 0.45v_{Crel}-2.4\omega_{BC} \\
(j) 0.227 = 0.86v_{Crel}+1.2\omega_{BC} \\
\omega_{BC} = 0.108 \text{ rad/s, and the velocity of the actuator, } v_{Crel} = 0.109 \text{ m/s} $$

## Question 9

The sleeve at A slides upward at a constant velocity of 10 m/s. Bar AC slides through the sleeve at B. Determine the angular velocity of bar AC and the velocity at which the bar slides relative to the sleeve at B. 

<img src = "figs\03_moving_systems\Q9.jpg" width="50%"> <br>

### Answer

In this question you have two sleeves, so remember that the coordinate system is the sleeve of B which  rotates with the bar but doesn't translate.

The unit vector between B and A is

$$ e = \frac{\cos(30)i+\sin(30)j}{\sqrt{cos(30)^2+\sin(30)^2}} = 0.866i+0.5j $$

Then velocity analysis

$$ v_A = v_B+v_{Arel}e+\omega_{AC}\times r_{A/B} \\ 
10j = 0 + v_{Arel}(0.866i+0.5j) + \begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{AC} \\
0.866 & 0.5 & 0
\end{vmatrix} \\
10j = (-0.5\omega_{AC} +0.866 v_{Arel})i+ (0.866\omega_{AC} + 0.5 v_{Arel}) $$

Equate components and solve as simultaneous equations

$$ (i) 0 = -0.5\omega_{AC} +0.866 v_{Arel} \\
(j) 10 = 0.866\omega_{AC} + 0.5 v_{Arel} \\
\omega_{AC} = 8.66 \text{ rad/s, and velocity of B towards A, } v_{Arel} = 5 \text{ m/s} $$

## Question 10

The satellite A is in a circular polar orbit (that intersects the earth’s axis of rotation). The radius of the orbit is $R$, and the magnitude of the satellite’s velocity relative to a non-rotating reference frame with its origin at the center of the earth is $v_A$. At the instant shown, the satellite is above the equator. An observer B on the earth directly below the satellite measures its motion using the earth-fixed coordinate system shown. What are the velocity and acceleration of the satellite relative to B’s earth-fixed coordinate system? The radius of the earth is $R_E$ and the angular velocity of the earth is $\omega_E$.

<img src = "figs\03_moving_systems\Q10.jpg" width="50%"> <br>

### Answer

The location of A in the coordinate system is 

$$ r_A = (R-R_E)i$$

and the velocity of the observer (B) is

$$ v_B =  \begin{vmatrix}
i & j & k\\
0 & \omega_E & 0 \\
R_E & 0 & 0
\end{vmatrix} = -\omega_E R_Ek$$

The velocity of A relative to B can then be found

$$ v_A = v_B+v_{Arel}+\omega_{AC}\times r_{A/B} \\
v_Aj = -\omega_E R_Ek + v_{Arel} + \begin{vmatrix}
i & j & k\\
0 & \omega_E & 0 \\
R-R_E & 0 & 0
\end{vmatrix} \\
v_Aj = -\omega_E R_Ek+v_{Arel}-\omega_E Rk+\omega_E R_Ek \\
v_{Arel} = v_Aj+\omega_E Rk
$$

Then onto acceleration. The acceleration of a is

$$ a_A = \frac{v^2}{r} =-\frac{v_A^2}{R}i$$

and B 

$$ a_B = r\omega^2 = -\omega_E^2R_Ei $$

Using the base equation (full version!)

$$ a_A = a_B + a_{Arel} + 2\omega \times v_{Arel}+\alpha\times r_{A/B} +\omega \times(\omega\times r_{A/B}) \\
-\frac{v_A^2}{R}i = -\omega_E^2R_Ei+ a_{Arel} + 2 \begin{vmatrix}
i & j & k \\
0 & \omega_E & 0 \\
0 & v_A & \omega_ER 
\end{vmatrix} + 0 + \omega_E \times \begin{vmatrix}
i & j & k \\
0 & \omega_E & 0 \\
R-R_E & 0 & 0 
\end{vmatrix}\\
-\frac{v_A^2}{R}i = - \omega_E^2R_Ei + a_{Arel} + 2\omega_E^2Ri + \begin{vmatrix}
i & j & k\\
0 & \omega_E & 0 \\
0 & 0 & -\omega_E(R-R_E) 
\end{vmatrix}\\
-\frac{v_A^2}{R}i =- \omega_E^2R_Ei + a_{Arel} + 2\omega_E^2Ri -\omega_E^2Ri+ \omega_E^2R_Ei \\
a_{Arel} =-(\frac{v_A^2}{R}+\omega_E^2R)i $$

<br><br>


