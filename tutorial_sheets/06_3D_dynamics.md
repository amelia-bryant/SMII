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


# Tutorial Sheet 6: 3D Dynamics

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

At the present instant, the angular velocity and angular acceleration of the casting are $\omega$=1.2i+0.8j−0.4k rad/s and $\alpha$=0.26i−0.07j+0.13k rad/s $^2$. What moment is exerted about the center of mass of the casting by the manipulator?

<img src = "figs\06_3D_dynamics\Q1.jpg" width="50%"> <br>

### Answer

$$ 0.0135i+0.0086j+0.01k \text{ Nm} $$

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

At the present instant, the casting is stationary. If the manipulator exerts a moment $\sum M$= 0.042i+0.036j+0.066k Nm about the center of mass, what is the
angular acceleration of the casting at that instant?

<img src = "figs\06_3D_dynamics\Q1.jpg" width="50%"> <br>

### Answer

$$ 1.43i+0.987j+1.65k \text{ rad/s}^2 $$


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

At the present instant, the rigid body’s angular velocity is $\omega$=6i+6j−4k rad/s and its angular acceleration is zero. What total moment about O is being exerted on the rigid body?

<img src = "figs\06_3D_dynamics\Q3.jpg" width="50%"> <br>

### Answer

$$ -76i+36j-60k \text{ Nm} $$


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

$$ 16.2i-5.6j+13.1k \text{ rad/s}^2 $$ 

## Question 5

In terms of the coordinate system shown, the inertia matrix of the 6 kg slender bar is

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

**(a)** 

$$ 6.01i-7.5j \text{ rad/s}^2 $$

**(b)**

$$ 11k \text{ m/s}^2 $$


## Question 6

The dimensions of the 20 kg thin plate are h=0.4 m and b=0.6 m. The plate is stationary relative to an inertial reference frame when the force F=10 N is applied in the direction perpendicular to the plate. No other forces or couples act on the plate. At the instant F is applied, what is the magnitude of the acceleration of point A relative to the inertial reference frame?

<img src = "figs\06_3D_dynamics\Q6.jpg" width="50%"> <br>

### Answer

$$ 2.5k \text{ m/s}^2 $$


## Question 7

The thin circular disk of radius R=0.2 m and mass m=4 kg is rigidly attached to the vertical shaft. The plane of the disk is slanted at an angle  $\beta$=30◦ relative to the horizontal. The shaft rotates with constant angular velocity $\omega_O$=25 rad/s.

Determine the couple exerted on the disk by the shaft.

<img src = "figs\06_3D_dynamics\Q7.jpg" width="50%"> <br>

### Answer

$$ 12.8i \text{ Nm} $$

## Question 8

The vertical shaft rotates with constant angular velocity $\omega_O$. The 35◦ angle between the edge of the 44.5 N thin rectangular plate pinned to the shaft and the shaft remains constant. Determine $\omega_O$.

<img src = "figs\06_3D_dynamics\Q8.jpg" width="50%"> <br>

### Answer

$$ 7.04 \text{ rad/s}
$$

<br><br>

