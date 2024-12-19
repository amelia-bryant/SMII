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


# Tutorial Sheet 6: 3D Dynamics Answers

**Topics covered are:**
- Euler equations
- Constructing inertia matrices in 3D

**Tips**
- Surprise, the equations are getting longer! I'd always have the Euler equation pulled up for reference so you can easily see what you need to calculate.
- The inertia matrices can get confusing if you need to construct them yourself. Be clear with directions and do more practice.
- Make sure you are clear with matrix manipulation.

<br>

## Question 1 

A robotic manipulator moves a casting. The inertia matrix of the casting in terms of a body-fixed coordinate system with its origin at the center of mass is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.04
\end{bmatrix} \text{kgm}^2
$$

At the present instant, the angular velocity and angular acceleration of the casting are $\omega$=1.2i+0.8j−0.4k rad/s and $\alpha$=0.26i−0.07j+0.13k
rad/s $^2$. What moment is exerted about the center of mass of the casting by the manipulator?

<img src = "figs\06_3D_dynamics\Q1.jpg" width="50%"> <br>


### Answer

The Euler equation is

$$ \begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} 
\begin{bmatrix}
d\omega_x/dt \\
d\omega_y/dt\\
d\omega_z/dt
\end{bmatrix} 
+ \begin{bmatrix}
0 & -\Omega_z & \Omega_y\\
\Omega_z & 0 & -\Omega_x\\
-\Omega_y & \Omega_x & 0
\end{bmatrix}
\begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix}
\begin{bmatrix}
\omega_x \\
\omega_y\\
\omega_z
\end{bmatrix}
$$

We are given all information required, so just sub in! Remember $d\omega/dt$ is $\alpha$ 

$$ \begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.04
\end{bmatrix} 
\begin{bmatrix}
0.26 \\
-0.07\\
0.13
\end{bmatrix} 
+ \begin{bmatrix}
0 & 0.4 & 0.8\\
-0.4 & 0 & -1.2\\
-0.8 & 1.2 & 0
\end{bmatrix}
\begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.04
\end{bmatrix}
\begin{bmatrix}
1.2 \\
0.8\\
-0.4
\end{bmatrix} \\
= 0.0135i-0.0086j+0.01k \text{ Nm}
$$


## Question 2

A robotic manipulator holds a casting. The inertia matrix of the casting in terms of a body-fixed coordinate system with its origin at the center of mass is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.04
\end{bmatrix} \text{kgm}^2
$$

At the present instant, the casting is stationary. If the manipulator exerts a moment $\sum M$= 0.042i+0.036j+0.066k Nm about the center of mass, what is the angular acceleration of the casting at that instant?

<img src = "figs\06_3D_dynamics\Q1.jpg" width="50%"> <br>


### Answer

In the Euler equation, because the casting is stationary, the $\omega$ terms are zero, so we are left with the matrix version of $M=I\alpha$

$$

\begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} 
\begin{bmatrix}
d\omega_x/dt \\
d\omega_y/dt\\
d\omega_z/dt
\end{bmatrix} 
$$

Then sub in values

$$ \begin{bmatrix}
0.042 \\
0.036\\
0.066
\end{bmatrix} 
= \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.04
\end{bmatrix} 
\begin{bmatrix}
d\omega_x/dt \\
d\omega_y/dt\\
d\omega_z/dt
\end{bmatrix} \\
= 1.43i+0.987j+1.65k \text{ rad/s}^2
$$

## Question 3

The rigid body rotates about the fixed point O. Its inertia matrix in terms of the body-fixed coordinate system is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
4 & -2 & 0\\
-2 & 3 & 1\\
0 & 1 & 5
\end{bmatrix} \text{kgm}^2
$$

At the present instant, the rigid body’s angular velocity is $\omega$=6i+6j−4k rad/s and its angular acceleration is zero. What total moment about 𝑂 is being exerted on the rigid body?

<img src = "figs\06_3D_dynamics\Q3.jpg" width="50%"> <br>


### Answer

The angular acceleration is zero so the equation is simplified to 

$$ \begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
=  \begin{bmatrix}
0 & -\Omega_z & \Omega_y\\
\Omega_z & 0 & -\Omega_x\\
-\Omega_y & \Omega_x & 0
\end{bmatrix}
\begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix}
\begin{bmatrix}
\omega_x \\
\omega_y\\
\omega_z
\end{bmatrix}
$$

