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

The Euler equation on the formula sheet is

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

The axes are fixed to the casting, so they turn with it: their angular velocity $\Omega$ is the casting's angular velocity $\omega$, and the $d\omega/dt$ terms are the components of $\alpha$. The matrix of $\Omega$ components is just the cross product $\omega \times$ written as a matrix, so the equation reads

$$ \sum M = [I]\alpha + \omega \times ([I]\omega) $$

We are given everything, so work out the two terms in turn. First the $[I]\alpha$ term,

$$ [I]\alpha = \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.10
\end{bmatrix} 
\begin{bmatrix}
0.26 \\
-0.07\\
0.13
\end{bmatrix} 
= \begin{bmatrix}
0.0151 \\
-0.0134\\
0.0130
\end{bmatrix} \text{ N m}
$$

Then the angular momentum $H = [I]\omega$,

$$ H = [I]\omega = \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.10
\end{bmatrix} 
\begin{bmatrix}
1.2 \\
0.8\\
-0.4
\end{bmatrix} 
= \begin{bmatrix}
0.036 \\
0.028\\
-0.040
\end{bmatrix} \text{ kg m}^2\text{/s}
$$

and the second term,

$$ \omega \times H = \begin{vmatrix}
i & j & k\\
1.2 & 0.8 & -0.4\\
0.036 & 0.028 & -0.040
\end{vmatrix} = -0.0208i+0.0336j+0.0048k \text{ N m} $$

Adding the two terms,

$$ \sum M = (0.0151-0.0208)i+(-0.0134+0.0336)j+(0.0130+0.0048)k \\
\sum M = -0.0057i+0.0202j+0.0178k \text{ N m}
$$


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

The casting is stationary, so $\omega = 0$ and the $\omega \times ([I]\omega)$ term is zero. What is left is the matrix version of $\sum M = I\alpha$:

$$ \begin{bmatrix}
0.042 \\
0.036\\
0.066
\end{bmatrix} 
= \begin{bmatrix}
0.05 & -0.03 & 0\\
-0.03 & 0.08 & 0\\
0 & 0 & 0.10
\end{bmatrix} 
\begin{bmatrix}
\alpha_x \\
\alpha_y\\
\alpha_z
\end{bmatrix} 
$$

The third row stands on its own: $0.10\alpha_z = 0.066$, so $\alpha_z = 0.66$ rad/s$^2$. The first two rows are two equations in two unknowns,

$$ 0.05\alpha_x - 0.03\alpha_y = 0.042 \\
-0.03\alpha_x + 0.08\alpha_y = 0.036 $$

which give $\alpha_x = 1.43$ rad/s$^2$ and $\alpha_y = 0.987$ rad/s$^2$. So

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

O is a fixed point, so we can take moments about O, using the inertia matrix about O (the one given). The angular acceleration is zero, so only the second term of Euler's equation is left:

$$ \sum M_O = \omega \times H, \qquad H = [I]\omega $$

First the angular momentum,

$$ H = [I]\omega = \begin{bmatrix}
4 & -2 & 0\\
-2 & 3 & 1\\
0 & 1 & 5
\end{bmatrix}
\begin{bmatrix}
6 \\
6\\
-4
\end{bmatrix} 
= \begin{bmatrix}
12 \\
2\\
-14
\end{bmatrix} \text{ kg m}^2\text{/s}
$$

then

$$ \sum M_O = \omega \times H = \begin{vmatrix}
i & j & k\\
6 & 6 & -4\\
12 & 2 & -14
\end{vmatrix} \\
= [(6)(-14)-(-4)(2)]i + [(-4)(12)-(6)(-14)]j + [(6)(2)-(6)(12)]k \\
\sum M_O = -76i+36j-60k \text{ N m}
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
\end{bmatrix} \text{ kg m}^2
$$

At the present instant, the rigid body’s angular velocity is $\omega$ = 6i + 6j − 4k rad/s. The total moment about O due to the forces and couples acting on the rigid body is zero. What is its angular acceleration?

