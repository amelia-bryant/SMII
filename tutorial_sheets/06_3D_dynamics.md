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
- Keep Euler's equation from the formula sheet in front of you. In every question here the axes are fixed to the body, so they turn with it: $\Omega = \omega$, and the $d\omega/dt$ terms are the components of $\alpha$. The equation then reads $\sum M = [I]\alpha + \omega \times ([I]\omega)$.
- Choose the point first: take moments about a fixed point O if the body has one, otherwise about the centre of mass G. The inertia matrix must be about the same point.
- Work it out in steps: $[I]\alpha$, then $H = [I]\omega$, then $\omega \times H$. If the body is at rest ($\omega = 0$) only $[I]\alpha$ is left; if the angular velocity is constant ($\alpha = 0$) only $\omega \times H$ is left.
- The formula sheet gives the moments and products of inertia of standard shapes. Check which axes it uses, and remember that the products go into the matrix with a minus sign.

<br>

## Question 1 

A robotic manipulator moves a casting. The inertia matrix of the casting in terms of a body-fixed coordinate system with its origin at the centre of mass is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.10
\end{bmatrix} \text{ kg m}^2
$$

At the present instant, the angular velocity and angular acceleration of the casting are $\omega$ = 1.2i + 0.8j − 0.4k rad/s and $\alpha$ = 0.26i − 0.07j + 0.13k rad/s$^2$. What moment is exerted about the centre of mass of the casting by the manipulator?

<img src = "figs\06_3D_dynamics\Q1.jpg" width="50%"> <br>

### Answer

$$ \sum M = -0.0057i+0.0202j+0.0178k \text{ N m} $$

## Question 2

A robotic manipulator holds a casting. The inertia matrix of the casting in terms of a body-fixed coordinate system with its origin at the centre of mass is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.10
\end{bmatrix} \text{ kg m}^2
$$

At the present instant, the casting is stationary. If the manipulator exerts a moment $\sum M$ = 0.042i + 0.036j + 0.066k N m about the centre of mass, what is the angular acceleration of the casting at that instant?

<img src = "figs\06_3D_dynamics\Q1.jpg" width="50%"> <br>

### Answer

$$ \alpha = 1.43i+0.987j+0.66k \text{ rad/s}^2 $$


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
\end{bmatrix} \text{ kg m}^2
$$

At the present instant, the rigid body’s angular velocity is $\omega$ = 6i + 6j − 4k rad/s and its angular acceleration is zero. What total moment about O is being exerted on the rigid body?

<img src = "figs\06_3D_dynamics\Q3.jpg" width="50%"> <br>

### Answer

$$ \sum M_O = -76i+36j-60k \text{ N m} $$


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
\end{bmatrix} \text{ kg m}^2
$$

At the present instant, the rigid body’s angular velocity is $\omega$ = 6i + 6j − 4k rad/s. The total moment about O due to the forces and couples acting on the rigid body is zero. What is its angular acceleration?

<img src = "figs\06_3D_dynamics\Q3.jpg" width="50%"> <br>

### Answer

$$ \alpha = \frac{146}{9}i-\frac{50}{9}j+\frac{118}{9}k \approx 16.2i-5.56j+13.1k \text{ rad/s}^2 $$ 

## Question 5

In terms of the coordinate system shown, the inertia matrix of the 6 kg slender bar is

$$ \begin{bmatrix}
I_{xx} & -I_{xy} & -I_{xz}\\
-I_{yx} & I_{yy} & -I_{yz}\\
-I_{zx} & -I_{zy} & I_{zz}
\end{bmatrix} = \begin{bmatrix}
\dfrac{1}{2} & \dfrac{2}{3} & 0\\[4pt]
\dfrac{2}{3} & \dfrac{8}{3} & 0\\[4pt]
0 & 0 & \dfrac{19}{6}
\end{bmatrix} \text{ kg m}^2
$$

The bar is stationary relative to an inertial reference frame when the force F = 12k N is applied at the right end of the bar. No other forces or couples act on the bar. Determine

**(a)** The bar’s angular acceleration relative to the inertial reference frame. <br>
**(b)** The acceleration of the right end of the bar relative to the inertial reference frame at the instant the force is applied.

<img src = "figs\06_3D_dynamics\Q5.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ \alpha = 6i-7.5j \text{ rad/s}^2 $$

**(b)**

$$ a = 11k \text{ m/s}^2 $$


## Question 6

The dimensions of the 20 kg thin plate are h = 0.4 m and b = 0.6 m. The plate is stationary relative to an inertial reference frame when the force F = 10 N is applied in the direction perpendicular to the plate. No other forces or couples act on the plate. At the instant F is applied, what is the magnitude of the acceleration of point A relative to the inertial reference frame?

<img src = "figs\06_3D_dynamics\Q6.jpg" width="50%"> <br>

### Answer

$$ \lvert a_A \rvert = 2.5 \text{ m/s}^2 $$


## Question 7

The thin circular disc of radius R = 0.2 m and mass m = 4 kg is rigidly attached at its centre to the vertical shaft. The plane of the disc is slanted at an angle $\beta$ = 30° relative to the horizontal. The shaft rotates with constant angular velocity $\omega_0$ = 25 rad/s.

Determine the magnitude of the couple exerted on the disc by the shaft.

<img src = "figs\06_3D_dynamics\Q7.jpg" width="50%"> <br>

### Answer

$$ \lvert C \rvert = \frac{25\sqrt{3}}{4} \approx 10.8 \text{ N m} $$

## Question 8

The vertical shaft rotates with constant angular velocity $\omega_0$. The 44.5 N thin rectangular plate is pinned to the shaft at one corner, so that it can swing in its own plane, and the 35° angle between the plate's edge and the shaft remains constant. Determine $\omega_0$.

<img src = "figs\06_3D_dynamics\Q8.jpg" width="50%"> <br>

### Answer

$$ \omega_0 = 7.06 \text{ rad/s} $$

<br><br>

