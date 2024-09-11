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


# Tutorial Sheet 1: Planar Kinematics Answers

**Topics covered are:**
- Types of motion
- Rotation around a fixed axis
- Relative velocity
- Instantaneous centres

**Tips**
- Always draw the situation! 
- The order of the cross product matters, $\omega\times r \neq r\times\omega$

<br>

## Question 1 

At the instant shown, the disk has angular velocity is 2 rad/s counter clockwise and angular acceleration 6 rad/s $^2$. Its radius is 0.2 m. 

What are the magnitudes of the velocity and acceleration of point A?

<img src = "figs\01_planar_kinematics\Q1.png" width="50%"> <br>


### Answer

It is useful to sketch the situation.

<img src = "figs\01_planar_kinematics\Q1_ans.png" width="50%"> <br>

Using the basic equations of motion and subbing in values, velocity can be calculated. 

$$ v=r \omega=0.2\times2 \\=0.4 m/s $$

The magnitude of acceleration can be calculated using the normal and tangential components, then using basic pythagoras to find the magnitude.

$$ a_n=r\omega^2 = 0.2\times 2^2 \\ = 0.8 m/s^2 $$ 

$$ a_t=r\alpha = 0.2\times6 \\=1.2 m/s^2 $$

$$ |a|= \sqrt{a_n^2+a_t^2} \\ = \sqrt{0.8^2+1.2^2} \\\ =1.44m/s^2 $$
<br>

## Question 2

The mass A starts from rest at t=0 and falls with a constant acceleration of 8 m/s $^2$. When the mass has fallen one meter, determine the magnitudes of: <br>
**(a)** The angular velocity of the pulley <br>
**(b)** The tangential and normal components of acceleration of a point at the outer edge of the pulley.

<img src = "figs\01_planar_kinematics\Q2.jpg" width="50%"> <br>

### Answer

**(a)** a=8, u=0 (starting from rest), s=1, calculate v in order to work out everything else. Using SUVAT
$$ v^2=a^2 +2as \\ v=\sqrt{0^2+2\times 8\times1}\\=4m/s$$
Use this with the given equations. 
$$ v=r\omega \\ 4=0.1 \times \omega \\ \omega = 40 rad/s$$
**(b)** 
Using the given equations and v from before
$$ a_n =\frac{v^2}{r} = \frac{4^2}{0.1} \\= 160 m/s^2 $$
We need alpha to find tangential accel. 
$$ \alpha = \frac{a}{r} = \frac{8}{0.1} = 80 rad/s^2$$
$$ a_t = r\alpha = 0.1\times 80 \\= 8m/s^2$$

## Question 3

**(a)**  If the bicycle’s 120 mm radius sprocket  wheel rotates through one revolution, through how many revolutions does the 45 mm gear turn? 

**(b)** If the angular velocity of the sprocket wheel is 1 rad/s, what is the
 angular velocity of the gear?

<img src = "figs\01_planar_kinematics\Q3.jpg" width="50%"> <br>

 ### Answer

 Sketch the situation so it's a bit more comprehensible. 

 <img src = "figs\01_planar_kinematics\Q3_ans.jpg" width="50%"> <br>

 **(a)** As the gears are attached by the chain, when the large sprocket wheel rotates by a certain length, the small one must also pass that length through. Hence we can simply use ratios. 

 Circumference of wheel 

 $$ l = \pi d = \pi \times 0.12\times 2 \\  = 0.754 \text{ m}$$

 'Length' passed through by gear. 
 $$0.754 = x \times \pi \times 2 \times 0.045 \\ x=2.67 \text{ revs} $$ 

 **(b)** The chain must be moving at a constant rate (velocity), therefore
 $$ v_s = v_g \\ r_s\omega_s = r_g\omega_g \\ 0.12\times 1 = 0.045\times \omega_g \\ \omega_g = 2.67 rad/s $$ 


 ## Question 4