<img src = "figs\06_3D_dynamics\Q3.jpg" width="50%"> <br>

### Answer

Now the total moment about O is zero, so Euler's equation gives

$$ 0 = [I]\alpha + \omega \times ([I]\omega) \quad\Rightarrow\quad [I]\alpha = -\,\omega \times ([I]\omega) $$

$\omega$ and $[I]$ are the same as in Question 3, so $\omega \times ([I]\omega)$ = −76i + 36j − 60k N m, and

$$ \begin{bmatrix}
4 & -2 & 0\\
-2 & 3 & 1\\
0 & 1 & 5
\end{bmatrix} 
\begin{bmatrix}
\alpha_x \\
\alpha_y\\
\alpha_z
\end{bmatrix} 
= \begin{bmatrix}
76 \\
-36\\
60
\end{bmatrix} $$

Rows 1 and 3 give $\alpha_x$ and $\alpha_z$ in terms of $\alpha_y$, and substituting both into row 2 gives $\alpha_y$:

$$ \begin{aligned}
4\alpha_x - 2\alpha_y &= 76 &&\Rightarrow\quad \alpha_x = 19 + \frac{1}{2}\alpha_y \\
\alpha_y + 5\alpha_z &= 60 &&\Rightarrow\quad \alpha_z = 12 - \frac{1}{5}\alpha_y \\
-2\alpha_x + 3\alpha_y + \alpha_z &= -36 &&\Rightarrow\quad -26 + \frac{9}{5}\alpha_y = -36 \quad\Rightarrow\quad \alpha_y = -\frac{50}{9}
\end{aligned} $$

Then

$$ \alpha_x = 19 - \frac{25}{9} = \frac{146}{9}, \qquad \alpha_z = 12 + \frac{10}{9} = \frac{118}{9} $$

so

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

**(a)** The origin of the coordinate system is the bar's centre of mass G. The bar is stationary, so $\omega = 0$ and Euler's equation about G is just $\sum M_G = [I]\alpha$. To find the moment of F about G, first locate G.

<img src = "figs\06_3D_dynamics\Q5ans.jpg" width="50%"> <br>

The bar is 3 m long and 6 kg, so the 1 m leg is 2 kg and the 2 m leg is 4 kg. Measuring from the corner, with each leg's mass at its midpoint,

$$ x_G = \frac{(2)(0)+(4)(1)}{6} = \frac{2}{3} \text{ m}, \qquad y_G = \frac{(2)(0.5)+(4)(0)}{6} = \frac{1}{6} \text{ m} $$

F acts out of the page at the right end A, which is 2 m from the corner, so the position of A relative to G is

$$ r_{A/G} = \left(2-\frac{2}{3}\right)i - \frac{1}{6}j = \frac{4}{3}i - \frac{1}{6}j \text{ m} $$

No couples act, so the moment about G is

$$ \sum M_G = r_{A/G} \times F = \begin{vmatrix}
i & j & k\\[4pt]
\dfrac{4}{3} & -\dfrac{1}{6} & 0 \\[4pt]
0 & 0 & 12
\end{vmatrix} = \left(-\frac{1}{6}\right)(12)\,i - \left(\frac{4}{3}\right)(12)\,j = -2i-16j \text{ N m} $$

Then $[I]\alpha = \sum M_G$. Every entry of the inertia matrix is a whole number of sixths, so take out the factor 1/6:

$$ \frac{1}{6}\begin{bmatrix}
3 & 4 & 0\\
4 & 16 & 0\\
0 & 0 & 19
\end{bmatrix} 
\begin{bmatrix}
\alpha_x \\
\alpha_y\\
\alpha_z
\end{bmatrix} 
= \begin{bmatrix}
-2 \\
-16 \\
0 \end{bmatrix} $$

The third row gives $\alpha_z = 0$. Multiplying the first two rows by 6 clears the fractions,

$$ \begin{aligned}
3\alpha_x + 4\alpha_y &= -12 \\
4\alpha_x + 16\alpha_y &= -96
\end{aligned} $$

