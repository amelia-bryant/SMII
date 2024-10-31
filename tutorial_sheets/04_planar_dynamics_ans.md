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


# Tutorial Sheet 4: Planar Dynamics Answers

Topics covered are 
- Forces, moments, and inertia
- SUVAT
- Inertia from different axes

**Tips**
- With lots of directions and taking forces from different locations, make sure you don't get mixed up.
- aka please draw them out trust me and mark on where your origin is.
- I include circle arrows to indicate which direction the moments are taken around.
- Sometimes part a and b have to be solved in different orders.
<br>

## Question 1 

A horizontal force F=133.4N is applied to the 1023N refrigerator as shown. Friction is negligible.

**(a)** What is the magnitude of the refrigerator’s acceleration? <br>
**(b)** What normal forces are exerted on the refrigerator by the floor at A and B?

<img src = "figs\04_planar_dynamics\Q1.jpg" width="50%"> <br>


### Answer

Draw it out

<img src = "figs\04_planar_dynamics\Q1ans.jpg" width="50%"> <br>

Take forces and moments

$$\sum F_x: F = ma\\
133.4 = \frac{1023}{9.81}a \\
a= 1.27 \text{ m/s, part (a) solved} $$

$$\sum F_y: A+B-1023 = 0 \\
b = 1023-A $$

$$\circlearrowright \sum M_o: (0.8128)(133.4)+(0.3556)A=(0.3556)B $$

Solving

$$ 108.43+0.3556A=0.3556(1023-A) \\
255.35=0.7112A\\
A = 359N, B=664N \text{, solving part (b)}$$

## Question 2

Solve Q1 if the coefficient of kinetic friction at A and B is $\mu_k$=0.1.

### Answer

Draw! 

<img src = "figs\04_planar_dynamics\Q2ans.jpg" width="50%"> <br>

Take forces and moments

$$\sum F_x: F-(f_A+f_B)= ma\\
133.4-(0.1(A+B)) = \frac{1023}{9.81}a $$

$$\sum F_y: A+B-1023 = 0 $$

$$\circlearrowright \sum M_o: (0.8128)(133.4)+(0.3556)A-(0.3556)B+0.7112(0.1B)+0.7112(0.1)A=0\\
108.43+0.3556A-0.3556(1023-A)+0.07112(1023-A)+0.07112(A)=0\\
-182.59+0.7112A=0 \\
A = 256.7N, B=766.3N \text{, solving part (b), and } a=0.3 \text{ m/s, solving (a)}$$ 

## Question 3

As the 2800 N airplane begins its take off run at t=0, its propeller exerts a horizontal force T=1000 N. Neglect horizontal forces exerted on the wheels by the runway.

**(a)** What distance has the airplane moved at t=2s? <br>
**(b)** What normal forces are exerted on the tires at A and B?

<img src = "figs\04_planar_dynamics\Q3.jpg" width="50%"> <br>

### Answer

<img src = "figs\04_planar_dynamics\Q3ans.jpg" width="50%"> <br>

**(a)** 

$$\sum F_x: F = ma \\
1000 = \frac{2800}{9.81}a \\
a = 3.5 $$

Then using suvat 

$$s = ut+\frac{1}{2}at^2\\
s = \frac{1}{2}(3.5)(2)^2 \\
s = 7 m$$

**(b)** 

$$\sum F_y: A+B = 2800 $$

$$\circlearrowright \sum M_o: 5A-1000(1)-2B=0 \\
5A-2(2800-A)=1000 \\
7A = 6600 \\
A=942.9N, B=1857N$$

## Question 4 

The crane moves to the right with constant acceleration, and the 800-kg load moves without swinging.

**(a)** What is the acceleration of the crane and load? <br>
**(b)** What are the tensions in the cables attached at A and B?

<img src = "figs\04_planar_dynamics\Q4.jpg" width="50%"> <br>

### Answer

<img src = "figs\04_planar_dynamics\Q4ans.jpg" width="50%"> <br>

$$\sum F_x: A_x+B_x = 800a\\
A\sin(5)+B\sin(5) = 800a $$

