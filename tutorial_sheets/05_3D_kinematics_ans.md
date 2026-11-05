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


# Tutorial Sheet 5: 3D Kinematics Answers

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

The origin of the body-fixed axes is the centre of mass G, so $r_{A/G}$ is just the coordinates of A. The velocity of A relative to G is

$$ v_{A/G} = v_A-v_G=\omega \times r_{A/G} \\ = \begin{vmatrix}
i & j & k\\
0.62 & 0.45 & -0.23 \\
3.6 & 0.8 & -1.2
\end{vmatrix} \\ 
= -0.356i-0.084j-1.12k \text{ m/s}$$

## Question 2 

The angular velocity of the cube relative to the primary reference frame, expressed in terms of the body-fixed coordinate system shown, is $\omega$=−6.4i+8.2j+12k rad/s. The velocity of the centre of mass G of the cube relative to the primary reference frame at the instant shown is $v_G$=26i+14j+32k m/s. What is the velocity of point A of the cube relative to the primary reference frame at the instant shown?

<img src = "figs\05_3D_kinematics\Q2.jpg" width="50%"> <br>

### Answer

G is at the centre of the 2 m cube and A is the corner shared by the +x, +y and +z faces, so the position of A relative to G is

$$ r_{A/G} = i+j+k \text{ m}$$

Then 

$$ v_A=v_G+\omega \times r_{A/G} \\ v_A= 26i+14j+32k + \begin{vmatrix}
i & j & k\\
-6.4 & 8.2 & 12 \\
1 & 1 & 1
\end{vmatrix} \\ 
v_A = 22.2i+32.4j+17.4k \text{ m/s}$$

## Question 3

Using the cube in Q2, the coordinate system shown is fixed with respect to the cube. The angular velocity of the cube relative to the primary reference frame, $\omega$=−6.4i+8.2j+12k rad/s, is constant. The acceleration of the centre of mass G of the cube relative to the primary reference frame at the instant shown is $a_G$=136i+76j−48k m/s². What is the acceleration of point A of the cube relative to the primary reference frame at the instant shown?

### Answer

The angular velocity is constant, so $\alpha = 0$. The inner cross product $\omega \times r_{A/G}$ is the one from Q2, so the acceleration is

$$
a_A=a_G+\alpha \times r_{A/G}+ \omega \times(\omega\times r_{A/G}) \\
a_A=(136i+76j-48k) +0 + (-6.4i + 8.2j + 12k ) \times \begin{vmatrix}
i & j & k\\
-6.4 & 8.2 & 12 \\
1 & 1 & 1
\end{vmatrix} \\
a_A= 136i+76j-48k + \begin{vmatrix}
i & j & k\\
-6.4 & 8.2 & 12 \\
-3.8 & 18.4 & -14.6
\end{vmatrix} \\
a_A= 136i+76j-48k + (-340.5i-139.0j-86.6k) \\
a_A = -204.5i-63.0j-134.6k \text{ m/s}^2
$$

## Question 4

The origin of the secondary coordinate system shown is fixed to the centre of mass G of the cube. The velocity of the centre of mass G of the cube relative to the primary reference frame at the instant shown is $v_G$=26i+14j+32k m/s. The cube is rotating relative to the secondary coordinate system with angular velocity $\omega_{rel}$=4.8i+6j−2.4k rad/s. The secondary coordinate system is rotating relative to the primary reference frame with angular velocity $\Omega$=−1.6i+3j+5.2k rad/s. Both vectors are expressed in terms of the secondary coordinate system.

**(a)** What is the velocity of point A of the cube relative to the primary reference frame at the instant shown? <br>
**(b)** If the components of $\omega_{rel}$ and $\Omega$ in the secondary coordinate system are constant, what is the cube’s angular acceleration relative to the primary reference frame?

<img src = "figs\05_3D_kinematics\Q2.jpg" width="50%"> <br>

### Answer

There is a lot going on here, so annotate the figure

<img src = "figs\05_3D_kinematics\Q4ans.jpg" width="50%"> <br>

**(a)** The cube's angular velocity relative to the primary reference frame is

$$\omega = \Omega+\omega_{rel} \\
\omega = (-1.6i+3j+5.2k)+(4.8i+6j-2.4k) \\
\omega = 3.2i+9j+2.8k \text{ rad/s}$$

As in Q2, $r_{A/G} = i+j+k$ m, so