Then sub in values 

$$ \begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
0 & 4 & 6\\
-4 & 0 & -6\\
-6 & 6 & 0
\end{bmatrix}
\begin{bmatrix}
4 & -2 & 0\\
-2 & 3 & 1\\
0 & 1 & 5
\end{bmatrix}
\begin{bmatrix}
6 \\
6\\
-4
\end{bmatrix} \\
= -76i+36j-60k \text{ Nm}
$$

## Question 4

The rigid body rotates about the fixed point O. Its inertia matrix in terms of the body-fixed coordinate system is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
4 & -2 & 0\\
-2 & 3 & 1\\
0 & 1 & 5
\end{bmatrix} \text{kgm}^2
$$

At the present instant, the rigid body’s angular velocity is $\omega$=6i+6j−4k rad/s. The total moment about O due to the forces and couples acting on the rigid body is zero. What is its angular acceleration?

<img src = "figs\06_3D_dynamics\Q3.jpg" width="50%"> <br>

### Answer

We have to use the full Euler equation - sub in the values!

$$ \begin{bmatrix}
0\\
0\\
0
\end{bmatrix} 
= \begin{bmatrix}
4 & -2 & 0\\
-2 & 3 & 1\\
0 & 1 & 5
\end{bmatrix} 
\begin{bmatrix}
d\omega_x/dt \\
d\omega_y/dt\\
d\omega_z/dt
\end{bmatrix} 
+ \begin{bmatrix}
0 & 4 & 6\\
-4 & 0 & -6\\
-6 & 6 & 0
\end{bmatrix}
\begin{bmatrix}
4 & -2 & 0\\
-2 & 3 & 1\\
0 & 1 & 5
\end{bmatrix}
\begin{bmatrix}
6 \\
6\\
-4
\end{bmatrix} \\
\alpha = 16.2i-5.6j+13.1k \text{ rad/s}^2
$$ 

## Question 5

In terms of the coordinate system shown, the inertia matrix of the 6-kg slender bar is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
0.5 & 0.667 & 0\\
0.667 & 2.667 & 0\\
0 & 0 & 3.167
\end{bmatrix} \text{kgm}^2
$$

The bar is stationary relative to an inertial reference frame when the force F=12k (Newtons) is applied at the right end of the bar. No other forces or couples act on the bar. Determine

**(a)** The bar’s angular acceleration relative to the inertial reference frame. <br>
**(b)** The acceleration of the right end of the bar relative to the inertial reference frame at the instant the force is applied.

<img src = "figs\06_3D_dynamics\Q5.jpg" width="50%"> <br>

### Answer

**(a)** Taking the individual bar CoM distances from the reference frame labelled

<img src = "figs\06_3D_dynamics\Q5ans.jpg" width="50%"> <br>

The CoM can be found

$$
\frac{x_1m_1+x_2m_2}{m_1+m_2}, \frac{y_1m_1+y_2m_2}{m_1+m_2} \\
= \frac{(0)(\frac{1}{3}.6)+(1)(\frac{2}{3}.6)}{(\frac{1}{3}.6)+(\frac{2}{3}.6)}, \frac{(0.5)(\frac{1}{3}.6)+(0)(\frac{2}{3}.6)}{(\frac{1}{3}.6)+(\frac{2}{3}.6)} \\
= (0.667,0.167) \text{ m}
$$

Remembering the distance 'r' is taken from the right side where the force is applied, calculating moments

$$
M = C+r\times F = I\alpha \\
0+(1.33i-0.167j)\times12k=I\alpha \\
\begin{bmatrix}
i & j & k\\
1.33 & -0.167 & 0 \\
0 & 0 & 12
\end{bmatrix} 
=\begin{bmatrix}
0.5 & 0.667 & 0\\
0.667 & 2.667 & 0\\
0 & 0 & 3.167
\end{bmatrix} \alpha
\\
\begin{bmatrix}
-2 \\
-16 \\
0 \end{bmatrix} 
=\begin{bmatrix}
0.5 & 0.667 & 0\\
0.667 & 2.667 & 0\\
0 & 0 & 3.167
\end{bmatrix} 
\begin{bmatrix}
d\omega_x/dt \\
d\omega_y/dt\\
d\omega_z/dt
\end{bmatrix} \\
\alpha = 6.01i-7.5j \text{ rad/s}^2
$$

**(b)** We can work out the linear acceleration of the CoM with Newton's second law

