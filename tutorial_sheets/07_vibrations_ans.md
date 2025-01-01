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


# Tutorial Sheet 7: Vibrations Answers

**Topics covered are:**
- Freely moving spring-mass oscillating systems
- Pendulums

**Tips**
- This needs to be done in radians!
- With spring systems on an angle be really careful if the system is starting at equilibrium, or you need to calculate the starting 'offset'.
- I've used mainly the equations taken directly from the formula sheet, but you can rearrange/combine them for certain variable combos to make them easier for use during the exam.

<br>

## Question 1 

The mass m=4 kg. The spring is unstretched when $x$=0. The period of vibration of the mass is measured and determined to be 0.5 s. The mass is displaced to the position  $x$=0.1 m and released from rest at t=0. Determine its position at t=0.4 s.

<img src = "figs\07_vibrations\Q1.jpg" width="50%"> <br>

### Answer

With the period, we can find spring constant

$$
T = 2\pi\sqrt{\frac{m}{k}} \\
0.5 = 2\pi\sqrt{\frac{4}{k}} \\
k = 631
$$

Then to find the natural frequency

$$
\omega^2 =\frac{k}{m} \\   
\omega = \sqrt{\frac{631}{4}} \\
\omega =  12.56 
$$

Then using the general solution equation with the initial conditions we can find the variables required to construct the displacement equation

$$
x=A\sin(\omega t)+B\cos(\omega t) \\
0.1 = A\sin(12.56t)+B\cos(12.56t), \text{ }t=0 \\
0.1=B
$$

$$
v=\omega A\cos(\omega t)-\omega B\sin(\omega t) \\
0=12.56A\cos(12.56t)-12.56(0.1)\sin(12.56t), \text{ }t=0 \\
0=A
$$

We can now construct the equation and solve

$$
x=0.1\cos(12.56t), \text{ when }t=0.4 \\
x=0.1\cos(5.024) \\
x = 0.0306 \text{ m}
$$

## Question 2

The mass m=4 kg. The spring is unstretched when $x$=0. The frequency of vibration of the mass is measured and determined to be 6 Hz. The mass is displaced to the position $x$=0.1 m and given a velocity $dx/dt$=5 m/s at t=0. Determine the amplitude of the resulting vibration.

<img src = "figs\07_vibrations\Q1.jpg" width="50%"> <br>

### Answer

With the frequency, we can find natural frequency by doing a simple equation sub in/rearrangement

$$
f = \frac{1}{2\pi}\omega \\
6 = \frac{1}{2\pi}\omega \\
\omega = 12\pi
$$

Then using the general solution with conditions provided

$$
x=A\sin(\omega t)+B\cos(\omega t) \\
0.1 = A\sin(12\pi t)+B\cos(12\pi t), \text{ }t=0 \\
0.1=B
$$

$$
v=\omega A\cos(\omega t)-\omega B\sin(\omega t) \\
5=12\pi A\cos(12\pi t)-12\pi(0.1)\sin(12\pi t), \text{ }t=0 \\
\frac{5}{12\pi} = A \\
A = 0.133
$$

The amplitude is then 

$$
E = \sqrt{A^2+B^2} \\
E = \sqrt{0.133^2+0.1^2} \\
E = 0.166 \text{ m}
$$

## Question 3

The 89 N disk rolls on the horizontal surface.Its radius is R=152.4 mm. Determine the spring constant k so that the frequency of vibration of the system relative to its equilibrium position is f=1 Hz.

<img src = "figs\07_vibrations\Q3.jpg" width="50%"> <br>

### Answer

Draw on the forces

<img src = "figs\07_vibrations\Q3ans.jpg" width="50%"> <br>

Write force equations

$$
\sum F_x:-kx+F=ma \\
\sum M: M=I\alpha \\
-FR=\frac{1}{2}mR^2\frac{a}{R}\\
F=\frac{ma}{-2}
$$

Eliminating F we get