$$ v_A=v_G+\omega \times r_{A/G} \\ v_A= 26i+14j+32k + \begin{vmatrix}
i & j & k\\
3.2 & 9 & 2.8 \\
1 & 1 & 1
\end{vmatrix} \\ 
v_A = 32.2i+13.6j+26.2k \text{ m/s}$$

**(b)** The components of $\omega$ in the secondary coordinate system are constant, so its rate of change seen in that system, $(d\omega/dt)_{xyz}$, is zero. The secondary system turns at $\Omega$, so

$$ \alpha = \left(\frac{d\omega}{dt}\right)_{xyz}+\Omega\times \omega \\
\alpha = 0 + \Omega\times(\Omega+\omega_{rel}) = \Omega\times\omega_{rel} \quad (\text{as } \Omega\times\Omega = 0) \\
\alpha = \begin{vmatrix}
i & j & k\\
-1.6 & 3 & 5.2 \\
4.8 & 6 & -2.4
\end{vmatrix} \\
\alpha = -38.4i+21.1j-24.0k \text{ rad/s}^2$$

## Question 5

Relative to an earth-fixed reference frame, points A and B of the rigid parallelepiped are fixed and it rotates about the axis AB with an angular velocity of 30 rad/s, in the direction shown (anticlockwise when viewed from B looking towards A). Determine the velocities of points C and D relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q5.jpg" width="50%"> <br>

### Answer

The origin of xyz is the hidden lower corner at the back right, directly below where the y axis leaves the top face. Reading the figure, the coordinates (in m) are

$$ A = (0, 0, 0.4), \quad B = (0.4, 0.2, 0), \quad C = (0, 0.2, 0.4), \quad D = (0.4, 0.2, 0.4) $$

We only know the magnitude of $\omega$, so we need its direction. The rotation is anticlockwise when viewed from B looking towards A, so by the right-hand rule $\omega$ points from A towards B. Using the unit vector along AB,

$$
r_{B/A} = 0.4i + 0.2j - 0.4k \text{ m}, \quad |r_{B/A}| = \sqrt{0.4^2+0.2^2+0.4^2} = 0.6 \text{ m} \\
\omega = (30)\frac{0.4i + 0.2j - 0.4k}{0.6} = 20i+10j-20k \text{ rad/s}
$$

Then, with $r_{C/A} = 0.2j$ m and $r_{D/A} = 0.4i+0.2j$ m, solving for the velocities of C and D gives

$$ 
v_C = v_A+\omega\times r_{C/A} \\
v_C = 0 + \begin{vmatrix}
i & j & k\\
20 & 10 & -20 \\
0 & 0.2 & 0
\end{vmatrix} \\
v_C = 4i+4k \text{ m/s}
$$

$$ 
v_D = v_A+\omega\times r_{D/A} \\
v_D = 0 + \begin{vmatrix}
i & j & k\\
20 & 10 & -20 \\
0.4 & 0.2 & 0
\end{vmatrix} \\
v_D = 4i-8j \text{ m/s}
$$

As a check, $\omega \times r_{B/A} = 0$, so B is at rest, as it should be.

## Question 6

Using the parallelepiped in Q5, relative to the xyz coordinate system shown, points A and B of the rigid parallelepiped are fixed and the parallelepiped rotates about the axis AB with an angular velocity of 30 rad/s, in the direction shown. Relative to an earth-fixed reference frame, point A is fixed and the xyz coordinate system rotates with angular velocity $\Omega$=−5i+8j+6k rad/s. Determine the velocities of points C and D relative to the earth-fixed reference frame.

### Answer

Relative to the xyz coordinate system the parallelepiped turns about AB exactly as in Q5, so its angular velocity relative to xyz is

$$
\omega_{rel}= 20i+10j-20k \text{ rad/s}
$$

The xyz coordinate system itself turns at $\Omega$, so the parallelepiped's angular velocity relative to the earth is

$$
\omega = \Omega+\omega_{rel} \\
\omega = (-5i+8j+6k)+(20i+10j-20k) \\
\omega = 15i+18j-14k \text{ rad/s}
$$

A is fixed relative to the earth and is a point of the parallelepiped, so

$$ 
v_C = v_A+\omega\times r_{C/A} \\
v_C = 0 + \begin{vmatrix}
i & j & k\\
15 & 18 & -14 \\
0 & 0.2 & 0
\end{vmatrix} \\
v_C = 2.8i+3k \text{ m/s}
$$