The disk is rotating about the origin with a constant clockwise angular velocity of 100 rpm. Determine the 𝑥 and 𝑦 components of velocity of points 𝐴 and 𝐵 (in cm/s).

 <img src = "figs\01_planar_kinematics\Q4.jpg" width="50%"> <br>

 ## Answer

 First, convert rpm to rad/s, or all the calculations will be messed up. You can do this manually - or just plug it into your calculator! 

$$ \frac{100}{60}.2\pi = 10.47 rad/s = \omega $$

Then using the basic $v=\omega r$ equation

**Point A**
$$ v_x=10.47\times 8=83.77 $$
$$ v_y=10.47\times 8=83.77 $$
In vector form
$ v_A=83.77i+83.77j $ cm/s

**Point B**
$$ v_x=10.47\times 16=167.5 $$
$$ v_y=10.47\times 0=0 $$
In vector form $ v_B=167.55j $ cm/s

## Question 5

The bar is moving in the x–y plane and is rotating in the counterclockwise direction. The magnitude of the velocity of point A relative to point B is 8 m/s. Relative to a nonrotating referenece frame with origin A, what is the 

**(a)** Angular velocity of the bar 

**(b)**  Velocity of B relative to the reference frame in vector form.


<img src = "figs\01_planar_kinematics\Q5.jpg" width="50%"> <br>

### Answer

**(a)**  $$ \omega = \frac{v}{r} = \frac{8}{2} \\ = 4 rad/s $$
**(b)**  
As we are dealing with vectors, we need to use the cross product. This is really important from now on so make sure you are comfortable with calculating this. I recommend the method below, but whatever works for you!

<img src = "figs\01_planar_kinematics\Q5ans.jpg" width="50%"> <br>

To calculate velocity of B

$$ v_B = \omega\times r \\ = 4k \times 2(cos(30)i+sin(30)j) = \begin{vmatrix}
i & j & k\\
0 & 0 & 4 \\
2cos(30) & 2sin(30) & 0
\end{vmatrix} $$

Using my cross product method

$$ 0\times0i-4\times2sin(30)i+4\times2cos(30)j-0\times0j+0\times2sin(30)i-0\times2cos(30k) \\

= -4i + 6.93j$$ 

## Question 6

The bar is rotating in the counterclockwise direction with angular velocity ω. The magnitude of the velocity of point A relative to point B is 6 m/s. Determine the velocity of point B (relative to the origin).

<img src = "figs\01_planar_kinematics\Q6.jpg" width="50%"> <br>

### Answer

The distance B from A can be simply found
$$ r_{A/B}=\sqrt{(0.4+0.4)^2+(0.4+0.2)^2} $$

The angular velocity of the bar is constant through the whole bar. 

$$ v_{A/B}=\omega. r_{A/B} \\ \omega= \frac{6}{1}=6 rad/s$$ 

From there, velocity of B can be calculated as normal

$$ v_B=\omega \times r_B = 6k \times (0.4i-0.2j) \\ v_B = 1.2i+2.4j \text{ m/s}$$

Remember to use the cross product!

## Question 7

The helicopter is in planar motion in  the x–y plane. At the instant shown, the position of its center of mass, G, is x=2m, y=2.5m, and its velocity is $v_G=12i+4j$ (m/s). The position of point T, where the tail rotor is mounted, is x= −3.5m, y=4.5m. The helicopter’s angular velocity is 0.2 rad/s clockwise. What is the velocity of point T?

<img src = "figs\01_planar_kinematics\Q7.jpg" width="50%"> <br>

## Answer

Draw the situation. 

<img src = "figs\01_planar_kinematics\Q7a.jpg" width="50%"> <br>

We currently only know the velocity of G. To find the velocity of T, we need to find the velocity of T from G, and add the velocity of G. See it as velocity 'origin to G + G to T'.

$$ r_{T/G}= (-3.5-2)i+(4.5-2.5)j=-5.5i+2j \text{ m} $$

$$ v_T=v_G +\omega \times r_{T/G} \\ = 12i+4j + 
\begin{vmatrix}
i & j & k\\
0 & 0 & -0.2 \\
-5.5 & 2 & 0
\end{vmatrix} \\
=12.4i+5.1j \text{ m/s}  $$