$$\sum F_y: A\cos(5)+B\cos(5) = 800g \\ B = \frac{800g-A\cos(5)}{cos(5)} $$

$$\circlearrowright \sum M_o: A\cos(5)(1.5)-B\cos(5)(1.5)+A\sin(5)(1)+B\sin(5)(1)=0 \\ 1.5A\cos(5)-1.5(\frac{800g-A\cos(5)}{cos(5)})\cos(5)+A\sin(5)+(\frac{800g-A\cos(5)}{cos(5)})\sin(5)=0 \\
A\sin(5)+800g\tan(5)-A\sin(5)+1.5A\cos(5)-(1.5)800g+1.5A\cos(5)=0 \\
11085=3A\cos(5) \\ 
A = 3709N, B=4169N \text{, part (b)} $$
 
$$ 3709\sin(5)+4169\sin(5) = 800a \\
a = 0.858 \text{ m/s}^2 \text{, part (a)} $$


## Question 5

The moment of inertia of the disk about O is I=20 kgm $^2$.At t=0, the stationary disk is subjected to a constant 50 Nm torque.

**(a)** What is the magnitude of the resulting angular acceleration of the disk?<br>
**(b)** How fast is the disk rotating (in rpm) at t=4s?

<img src = "figs\04_planar_dynamics\Q5.jpg" width="50%"> <br>

### Answer

**(a)**

$$ M = I\alpha \\
50=20\alpha \\
\alpha=2.5 \text{ rad/s}^2 $$

**(b)** 

$$\omega=\alpha t \\
= (2.5)(4)\\
= 10 \text{ rad/s} \\
= 95.5 \text{ rpm}$$

## Question 6

The radius of the pulley is 125 mm and the moment of inertia about its axis is I=0.05 kgm $^2$. If the system is released from rest, how far does the 20 kg mass fall in 0.5 s? What is the tension in the rope between the 20 kg mass and the pulley?

<img src = "figs\04_planar_dynamics\Q6.jpg" width="50%"> <br>

### Answer

Draw the free body diagrams

<img src = "figs\04_planar_dynamics\Q6ans.jpg" width="50%"> <br>

Write out equations we know

$$ \sum F_y: T_1-4g=4a \\ 
\sum F_y: 20g-T_2=20a \\
\sum M_o: (T_2-T_1)0.125=0.05\alpha \\
a=0.125\alpha$$

Solve

$$ ((20g-20a)-(4a+4g))0.125=0.05\frac{a}{0.125}\\
2g-3a=0.4a$$

then

$$ a=5.77, T_1=62.32, T_2=80.8N \text{ (tension in rope) }, \alpha=46.2 $$

Using suvat, we can find the distance

$$ s = ut+\frac{1}{2}at^2 \\
s = \frac{1}{2}(5.77)(0.5)^2 \\
s = 0.721m  $$

## Question 7

Points B and C lie in the x–y plane. The axis is vertical. The center of mass of the 18 kg arm BC is at the midpoint of the line from B to C, and the moment of inertia of the arm about the axis through the center of mass that is parallel to the z axis is 1.5 kgm $^2$. At the instant shown, the angular velocity and angular acceleration vectors of arm AB are $\omega_{AB}$=0.6k rad/s and $\alpha_{AB}$=−0.3k rad/s $^2$.The angular velocity and angular acceleration vectors of arm BC are $\omega_{BC}$=0.4k rad/s and $\alpha_{BC}$=2k rad/s $^2$. Determine the force and couple exerted on arm BC at B.

<img src = "figs\04_planar_dynamics\Q7.jpg" width="50%"> <br>

### Answer

<img src = "figs\04_planar_dynamics\Q7ans.jpg" width="50%"> <br>

The acceleration at B is

$$ a_B = a_A + \alpha_{AB}\times r_{B/A} - \omega_{AB}^2 r_{B/A} \\
a_B=0+\begin{vmatrix}
i & j & k\\
0 & 0 & -0.3 \\
0.76\cos(15) & -0.76\sin(15) & 0 
\end{vmatrix} - 0.6^2(0.76\cos(15)i -0.76\sin(15)j) \\
a_B=-0.323i-0.149j \text{ m/s}^2
$$