$$
F = ma_O \\
12k = 6a_O \\
a_O =  2k \text{ m/s}^2
$$

Then use the acceleration equation to solve acceleration of the right end (denoted A) from the CoM

$$
a_A=a_O+\alpha \times r_{A/O}+\omega \times(\omega \times r_{A/O}) \\
a_A = 2k+\begin{vmatrix}
i & j & k\\
6.01 & -7.5 & 0\\
1.33 & -0.167 & 0
\end{vmatrix} +0 \\
a_A = 11k \text{ m/s}^2
$$

## Question 6

The dimensions of the 20 kg thin plate are h=0.4 m and b=0.6 m. The plate is stationary relative to an inertial reference frame when the force F=10 N is applied in the direction perpendicular to the plate. No other forces or couples act on the plate. At the instant F is applied, what is the magnitude of the acceleration of point A relative to the inertial reference frame?

<img src = "figs\06_3D_dynamics\Q6.jpg" width="50%"> <br>

### Answer

First we need to construct the inertia matrix. Referring to the formula sheet (thin rectangular plate) we construct

<img src = "figs\06_3D_dynamics\Q6ans.jpg" width="50%"> <br>

$$ \begin{bmatrix}
\frac{1}{12}mh^2 & 0 & 0\\
0 & \frac{1}{12}mh^2 & 0\\
0 & 0 & \frac{1}{12}m(b^2+h^2)
\end{bmatrix} = \begin{bmatrix}
0.267 & 0 & 0\\
0 & 0.6 & 0\\
0 & 0 & 0.867
\end{bmatrix} \text{kgm}^2
$$

The moment can be found with

$$
\sum M = C+r\times F \\
\sum M = 0 + \begin{vmatrix}
i & j & k\\
0.3 & -0.2 & 0\\
0 & 0 & -10
\end{vmatrix} \\
= 2i+3j
$$

We know that $\omega$ is zero so the Euler equation is simplified and we can find the angular acceleration  

$$
\begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} 
\begin{bmatrix}
d\omega_x/dt \\
d\omega_y/dt\\
d\omega_z/dt
\end{bmatrix} \\
\begin{bmatrix}
2 \\
3\\
0
\end{bmatrix} 
= \begin{bmatrix}
0.267 & 0 & 0\\
0 & 0.6 & 0\\
0 & 0 & 0.867
\end{bmatrix} 
\begin{bmatrix}
d\omega_x/dt \\
d\omega_y/dt\\
d\omega_z/dt
\end{bmatrix} \\
\alpha = 7.6i+5j \text{ m/s}^2
$$

Then to find the acceleration of the CoM we use Newton's second law

$$
F = ma_O \\
-10 = 20 a_O \\
a_O = -0.5k
$$

Then the acceleration of point A

$$
a_A=a_O+\alpha \times r_{A/O}+\omega \times(\omega \times r_{A/O}) \\
a_A = -0.5k+\begin{vmatrix}
i & j & k\\
7.6 & 5 & 0\\
-0.3 & 0.2 & 0
\end{vmatrix} +0 \\
a_A = 2.5k \text{ m/s}^2
$$

## Question 7

The thin circular disk of radius R=0.2 m and mass m=4 kg is rigidly attached to the vertical shaft. The plane of the disk is slanted at an angle  $\beta$=30◦ relative to the horizontal. The shaft rotates with constant angular velocity $\omega_O$=25 rad/s.

Determine the couple exerted on the disk by the shaft.

<img src = "figs\06_3D_dynamics\Q7.jpg" width="50%"> <br>

### Answer

Let's draw out a free body diagram the information in the question, considering its body-fixed reference frame

<img src = "figs\06_3D_dynamics\Q7ans.jpg" width="50%"> <br>

Construct the inertia matrix of the thin circular disk according to the body-fixed reference frame - note the reference frame is tiled by $\beta$ in order for construction using the formulae provided.

$$ \begin{bmatrix}
\frac{1}{4}mR^2 & 0 & 0\\
0 & \frac{1}{4}mR^2 & 0\\
0 & 0 & \frac{1}{2}mR^2
\end{bmatrix} = \begin{bmatrix}
0.04 & 0 & 0\\
0 & 0.04 & 0\\
0 & 0 & 0.08
\end{bmatrix} \text{kgm}^2
$$

The disk's angular velocity needs to be written in terms of the 'new' body-fixed reference frame (which has been tilted by $\beta$)