Dividing the second row by 4 gives $\alpha_x + 4\alpha_y = -24$, and subtracting this from the first row gives $2\alpha_x = 12$. So

$$ \alpha_x = 6, \qquad \alpha_y = \frac{-24-6}{4} = -\frac{15}{2} \\
\alpha = 6i-7.5j \text{ rad/s}^2 $$

**(b)** Newton's second law gives the acceleration of G,

$$ F = ma_G \quad\Rightarrow\quad 12k = 6a_G \quad\Rightarrow\quad a_G = 2k \text{ m/s}^2 $$

Then use the rigid body acceleration equation from G to A, with $\omega = 0$ at this instant,

$$
a_A=a_G+\alpha \times r_{A/G}+\omega \times(\omega \times r_{A/G}) \\
a_A = 2k+\begin{vmatrix}
i & j & k\\[4pt]
6 & -\dfrac{15}{2} & 0\\[4pt]
\dfrac{4}{3} & -\dfrac{1}{6} & 0
\end{vmatrix} +0 \\
a_A = 2k + \left[(6)\left(-\frac{1}{6}\right)-\left(-\frac{15}{2}\right)\left(\frac{4}{3}\right)\right]k = 2k + (-1+10)k \\
a_A = 11k \text{ m/s}^2
$$

## Question 6

The dimensions of the 20 kg thin plate are h = 0.4 m and b = 0.6 m. The plate is stationary relative to an inertial reference frame when the force F = 10 N is applied in the direction perpendicular to the plate. No other forces or couples act on the plate. At the instant F is applied, what is the magnitude of the acceleration of point A relative to the inertial reference frame?

<img src = "figs\06_3D_dynamics\Q6.jpg" width="50%"> <br>

### Answer

The plate is stationary, so $\omega = 0$ and only the $[I]\alpha$ term of Euler's equation is left. There is no fixed point, so take moments about the centre of mass G, with x along b, y along h and z perpendicular to the plate:

<img src = "figs\06_3D_dynamics\Q6ans.jpg" width="50%"> <br>

From the formula sheet (thin rectangular plate, axes through the centre of mass),

$$ [I] = \begin{bmatrix}
\dfrac{1}{12}mh^2 & 0 & 0\\[4pt]
0 & \dfrac{1}{12}mb^2 & 0\\[4pt]
0 & 0 & \dfrac{1}{12}m(b^2+h^2)
\end{bmatrix} = \begin{bmatrix}
\dfrac{4}{15} & 0 & 0\\[4pt]
0 & \dfrac{3}{5} & 0\\[4pt]
0 & 0 & \dfrac{13}{15}
\end{bmatrix} \text{ kg m}^2
$$

F pushes into the plate, so F = −10k N, and it acts at the bottom right corner, $r$ = 0.3i − 0.2j m from G. No couples act, so

$$ \sum M_G = r \times F = \begin{vmatrix}
i & j & k\\
0.3 & -0.2 & 0\\
0 & 0 & -10
\end{vmatrix} = 2i+3j \text{ N m} $$

Then $[I]\alpha = \sum M_G$. The inertia matrix is diagonal, so each row stands on its own:

$$ \alpha_x = 2 \times \frac{15}{4} = 7.5, \qquad \alpha_y = 3 \times \frac{5}{3} = 5, \qquad \alpha_z = 0 \\
\alpha = 7.5i+5j \text{ rad/s}^2
$$

Newton's second law gives the acceleration of G,

$$ F = ma_G \quad\Rightarrow\quad -10k = 20a_G \quad\Rightarrow\quad a_G = -0.5k \text{ m/s}^2 $$

A is the top left corner, so $r_{A/G}$ = −0.3i + 0.2j m, and with $\omega = 0$