Denote the CoM of the arm BC as G. The acceleration of G is

$$ a_G = a_B + \alpha_{BC}\times r_{G/B} - \omega_{BC}^2 r_{G/b} \\
a_B=-0.323i-0.149j+\begin{vmatrix}
i & j & k\\
0 & 0 & -0.3 \\
0.45\cos(50) & 0.45\sin(50) & 0 
\end{vmatrix} - 0.4^2(0.45\cos(50)i +0.45\sin(50)j) \\
a_B=-1.059i+0.374j\text{ m/s}^2
$$

Then use dynamic equations

$$ \sum F: B_xi+(B_y-18g)j = 18(-1.059i+0.374j)\\
B_x=-19.1N, B_y = 183.3N$$

$$\sum M=I_{BC}\alpha_{BC} = Fd \\
(1.5)(2) = 0.45\sin(50)(-19.1)-0.45\cos(50)(183.3)+M_B \\
M_B=62.6Nm  $$

## Question 8

An engineer gathering data for the design of a maneuvering unit determines that the astronaut’s center of mass is at x=1.01 m, y=0.16 m and that her moment of inertia about the z axis is 105.6 kgm $^2$. The astronaut’s mass is 81.6 kg. What is her moment of inertia about the z' axis through her center of mass?

<img src = "figs\04_planar_dynamics\Q8.jpg" width="50%"> <br>

### Answer

The distance z' to z can be found

$$ d=\sqrt{d_x^2+d_y^2}
= \sqrt{1.01^2+0.16^2} \\
d=1.02257 $$

Then inertia is

$$ I_{zz}= I_{z'z'}+d^2m \\ 
I_{z'z'} =  105.6-(1.02257)(81.6) \\ I_{z'z'} =  20.27 kgm^2$$

## Question 9

The mass of the object is 10 kg. Its moment of inertia about L $_1$ is 10 kgm $^2$. What is its moment of inertia about L $_2$? The three axes are in the same plane.

<img src = "figs\04_planar_dynamics\Q9.jpg" width="50%"> <br>

### Answer

We can first determine MoI around L, which can be then used to find it around L $_2$

$$ I_{L1}= I_{L}+d^2m  \\
10 = I_{L} + (0.6)^2(10) \\
I_{L1} = 6.4 $$

$$ I_{L2}= I_{L}+d^2m  \\
I_{L2}= 6.4 +(1.2)^2(10) \\
I_{L2}= 20.8 kgm^2 $$

## Question 10

Two homogenous slender bars, each of mass m and length l, are welded together to form the T-shaped object. Use the parallel-axis theorem to determine the moment of inertia of the object about the axis

**(a)** through point O that is perpendicular to the bars.
**(b)** through the center of mass of the object that is perpendicular to the two bars.

<img src = "figs\04_planar_dynamics\Q10.jpg" width="50%"> <br>

### Answer

Call the horizontal bar bar 1, and vertical bar 2