$$
\Omega = \omega_O\sin(\beta)j+\omega_O\cos(\beta)k \\
\Omega = 25\sin(30)j+25\cos(30)k \\
\Omega = 12.5j+21.65k
$$

The angular acceleration is zero (constant velocity) so the Euler equation simplifies to 

$$ \begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
0 & -\Omega_z & \Omega_y\\
\Omega_z & 0 & -\Omega_x\\
-\Omega_y & \Omega_x & 0
\end{bmatrix}
\begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix}
\begin{bmatrix}
\omega_x \\
\omega_y\\
\omega_z
\end{bmatrix}
$$

Then subbing in values

$$ \begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
0 & -21.65 & 12.5\\
21.65 & 0 & 0\\
-12.5 & 0 & 0
\end{bmatrix}
\begin{bmatrix}
0.04 & 0 & 0\\
0 & 0.04 & 0\\
0 & 0 & 0.08
\end{bmatrix}
\begin{bmatrix}
0 \\
12.5\\
21.65
\end{bmatrix} \\
M = 12.8i \text{ Nm}
$$

## Question 8

The vertical shaft rotates with constant angular velocity $\omega_O$. The 35◦ angle between the edge of the 44.5 N thin rectangular plate pinned to the shaft and the shaft remains constant. Determine $\omega_O$.

<img src = "figs\06_3D_dynamics\Q8.jpg" width="50%"> <br>

### Answer

Draw a free body diagram with the origin at the pinned joint and labelling angles and axes

<img src = "figs\06_3D_dynamics\Q8ans.jpg" width="50%">  <br>

We need to calculate a lot of things before we can sub into the Euler equation. First construct the inertia matrix 

$$ \begin{bmatrix}
\frac{1}{3}mh^2 & \frac{1}{3}mbh & 0\\
\frac{1}{3}mbh & \frac{1}{3}mb^2 & 0\\
0 & 0 & \frac{1}{3}m(b^2+h^2)
\end{bmatrix} = \begin{bmatrix}
0.14 & -0.21 & 0\\
-0.21 & 0.56 & 0\\
0 & 0 & 0.7
\end{bmatrix} \text{kgm}^2
$$

The weight force in terms of the reference frame is

$$
F = W(\cos(\beta)i-\sin(\beta)j) \\
F = 44.5(\cos(35)i-\sin(35)j) \\
F = 36.4i-25.5j \text{ N}
$$

The moment about the CoM is 

$$
\sum M = C+r\times F \\
\sum M = 0+\begin{vmatrix}
i & j & k\\
0.305 & 0.155 & 0\\
36.4 & -25.5 & 0
\end{vmatrix} \\
=-13.4k \text{ Nm}
$$

The plate rotates with angular velocity

$$
\omega = -\omega_O\cos(\beta)i+\omega_O\sin(\beta)j \\
\omega = -0.82\omega_Oi+0.57\omega_Oj
$$

As the shaft and plate are attached, 

$$
\omega = \Omega
$$

We can then use the Euler equation with $\omega_O$ factored out, taking into account angular acceleration is zero


$$ \begin{bmatrix}
\sum M_x \\
\sum M_y\\
\sum M_z
\end{bmatrix} 
= \begin{bmatrix}
0 & -\Omega_z & \Omega_y\\
\Omega_z & 0 & -\Omega_x\\
-\Omega_y & \Omega_x & 0
\end{bmatrix}
\begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix}
\begin{bmatrix}
\omega_x \\
\omega_y\\
\omega_z
\end{bmatrix} $$ 

$$
\begin{bmatrix}
0 \\
0\\
-13.4
\end{bmatrix} 
= \begin{bmatrix}
0 & 0 & 0.57\\
0 & 0 & 0.82\\
-0.57 & -0.82 & 0
\end{bmatrix}
\begin{bmatrix}
0.14 & -0.21 & 0\\
-0.21 & 0.56 & 0\\
0 & 0 & 0.7
\end{bmatrix}
\begin{bmatrix}
-0.82 \\
0.57 \\
0
\end{bmatrix} \omega_O^2\\
\begin{bmatrix}
0 \\
0\\
-13.4
\end{bmatrix} = 
\begin{bmatrix}
0 \\
0\\
-0.27
\end{bmatrix} \omega_O^2 $$

Then finally 

$$
-13.4 = -0.27  \omega_O^2\\
 \omega_O = 7.04 \text{ rad/s}
$$


<br><br>