$$
-kx+\frac{ma}{-2}=ma \\
kx+\frac{3m}{2}a=0
$$

We can then calculate the appropriate spring constant 

$$
f=\frac{1}{2\pi}\sqrt{\frac{k}{m}}\\
1=\frac{1}{2\pi}\sqrt{\frac{k}{\frac{3m}{2}}} \\
(2\pi)^2=\frac{2k}{3(\frac{89}{0.81})}\\
k=537 \text{N/m}
$$


## Question 4

The 89 N disk rolls on the horizontal surface. Its radius is R=152.4 mm. The spring constant is k=218.9 N/m. At t=0, the spring is unstretched and the disk has a clockwise angular velocity of 2 rad/s. What is the amplitude of the resulting vibrations of the center of the disk?

<img src = "figs\07_vibrations\Q3.jpg" width="50%"> <br>

### Answer

Start in the same way as Q3 but with values provided

$$
\sum F_x:-kx+F=ma \\
\sum M: M=I\alpha \\
-FR=\frac{1}{2}mR^2\frac{a}{R}\\
F=\frac{ma}{-2}
-kx+\frac{ma}{-2}=ma \\
kx+\frac{3m}{2}a=0 \\
13.61\ddot{x}+218.9x=0 \\
$$

Find the natural frequency

$$
\omega = \sqrt{\frac{k}{m}}\\
\omega = \sqrt{\frac{218.9}{13.61}}\\
\omega = 4.04
$$

We need to convert angular velocity to linear velocity so it can be used with the initial conditions

$$
v=\omega r \\
v = (2)(0.1524) \\
v = 0.305
$$

Then using the general equation with provided initial conditions

$$
t=0, x=0,v=0.305
$$

$$
x=A\sin(\omega t)+B\cos(\omega t) + x_0\\
0 = A\sin(4.04t)+B\cos(4.04t) \\
B=0
$$

$$
v=\omega A\cos(\omega t)-\omega B\sin(\omega t) \\
0.305=4.04A\cos(4.04t)-4.04(0)\sin(4.04t) \\
A=0.075
$$

Hence

$$
x=0.075\sin(4.04t)
$$

The amplitude is then 

$$
E = \sqrt{A^2+B^2} \\
E = \sqrt{0.075^2} \\
E = 0.075 \text{ m}
$$

## Question 5

The mass m=4 kg and the spring constant is k=64 N/m. For vibration of the spring-mass oscillator relative to its equilibrium position, determine

**(a)** The frequency <br>
**(b)** The period

<img src = "figs\07_vibrations\Q5.jpg" width="50%"> <br>

### Answer

The question asks for the values relative to the equilibrium position, hence for this question we don't need to take into account the impact of the mass itself on the object's motion.

**(a)** 

$$
f=\frac{1}{2\pi}\sqrt{\frac{k}{m}} \\
f=\frac{1}{2\pi}\sqrt{\frac{64}{4}} \\
f = 0.637 Hz
$$

**(b)**

$$
T=\frac{1}{f}\\
T=\frac{1}{0.637} \\
T=1.57 s
$$

## Question 6

The mass m=4 kg and the spring constant is k=64 N/m. The spring is unstretched when $x$=0. At t=0, $x$=0 and the mass has a velocity of 2 m/s down the inclined surface. What is the value of $x$ at t=0.8 s?

<img src = "figs\07_vibrations\Q5.jpg" width="50%"> <br>

### Answer

Draw the free body diagram

<img src = "figs\07_vibrations\Q6ans.jpg" width="50%"> <br>

We first need to calculate the equilibrium position. The spring will begin stretched as the mass pulls it down the slope, which means the period of the general equation is shifted. Remember when at rest, acceleration is zero.

$$
\sum F_x:4g\sin(20)-kx=ma \\
4g\sin(20)-64x=(4)(0) \\
x=0.21
$$

The natural frequency is