**(a)** Using formulae for the slender bar, bar 1 being the $I_z$ axis and bar 2 being the $I_{z'}$ (visualise where the rotation is occurring, an axis sticking out of the page)

<img src = "figs\04_planar_dynamics\Q10aans.jpg" width="50%"> <br>


$$I_{n'} = I_n+d^2m\\ 
\text{Bar 1: } \frac{1}{3}ml^2+0^2m \\ 
\text{Bar 2: } \frac{1}{12}ml^2+l^2m $$

then sum

$$ = \frac{17}{12}ml^2 $$

**(b)** First we need to find the location of the CoM 

<img src = "figs\04_planar_dynamics\Q10ans.jpg" width="50%"> <br>

$$\frac{0.5li+li}{2} \\
= 0.75li $$

Then similar approach using slender bar equations and the now-calculated CoM

$$I_{n'} = I_n+d^2m\\ 
\text{Bar 1: } \frac{1}{12}ml^2+(\frac{1}{4}l)^2m \\ 
\text{Bar 2: } \frac{1}{12}ml^2+(\frac{1}{4}l)^2m $$

Sum

$$ = \frac{7}{24}ml^2 $$

## Question 11

The rocket is used for atmospheric research. Its weight and its moment of inertia about the z axis through its center of mass (including its fuel) are 44480 N and 13826 kgm $^2$, respectively. The rocket’s fuel weighs 26688 N, its center of mass is located at x=−0.91, y=0, and z=0 m,and the moment of inertia of the fuel about the axis through the fuel’s center of mass parallel to z axis is 2983 kgm $^2$. When the fuel is exhausted, what is the rocket’s moment of inertia about the axis through its new center of mass parallel to z axis?

<img src = "figs\04_planar_dynamics\Q11.jpg" width="50%"> <br>

### Answer

There is a lot of info in this question, so annotating everything will make it a lot easier to digest.

<img src = "figs\04_planar_dynamics\Q11ans.jpg" width="50%"> <br>

Inertia of rocket (mass and fuel) ($I_R$)= inertia of empty rocket ($I_E$) + inertia of fuel ($I_F$)

$$ I_R = I_E+d_E^2m_E + I_F+d_F^2m_F$$

The weight of the empty rocket is evidently

$$ 44480-26688 \\ = 17792N $$

The full rocket CoM can be found with

$$ \frac{(-0.91)(26688)+x(17792)}{44480} =0 \\
x = 1.37 $$

MoI of the empty rocket is then 

$$
13826 = I_E+1.37^2(\frac{17792}{9.81})+2983+(-0.91)^2(\frac{26688}{9.81}) \\
I_E = 5186 kgm^2
$$

## Question 12

Model the arm ABC as a single rigid body. Its mass is 320 kg, and the moment of inertia
about its center of mass is I=360 kgm $^2$. Point A is stationary. If the hydraulic piston exerts a 14 kN force on the arm at B what is the arm’s angular acceleration?

<img src = "figs\04_planar_dynamics\Q12.jpg" width="50%"> <br>

### Answer

Find the inertia of the CoM about A

$$
I_A = 360+(1.8^2+1.1^2)320 \\
= 1784 kgm^2
$$

The angle between B and the horizontal is

$$ \theta = \tan^{-1} (\frac{1.5}{1.4}) = 46.97 $$

The moment can then be found with

$$\circlearrowright \sum M_A: (1.4)1499\sin(46.97) - (0.8)14000\cos(46.97)-(1.8)320g+1784\alpha \\ \alpha = -0.59 rad/s^2 \\
\text{therefore }0.59 rad/s^2 \text{ anticlockwise} $$

## Question 13

A thin ring and a homogeneous circular disk, each of mass m and radius R, are released from rest on an inclined surface. Determine the ratio $v_{ring}/v_{disk}$ of the velocities of the their centers when they have rolled a distance D.

<img src = "figs\04_planar_dynamics\Q13.jpg" width="50%"> <br>

### Answer

<img src = "figs\04_planar_dynamics\Q13ans.jpg" width="50%"> <br>

Write out equations

$$\sum F_x: mg\sin(\theta)-f = ma \\
\sum F_y: N-mg\cos(\theta)=0 \\
\circlearrowright \sum M_o: fR=I\alpha \\
a = R\alpha
$$

Then solving

$$ Ia = fR^2 \\
Ia= (mg\sin(\theta)-ma)R^2 \\
maR^2+Ia=R^2mg\sin(\theta) \\
a = \frac{R^2mg\sin(\theta)}{I+mR^2} $$

The accelerations of each respective disk can be found with their respective inertia

Ring:

$$ I_{ring} = mR^2 \\
a = \frac{R^2mg\sin(\theta)}{mR^2+mR^2} = \frac{g\sin(\theta)}{2}$$

Disk:

$$ I_{ring} = \frac{1}{2}mR^2 \\
a = \frac{R^2mg\sin(\theta)}{\frac{1}{2}mR^2+mR^2} = \frac{2g\sin(\theta)}{3}$$

Velocity ratio can then be calculated

$$ 
v = \sqrt{2aD} \\
\sqrt{\frac{v_{ring}}{v_{disk}}} = \sqrt{\frac{\frac{(2)g\sin(\theta)D}{2}}{\frac{(2)2g\sin(\theta)D}{3}}} \\
= \sqrt{\frac{3}{4}}
$$

<br><br>