$$
a_A=a_G+\alpha \times r_{A/G}+\omega \times(\omega \times r_{A/G}) \\
a_A = -0.5k+\begin{vmatrix}
i & j & k\\
7.5 & 5 & 0\\
-0.3 & 0.2 & 0
\end{vmatrix} +0 = -0.5k + 3k = 2.5k \text{ m/s}^2
$$

The question asks for the magnitude,

$$ \lvert a_A \rvert = 2.5 \text{ m/s}^2 $$

## Question 7

The thin circular disc of radius R = 0.2 m and mass m = 4 kg is rigidly attached at its centre to the vertical shaft. The plane of the disc is slanted at an angle $\beta$ = 30° relative to the horizontal. The shaft rotates with constant angular velocity $\omega_0$ = 25 rad/s.

Determine the magnitude of the couple exerted on the disc by the shaft.

<img src = "figs\06_3D_dynamics\Q7.jpg" width="50%"> <br>

### Answer

Draw the disc edge-on, with body-fixed axes x'y'z': z' perpendicular to the disc, y' in the plane of the disc pointing up the slope, and x' into the page.

<img src = "figs\06_3D_dynamics\Q7ans.jpg" width="50%"> <br>

The disc's centre G is on the shaft's axis, so it does not move. The shaft exerts a force on the disc, which balances the weight, and the couple C that we want. The weight and the shaft's force both act through G, so taking moments about G,

$$ \sum M_G = C $$

These axes lie along the disc's axes of symmetry, so the formula sheet (thin circular plate) gives

$$ [I] = \begin{bmatrix}
\dfrac{1}{4}mR^2 & 0 & 0\\[4pt]
0 & \dfrac{1}{4}mR^2 & 0\\[4pt]
0 & 0 & \dfrac{1}{2}mR^2
\end{bmatrix} = \begin{bmatrix}
0.04 & 0 & 0\\
0 & 0.04 & 0\\
0 & 0 & 0.08
\end{bmatrix} \text{ kg m}^2
$$

The disc turns with the shaft, about the vertical. The vertical is at $\beta$ to z' and at $90^\circ - \beta$ to y', so in the body axes, keeping $\cos 30^\circ = \sqrt{3}/2$ exact,

$$ \omega = \omega_0\sin\beta\, j' + \omega_0\cos\beta\, k' = 25\sin 30^\circ\, j' + 25\cos 30^\circ\, k' = \frac{25}{2}j' + \frac{25\sqrt{3}}{2}k' \text{ rad/s} $$

$\omega$ is constant, so $\alpha = 0$ and only the second term of Euler's equation is left. First the angular momentum,

$$ H = [I]\omega = \begin{bmatrix}
0.04 & 0 & 0\\[4pt]
0 & 0.04 & 0\\[4pt]
0 & 0 & 0.08
\end{bmatrix}
\begin{bmatrix}
0 \\[4pt]
\dfrac{25}{2}\\[4pt]
\dfrac{25\sqrt{3}}{2}
\end{bmatrix} 
= \begin{bmatrix}
0 \\[4pt]
\dfrac{1}{2}\\[4pt]
\sqrt{3}
\end{bmatrix} \text{ kg m}^2\text{/s}
$$

then

$$ C = \omega \times H = \begin{vmatrix}
i' & j' & k'\\[4pt]
0 & \dfrac{25}{2} & \dfrac{25\sqrt{3}}{2}\\[4pt]
0 & \dfrac{1}{2} & \sqrt{3}
\end{vmatrix} = \left[\left(\frac{25}{2}\right)\left(\sqrt{3}\right)-\left(\frac{25\sqrt{3}}{2}\right)\left(\frac{1}{2}\right)\right] i' \\
C = \left(\frac{25\sqrt{3}}{2} - \frac{25\sqrt{3}}{4}\right) i' = \frac{25\sqrt{3}}{4}\, i' \text{ N m} $$

So the magnitude of the couple is

$$ \lvert C \rvert = \frac{25\sqrt{3}}{4} \approx 10.8 \text{ N m} $$

It acts about x', into the page. In the figure it turns the disc clockwise, towards a steeper slope: without it, the spinning disc would turn towards horizontal.