$$
\omega = \sqrt{\frac{k}{m}} \\
\omega = \sqrt{\frac{64}{4}} \\
\omega = 4
$$

Then using the general equation with provided initial conditions

$$
t=0, x=0,v=2
$$

$$
x=A\sin(\omega t)+B\cos(\omega t) + x_0\\
0 = A\sin(4t)+B\cos(4t)+0.21 \\
B=-0.21
$$

$$
v=\omega A\cos(\omega t)-\omega B\sin(\omega t) \\
2=4A\cos(4t)-4(-0.21)\sin(4t) \\
A=0.5
$$

Hence

$$
x=0.5\sin(4t)-0.21\cos(4t)+0.21 , \text{ when }t=0.8\\
x=0.39 \text{ m}
$$

## Question 7

Consider the one-degree of freedom system below (a pendulum). The slender bar is rotated to some angle $\theta$, released, and it oscillates back and forth.

**(a)** Draw the free-body diagram of the bar. <br>
**(b)** Using Newton’s 2nd law write the moment balance about the centre of rotation A. <br>
**(c)** Write the general equation to determine the frequency of a pendulum. <br>
**(d)** Determine the frequency of the pendulum in rad/s and Hz.

<img src = "figs\07_vibrations\Q7.jpg" width="50%"> <br>

### Answer

**(a)**

<img src = "figs\07_vibrations\Q7ans.jpg" width="50%"> <br>

**(b)** Use Newton's second law and moments of inertia formulae for a slender bar

$$
M=I\alpha=\frac{L}{2}mg\sin(\theta) \\
M=\frac{1}{3}mL^2\alpha=\frac{L}{2}mg\sin(\theta) \\
M=\frac{2}{3}L\alpha-g\sin(\theta)
$$

**(c)** Under the assumption that $\theta$ remains small enough to be approximated by $\theta$, the pendulum equation of motion becomes equal to that of the spring mass oscillator (you can prove this using conservation of energy principles, differentiating, then using Taylor series approximations).

Comparing the two

$$
\frac{2}{3}L\alpha-g\sin(\theta)=0, \frac{d^2x}{dt^2}+\frac{k}{m}x=0
$$

and knowing that 

$$
\omega^2=\frac{k}{m}
$$

we can look at like terms and draw that for a pendulum

$$
\omega^2=\frac{g}{L}
$$

**(d)** Getting our force equation from (b) into the appropriate form

$$
\frac{2}{3}L\alpha-g\sin(\theta)=0 \\
\alpha -\frac{3g}{2L}\sin(\theta)=0 \text{, } \sin(\theta)\approx\theta \\
\alpha -\frac{3g}{2L}\theta=0
$$

We then can compare like terms and see

$$
\omega^2=\frac{3g}{2L} \\
\omega=\sqrt{\frac{3g}{2L}} \text{ rad/s}
$$

and in Hz

$$
f = \frac{1}{2\pi}\sqrt{\frac{3g}{2L}}\text{ Hz}
$$

## Question 8

You are asked to design a pendulum clock, and you begin with the pendulum. The mass of the disk is 2 kg. Determine the length L of the bar so that the period of small oscillations of the pendulum is 1 s. For this question, neglect the mass of the bar.

<img src = "figs\07_vibrations\Q8.jpg" width="50%"> <br>

### Answer

Construct the force equation (remember parallel axis theorem) (also remember that $sin\theta\approx\theta$)

$$
M=I\alpha=mg\sin(\theta) \\
(\frac{1}{2}mR^2+m(L+R)^2)\alpha=mg(L+R)(\theta) \\
\alpha+(\frac{2g(L+R)}{r^2+(L+R)^2})\theta=0
$$

The time period expression can then be similarly found (pendulum $\frac{g}{l}$ is like spring $\frac{k}{m}$) and used to solve