## Question 8

At the instant shown, the piston’s velocity is $v_C = −14i$ m/s. What is the angular velocity of the crank AB, which rotates around A?

<img src = "figs\01_planar_kinematics\Q8.jpg" width="50%"> <br>


### Answer

Looking at the mechanism, we can see that C is limited to only i. Also knowing that A is static, we can set up some equations.  

$$ v_B=v_A +\omega_{BA} \times r_{BA} \\ 0+\omega_{BA}k \times (0.05i+0.05j) \\ = -0.05 \omega_{BA}i + 0.05 \omega_{BA}j$$

$$v_B=v_C +\omega_{BC} \times r_{BC} \\ -14i+\omega_{BC}k \times (0.175i-0.05j) \\ = -14i -0.05 \omega_{BC}i -0.175 \omega_{BC}j$$

Then analyse looking at each component of velocity

$$(i) -0.05 \omega_{BA}+0.05 \omega_{BC} =-14 \\ (j) 0.05 \omega_{BA}=-0.175 \omega_{BC} $$ 

And using simultaneous equations

$$ \omega_{BA}=218 \text{ rad/s} $$

## Question 9

Points A and B of the 2-m bar slide on the plane surfaces. Point B is moving to the right at 3 m/s. What is the velocity of the midpoint G of the bar?

<img src = "figs\01_planar_kinematics\Q9.jpg" width="50%"> <br>

## Answer

Take advantage of the constraints from the floor and wall to solve this; the velocity of A has only j component, the velocity of B has only i.

$$ v_A = v_B +\omega \times r_{A/B} \\ v_Aj=3i+  \begin{vmatrix}
i & j & k\\
0 & 0 & \omega \\
-2\cos(70) & 2\sin(70) & 0
\end{vmatrix}  \\ v_A=-1.88\omega i -0.7\omega j +3 i$$

Now equate i and j components

$$ (i) 0=-1.88\omega +3 \rightarrow \omega=1.6 \\ (j) v_A=-0.7\omega$$

Now work out the velocity of G. You can do this from point B or point A (using the above relation) but given point B's velocity is given in the question, I'd advise you to go from point B just in case you make an exam. 

$$ v_G = v_B +\omega \times r_{G/B}  \\ v_G=3i+  \begin{vmatrix}
i & j & k\\
0 & 0 & 1.6 \\
-\cos(70) & \sin(70) & 0
\end{vmatrix} \\ = 1.5i- 0.547j \text{ m/s}$$

## Question 10

Bar AB rotates in the counterclockwise direction at 6 rad/s. Determine the angular velocity of bar BD and the velocity of point D.

<img src = "figs\01_planar_kinematics\Q10.jpg" width="50%"> <br>


### Answer

Looking at the mechanism we can determine some key constraints that will help us solve this. A is a fixed centre of rotation so has zero velocity. C has only an i component.

First calculate $v_B$ from point A

$$ v_B=v_A + \omega_{AB}\times r_{B/A} \\ =0 + 6k \times 0.32i \\ = 1.92j$$

We can then need to calculate $\omega_{BD}$ (which is the same as $\omega_{BC}$). We can do this using the calculated $v_B$ and the constraints we know about C. 

$$ v_C=v_B + \omega_{BC}\times r_{C/B} \\ = 0.48\omega_{BC} i+0.24 \omega_{BC} j+1.92j $$

Now analyse components

$$(i) v_C=0.48\omega_{BC} \\ (j) 0=1.92+0.24 \omega_{BC} $$

Solving $$ \omega_{BC}=-8k \\ v_C = 3.84i $$

Now to calculate velocity of D 

$$ v_D=v_B + \omega_{BD}\times r_{D/B} \\ = 1.92j + \begin{vmatrix}
i & j & k\\
0 & 0 & -8 \\
0.4 & 0.8 & 0
\end{vmatrix} \\ v_D=6.4i-1.28j$$

## Question 11