## Question 8

The vertical shaft rotates with constant angular velocity $\omega_0$. The 44.5 N thin rectangular plate is pinned to the shaft at one corner, so that it can swing in its own plane, and the 35° angle between the plate's edge and the shaft remains constant. Determine $\omega_0$.

<img src = "figs\06_3D_dynamics\Q8.jpg" width="50%"> <br>

### Answer

The plate is pinned at O, on the shaft's axis, so O is a fixed point: take moments about O, with axes fixed to the plate and their origin at O. In the figure x runs along the edge of length b = 0.61 m, y along the edge of length h = 0.31 m, and z is perpendicular to the plate.

<img src = "figs\06_3D_dynamics\Q8ans.jpg" width="50%">  <br>

The forces on the plate are its weight W = 44.5 N, acting at the centre of mass G, and the force from the pin. The pin's force acts through O, so it has no moment about O. The pin can also exert couples about x and y, but not about its own axis z. So the z component of Euler's equation contains only the weight, and that is the one we need.

First the inertia matrix about O, from the formula sheet (thin rectangular plate, axes at a corner), with $m$ = 44.5/9.81 = 4.536 kg:

$$ [I_O] = \begin{bmatrix}
\dfrac{1}{3}mh^2 & -\dfrac{1}{4}mbh & 0\\[4pt]
-\dfrac{1}{4}mbh & \dfrac{1}{3}mb^2 & 0\\[4pt]
0 & 0 & \dfrac{1}{3}m(b^2+h^2)
\end{bmatrix} = \begin{bmatrix}
0.1453 & -0.2144 & 0\\
-0.2144 & 0.5626 & 0\\
0 & 0 & 0.7079
\end{bmatrix} \text{ kg m}^2
$$

The product of inertia $I_{xy} = \frac{1}{4}mbh$ goes into the matrix with a minus sign.

The vertical is at 35° to the x axis, so the weight in these axes is

$$
W = 44.5(\cos 35^\circ\, i - \sin 35^\circ\, j) = 36.45i - 25.52j \text{ N}
$$

G is at $r_{G/O}$ = 0.305i + 0.155j m, so the moment about O is

$$
\sum M_O = r_{G/O} \times W = \begin{vmatrix}
i & j & k\\
0.305 & 0.155 & 0\\
36.45 & -25.52 & 0
\end{vmatrix} = -13.43k \text{ N m}
$$

The plate turns with the shaft, about the vertical (its sense does not matter, as $\omega_0$ ends up squared):

$$
\omega = \omega_0(-\cos 35^\circ\, i + \sin 35^\circ\, j) = \omega_0(-0.8192i + 0.5736j)
$$

$\omega_0$ is constant, so $\alpha = 0$ and only the second term of Euler's equation is left. With $\omega_0$ taken out of each vector, the angular momentum is

$$ H_O = [I_O]\omega = \omega_0 \begin{bmatrix}
0.1453 & -0.2144 & 0\\
-0.2144 & 0.5626 & 0\\
0 & 0 & 0.7079
\end{bmatrix}
\begin{bmatrix}
-0.8192 \\
0.5736 \\
0
\end{bmatrix} = \omega_0 \begin{bmatrix}
-0.2420 \\
0.4983 \\
0
\end{bmatrix} $$

and

$$ \omega \times H_O = \omega_0^2 \begin{vmatrix}
i & j & k\\
-0.8192 & 0.5736 & 0\\
-0.2420 & 0.4983 & 0
\end{vmatrix} = \omega_0^2\,[(-0.8192)(0.4983)-(0.5736)(-0.2420)]\,k = -0.2694\,\omega_0^2\,k $$

Its x and y components are zero, so here the pin exerts no couple about x or y. The z components give

$$
-13.43 = -0.2694\,\omega_0^2 \quad\Rightarrow\quad \omega_0 = 7.06 \text{ rad/s}
$$

The answer is sensitive to rounding, so keep four significant figures in the working.


<br><br>