$$ 
v_D = v_A+\omega\times r_{D/A} \\
v_D = 0 + \begin{vmatrix}
i & j & k\\
15 & 18 & -14 \\
0.4 & 0.2 & 0
\end{vmatrix} \\
v_D = 2.8i-5.6j-4.2k \text{ m/s}
$$


## Question 7

Relative to an earth-fixed reference frame, the vertical shaft rotates about its axis with angular velocity $\omega_O$=4 rad/s. The secondary xyz coordinate system is fixed with respect to the shaft, and its origin O, at the centre of the disc, is stationary. Relative to the secondary coordinate system, the disc (radius 8 cm) rotates with constant angular velocity $\omega_d$=6 rad/s. At the instant shown, determine the velocity of point A:

**(a)** relative to the secondary coordinate system;<br>
**(b)** relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q7.jpg" width="50%"> <br>

### Answer

<img src = "figs\05_3D_kinematics\Q7ans.jpg" width="50%"> <br>

The origin O, at the centre of the disc, is stationary and is a point of the disc, so measure positions from O. (Don't use the foot of the shaft: it is not a point of the disc, because the disc turns relative to the shaft.)

$$ r_{A/O} = 8\sin 45^\circ j+8\cos 45^\circ k \text{ cm} $$

**(a)** Relative to the secondary coordinate system the disc just spins about the x axis, with $\omega_{rel} = 6i$ rad/s, and O does not move, so

$$
v_{Arel}=\omega_{rel} \times r_{A/O} \\
v_{Arel}= \begin{vmatrix}
i & j & k\\
6 & 0 & 0 \\
0 & 8\sin 45^\circ & 8\cos 45^\circ 
\end{vmatrix} \\
v_{Arel} = -33.9j+33.9k \text{ cm/s}
$$

**(b)** The secondary coordinate system turns with the shaft, $\Omega = 4j$ rad/s, so

$$
\omega = \Omega+\omega_{rel} \\
\omega = 6i+4j \text{ rad/s} \\
v_A=v_O+\omega \times r_{A/O} \\ 
v_A=0+ \begin{vmatrix}
i & j & k\\
6 & 4 & 0 \\
0 & 8\sin 45^\circ & 8\cos 45^\circ 
\end{vmatrix} \\
v_A = 22.6i-33.9j+33.9k \text{ cm/s}
$$

## Question 8 
The object in figure (a) is supported by bearings at A and B in figure (b), which are fixed to the horizontal circular disc. The disc is supported by a vertical shaft that rotates with constant angular velocity $\omega_O$=6 rad/s. The horizontal bar rotates relative to the disc with constant angular velocity $\omega_b$=10 rad/s. The xyz coordinate system is fixed to the disc. At the instant shown:

**(a)** What is the velocity relative to an earth-fixed reference frame of the end C of the vertical bar? <br>
**(b)** What is the angular acceleration vector of the object relative to an earth-fixed reference frame? <br>
**(c)** What is the acceleration relative to an earth-fixed reference frame of the end C of the vertical bar?

<img src = "figs\05_3D_kinematics\Q8.jpg" width="50%"> <br>

### Answer

<img src = "figs\05_3D_kinematics\Q8ans.jpg" width="50%"> <br>

O, the middle of the horizontal bar, lies on both the shaft's axis and the bar's axis, so it is fixed: $v_O = 0$ and $a_O = 0$. From figure (a), $r_{C/O} = 0.1i+0.1j$ m. The xyz coordinate system is fixed to the disc, so its angular velocity is $\Omega = \omega_O j = 6j$ rad/s, and the bar's angular velocity relative to it is $\omega_{rel} = \omega_b i = 10i$ rad/s.

**(a)** 

$$ \omega = \Omega+\omega_{rel} \\
\omega = 6j+10i \text{ rad/s} $$

$$ v_C = v_O+\omega \times r_{C/O} \\
v_C = 0+\begin{vmatrix}
i & j & k\\
10 & 6 & 0 \\
0.1 & 0.1 & 0 
\end{vmatrix} \\
v_C = 0.4k \text{ m/s} $$

**(b)** Both rates are constant, so the components of $\omega$ in xyz are constant and $(d\omega/dt)_{xyz} = 0$:

$$ \alpha = \left(\frac{d\omega}{dt}\right)_{xyz} + \Omega\times\omega \\
\alpha =  0+\begin{vmatrix}
i & j & k\\
0 & 6 & 0 \\
10 & 6 & 0 
\end{vmatrix} \\
\alpha = -60k \text{ rad/s}^2 $$

**(c)** Because $v_O = 0$, the cross product $\omega \times r_{C/O}$ is just $v_C$ from part (a), so $\omega\times(\omega\times r_{C/O}) = \omega \times v_C$:

$$ a_C = a_O+\alpha\times r_{C/O}+\omega\times(\omega\times r_{C/O}) \\
a_C = 0+ \begin{vmatrix}
i & j & k\\
0 & 0 & -60 \\
0.1 & 0.1 & 0 
\end{vmatrix} + \begin{vmatrix}
i & j & k\\
10 & 6 & 0 \\
0 & 0 & 0.4 
\end{vmatrix} \\
a_C = (6i-6j)+(2.4i-4j) \\
a_C = 8.4i-10j \text{ m/s}^2
$$

## Question 9 

The point of the spinning top remains at a fixed point on the floor, which is the origin O of the secondary reference frame shown. The top’s angular velocity vector relative to the secondary reference frame, $\omega_{rel}$=50k rad/s, is constant. The angular velocity vector of the secondary reference frame relative to an earth-fixed primary reference frame is $\Omega$=2j+5.6k rad/s. The components of this vector are constant. (Notice that it is expressed in terms of the secondary reference frame.) Point A of the top has coordinates (0, 20, 30) mm.

**(a)** Determine the velocity of point A relative to the earth-fixed reference frame. <br>
**(b)** What is the top’s angular acceleration vector relative to the earth-fixed reference frame? <br>
**(c)** Determine the acceleration of point A relative to the earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q9.jpg" width="50%"> <br>

### Answer

O is fixed, so $v_O = 0$ and $a_O = 0$, and $r_{A/O} = 0.02j+0.03k$ m.

**(a)**

$$ \omega = \Omega + \omega_{rel} \\
\omega = (2j+5.6k)+50k \\
\omega = 2j+55.6k \text{ rad/s} $$

$$
v_A = v_O+\omega\times r_{A/O} \\
v_A = 0+\begin{vmatrix}
i & j & k\\
0 & 2 & 55.6 \\
0 & 0.02 & 0.03 
\end{vmatrix} \\
v_A = -1.052i \approx -1.05i \text{ m/s}
$$

**(b)** The components of $\omega$ in the secondary reference frame are constant, so $(d\omega/dt)_{xyz} = 0$:

$$ \alpha = \left(\frac{d\omega}{dt}\right)_{xyz} + \Omega\times\omega \\
\alpha =  0+\begin{vmatrix}
i & j & k\\
0 & 2 & 5.6 \\
0 & 2 & 55.6 
\end{vmatrix} \\
\alpha = 100i \text{ rad/s}^2 $$

**(c)** As in Q8, $v_O = 0$ means $\omega \times r_{A/O}$ is just $v_A$. Keep the unrounded $v_A = -1.052i$ m/s here: rounding it first gives $-61.4j$ instead of $-61.5j$.

$$ a_A = a_O+\alpha\times r_{A/O}+\omega\times(\omega\times r_{A/O}) \\
a_A = 0 + \begin{vmatrix}
i & j & k\\
100 & 0 & 0 \\
0 & 0.02 & 0.03 
\end{vmatrix} + \begin{vmatrix}
i & j & k\\
0 & 2 & 55.6 \\
-1.052 & 0 & 0 
\end{vmatrix} \\
a_A = (-3j+2k)+(-58.49j+2.104k) \\
a_A = -61.5j+4.10k \text{ m/s}^2 $$


## Question 10

The radius of the circular disc is R=0.2 m, and b=0.3 m. The disc rotates with angular velocity $\omega_d$=6 rad/s relative to the horizontal bar. The bar is pinned to the top of the vertical shaft and rotates relative to the shaft about the pin (the z axis) with angular velocity $\omega_b$=4 rad/s, and the vertical shaft rotates with angular velocity $\omega_O$=2 rad/s relative to an earth-fixed reference frame. Assume that the secondary reference frame shown is fixed with respect to the horizontal bar.

**(a)** What is the angular velocity vector $\omega_{rel}$ of the disc relative to the secondary reference frame? <br>
**(b)** At the instant shown, determine the velocity relative to the earth-fixed reference frame of point P, which is the uppermost point of the disc.

<img src = "figs\05_3D_kinematics\Q10.jpg" width="50%"> <br>


### Answer

There are a lot of moving parts, so I'm going to label it so the algebra symbols don't get mixed up. C is the hinge at the top of the shaft and M is the centre of the disc.

<img src = "figs\05_3D_kinematics\Q10ans.jpg" width="50%"> <br>

The secondary reference frame is fixed to the bar. The bar turns with the shaft about the y axis ($\omega_O$ = 2 rad/s) and, relative to the shaft, about the hinge pin, the z axis ($\omega_b$ = 4 rad/s). So the frame's angular velocity is

$$ \Omega = 2j+4k \text{ rad/s} $$

**(a)** Relative to the bar, the disc spins about the x axis, so this is simply

$$ \omega_{rel} =  6i \text{ rad/s}$$

**(b)** The angular velocity of the disc relative to the primary reference frame is

$$ \omega = \Omega+\omega_{rel} \\
\omega = 6i+2j+4k \text{ rad/s}$$

The hinge C is on the shaft's axis, so it is fixed, and it is a point of the bar. M is also a point of the bar, so the velocity of M is

$$ v_M = v_C+\Omega\times r_{M/C} \\
v_M = 0 + \begin{vmatrix}
i & j & k\\
0 & 2 & 4 \\
0.3 & 0 & 0 
\end{vmatrix} \\ 
v_M=1.2j-0.6k \text{ m/s}$$

(Don't use the foot of the shaft as the base point here: it is not a point of the bar, because the bar turns relative to the shaft about the hinge.)

M and P are both points of the disc, so the velocity of P is

$$
v_P = v_M+\omega\times r_{P/M} \\
v_P = 1.2j-0.6k + \begin{vmatrix}
i & j & k\\
6 & 2 & 4 \\
0 & 0.2 & 0 
\end{vmatrix} \\
v_P = -0.8i+1.2j+0.6k \text{ m/s}
$$

## Question 11

A small collar P slides up the vertical bar of the object in Q8, towards C, at a constant speed of 0.2 m/s relative to the bar. At the instant shown the collar is halfway up the vertical bar. The disc and the bar turn at the constant rates given in Q8. Determine:

**(a)** the velocity of the collar relative to an earth-fixed reference frame; <br>
**(b)** the acceleration of the collar relative to an earth-fixed reference frame.

<img src = "figs\05_3D_kinematics\Q8.jpg" width="50%"> <br>

### Answer

The collar moves over the object, so use a secondary reference frame fixed to the object, with its origin at O (fixed, as in Q8). This frame turns with the object, so from Q8 its angular velocity and angular acceleration are

$$ \Omega = 10i+6j \text{ rad/s}, \quad \alpha = -60k \text{ rad/s}^2 $$

Relative to this frame the collar moves up the bar in a straight line at constant speed, so

$$ r_{P/O} = 0.1i+0.05j \text{ m}, \quad v_{Prel} = 0.2j \text{ m/s}, \quad a_{Prel} = 0 $$

**(a)**

$$ v_P = v_O + v_{Prel} + \Omega\times r_{P/O} \\
v_P = 0 + 0.2j + \begin{vmatrix}
i & j & k\\
10 & 6 & 0 \\
0.1 & 0.05 & 0 
\end{vmatrix} \\
v_P = 0.2j-0.1k \text{ m/s} $$

**(b)** Now every term of the acceleration equation is needed, including the Coriolis term $2\Omega \times v_{Prel}$. We found $\Omega \times r_{P/O} = -0.1k$ in part (a):

$$ a_P = a_O + a_{Prel} + 2\Omega\times v_{Prel} + \alpha\times r_{P/O} + \Omega\times(\Omega\times r_{P/O}) \\
a_P = 0 + 0 + 2\begin{vmatrix}
i & j & k\\
10 & 6 & 0 \\
0 & 0.2 & 0 
\end{vmatrix} + \begin{vmatrix}
i & j & k\\
0 & 0 & -60 \\
0.1 & 0.05 & 0 
\end{vmatrix} + \begin{vmatrix}
i & j & k\\
10 & 6 & 0 \\
0 & 0 & -0.1 
\end{vmatrix} \\
a_P = 4k + (3i-6j) + (-0.6i+j) \\
a_P = 2.4i-5j+4k \text{ m/s}^2 $$


<br><br>