The horizontal member ADE supporting the scoop is stationary. If the link BD is rotating in the clockwise direction at 1 rad/s,what is the angular velocity of the scoop?

<img src = "figs\01_planar_kinematics\Q11.jpg" width="50%"> <br>

### Answer

This question relies on calculating a lot of velocities relative to each other, so be careful with carrying over errors!

$$ v_B=v_D+\omega_{BD} \times r_{B/D} \\ = 0 + \begin{vmatrix}
i & j & k\\
0 & 0 & -1 \\
0.31 & 0.61 & 0
\end{vmatrix} = 0.61i-0.31j $$

Then if we write multiple expressions for $v_C$ we can make simultaneous equations to solve the question.

$$ v_C = v_B + \omega_{BC} \times r_{C/B} \\ 0.61i-0.31j + 
\begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{BC} \\
0.76 & -0.15 & 0
\end{vmatrix} \\ = 0.61i-0.31j +0.15\omega_{BC}i+0.76\omega_{BC}j $$

$$ v_C = v_E + \omega_{CE} \times r_{C/E} \\ 0 + 
\begin{vmatrix}
i & j & k\\
0 & 0 & \omega_{CE} \\
0 & 0.46 & 0
\end{vmatrix} \\ = -0.46\omega_{CE}i $$

Equating $v_C$ expressions in terms of i and j components

$$ (i) -0.46\omega_{CE} = 0.61+0.15\omega_{BC} \\(j) 0 = 0.31+0.76\omega_{BC} $$

Hence

$$ \omega_{BC}=0.4 \text{ rad/s} \\\omega_{CE}=-1.47 \text{ rad/s} $$

Where CE is the scoop!

## Question 12

The velocity of point O of the bat is $v_O$ =−1.83i− 4.27j m/s, and the bat rotates about the z axis with a counterclockwise angular velocity of 4 rad/s. What are the x and y coordinates of the bat’s instantaneous center?

<img src = "figs\01_planar_kinematics\Q12.jpg" width="50%"> <br>

### Answer

Arbitrarily place the instentaneous center. It doesnt really matter where - as long as you have signs right the maths will correct itself. 

<img src = "figs\01_planar_kinematics\Q12ans.jpg" width="50%"> <br>

Say the coordinates of the instantaneous center is $(x_I, y_I)$, you then work it all out as O from I (as I has zero velocity). 

$$ v_O=−1.83i− 4.27j=\omega\times r_{O/I} = \begin{vmatrix}
i & j & k\\
0 & 0 & 4 \\
-x_I & -y_I & 0
\end{vmatrix} = 4y_I i-4x_I j $$

Equate terms to find the coordinates. 

$$ (i) -1.83 = 4y_C \rightarrow y_C=-0.46 \\  (j) -4.27 = -4x_C \rightarrow x_C=1.07 \\ (1.07,-0.46) \text{ m}$$

## Question 13
Points A and B of the 1m bar slide on the plane surfaces. The velocity of B is $v_B$ = 2i (m/s).

**(a)** What are the coordinates of the instantaneous center of the bar?

**(b)** Use the instantaneous center to determine the velocity at A.

<img src = "figs\01_planar_kinematics\Q9.jpg" width="50%"> <br>

### Answer

Just as in Q9, the bar is constrained A in j, B in i. 

**(a)** Work this out using geometry. Draw perpendiculars to the velocity vectors. at A and B. 

<img src = "figs\01_planar_kinematics\Q13ans.jpg" width="50%"> <br>

$$ (\sin(20), \cos(20))  \\ = (0.34, 0.94) $$

**(b)** Find the angular velocity of the bar

 $$ v_B=2i = v_I+\omega \times r_{O/I} \\ 2 = 0.94\omega \rightarrow \omega=2.13 \text{ rad/s} $$

 Then the velocity of A from the instantaneous center

$$ v_A = v_I+\omega \times r_{A/I} \\ = 0+2.13k\times -0.34i \\ = -0.23j \text{ m/s} $$

<br><br>