$$
\omega = \sqrt{\frac{2g(L+R)}{r^2+(L+R)^2}} \\
T = 2\pi\sqrt{\frac{R^2+(L+R)^2}{2g(L+R)}} \\
1 = 2\pi\sqrt{\frac{0.05^2+(L+0.05)^2}{2g(L+0.05)}} \\
L=0.193 \text{ m}
$$

## Question 9

The spring constant is k=785  N/m. The spring is unstretched when $x$=0. Neglect the mass of the pulley, that is, assume that the tension in the rope is the same on both sides of the pulley. The system is released from rest with $x$=0. Determine $x$=0 as a function of time.

<img src = "figs\07_vibrations\Q9.jpg" width="50%"> <br>

### Answer

Draw the forces

<img src = "figs\07_vibrations\Q9ans.jpg" width="50%"> <br>

For each mass, construct force equations

$$
\sum F_1: T-kx-4g=4a \\
\sum F_2: 20g-T=20a 
$$

Equate T and change notation 

$$
kx+4g+4a = 20g-20a \\
24\ddot{x}+785x-16g=0 \\
$$

We then need to solve the general equation - start with finding the equilibrium position, when a=0

$$
785x_0=16g\\
x_0=0.2
$$

Calculate the natural frequency 

$$
\omega=\sqrt{\frac{k}{m}}\\
\omega=\sqrt{\frac{785}{24}}\\
\omega=5.71
$$

Then solve the general equation

$$
t=0, x=0,v=0
$$

$$
x=A\sin(\omega t)+B\cos(\omega t) + x_0\\
0 = A\sin(5.71t)+B\cos(5.71t)+0.2 \\
B=-0.2
$$

$$
v=\omega A\cos(\omega t)-\omega B\sin(\omega t) \\
2=5.71A\cos(5.71t)-5.71(-0.2)\sin(5.71t) \\
A=0
$$

Hence

$$
x=-0.2\cos(5.71t)+0.2
$$

## Question 10

The spring constant is k=785 N/m. The spring is unstretched with $x$=0. The radius of the pulley is 125 mm, and moment of inertia about its axis is I=0.05 kgm $^2$. The system is released from rest with $x$=0. Determine  $x$ as a function of time.

<img src = "figs\07_vibrations\Q9.jpg" width="50%"> <br>

### Answer

In this question, we need to take into account the pulley as well.

Draw the forces

<img src = "figs\07_vibrations\Q10ans.jpg" width="50%"> <br>

Write force equations

$$
\sum F_1: T_1-kx-4g=4a \\
\sum F_2: 20g-T_2=20a \\
$$

The couple acting is

$$
\sum M=I\alpha\\
(T_2-T_1)(0.125)=0.05\frac{a}{0.125}
$$ 

Eliminating T from the equations

$$
\sum M=I\alpha\\
((20g-20a)-(4a+4g+kx))(0.125)=0.05\frac{a}{0.125} \\
(16g-24a-785x)(0.125)^2=0.05a \\
(16g-24a-785x)(0.125)^2=0.05a \\
2.45-0.375a-12.27x=0.05a \\
0.43a+12.27x-2.45=0 \\
0.43\ddot{x}+12.27x-2.45=0 \\
$$


From here it's the same procedure as Q7 solving the general equation, starting with finding the equilibrium position

$$
12.27x_0=2.45\\
x_0=0.2
$$

Then the natural frequency 

$$
\omega=\sqrt{\frac{k}{m}}\\
\omega=\sqrt{\frac{12.27}{0.43}}\\
\omega=5.34
$$

Then solve the general equation

$$
t=0, x=0,v=0
$$

$$
x=A\sin(\omega t)+B\cos(\omega t) + x_0\\
0 = A\sin(5.34t)+B\cos(5.34t)+0.2 \\
B=-0.2
$$

$$
v=\omega A\cos(\omega t)-\omega B\sin(\omega t) \\
2=5.34A\cos(5.34t)-5.34(-0.2)\sin(5.34t) \\
A=0
$$

Hence

$$
x=-0.2\cos(5.34t)+0.2
$$


<br><br>



