<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>



# Tutorial Sheet 10: Damped and Force Vibrations

**Topics covered are:**
- Damped vibrations
- Forced vibrations
- Rotational vibrations

**Tips**
- Even though the equations are getting longer, as long as you  make sure you know what all the parameters are, you are familiar with the equations, and how to manipulate them, you shouldn't have too much of an issue.
- Instead of calculating all the variables, you can start to recognise them directly by inspection from the equations - this can be quicker, but make you more prone to mistakes

<br>

## Question 1 

The mass m=2 kg, the spring constant is k=72 N/m, and the damping constant is c=8 Ns/m. The spring is unstretched when $x$=0. The mass is displaced to the position $x$=1 m and released from rest.

(a) What is the frequency of the resulting damped vibrations?

(b) What is the value of $x$ at t=1 s?

<img src = "figs\08_vibrations_dampedforced\Q1.jpg" width="50%"> <br>


### Answer

(a) First we need to know what kind of damped the system is. This depends on d (damping coefficient) and the undamped angular frequency

$$
\omega = \sqrt{\frac{k}{m}} \text{, } d=\frac{c}{2m} \\
\omega = \sqrt{\frac{72}{2}} \text{, } d=\frac{8}{2(2)}\\
\omega = 6 \text{, } d=2 \\
\omega > d \therefore \text{subcritical damping}
$$

Then we can find the angular frequency

$$
\omega_d=\sqrt{{\omega^2}-{d^2}} \\
\omega_d=\sqrt{{6^2}-{2^2}} \\
\omega_d=5.66 \text{ rad/s}
$$

Which allows us to find the frequency of the damped vibrations

$$
f_d = \frac{\omega_d}{2\pi} \\
f_d = \frac{5.66}{2\pi} \\
f_d = 0.9 \text{ Hz}
$$

(b) Solve the differential equation using the subcritical damped system equation and initial conditions provided 

$$
t=0,x=1,v=0
$$

$$
x=e^{-dt}(A\sin(\omega_dt)+B\cos(\omega_dt))\\
1=e^{0}(B\cos(5.66(0))) \\
B=1
$$

$$
v=e^{-dt}([A\omega_d-Bd]\cos(\omega_dt)-[B\omega_d+Ad]\sin(\omega_dt)) \\
0=e^{0}([A(5.66)-(1)(2)]\cos(5.66(0))) \\
0=5.66A-2 \\
A = 0.353
$$

Hence

$$
x=e^{-dt}(0.353\sin(5.66t)+\cos(5.66t))\text{, when t=1}\\
x=0.0816 \text{ m}
$$

## Question 2

The mass m=2 kg, the spring constant is k=72 N/m, and the damping constant is c=32 Ns/m. The spring is unstretched when $x$=0. The mass is displaced to the position $x$=1 m and released from rest.

(a) What is the frequency of the resulting damped vibrations?

(b) What is the value of $x$ at t=1 s?

<img src = "figs\08_vibrations_dampedforced\Q1.jpg" width="50%"> <br>

### Answer

(a) Calculate the type of damping

$$
\omega = \sqrt{\frac{k}{m}} \text{, } d=\frac{c}{2m} \\
\omega = \sqrt{\frac{72}{2}} \text{, } d=\frac{32}{2(2)}\\
\omega = 6 \text{, } d=8 \\
d > \omega \therefore \text{supercritical damping}
$$

Then find the angular frequency and frequency of the damped vibrations

$$
\omega_d=\sqrt{{\omega^2}-{d^2}} \\
\omega_d=\sqrt{{6^2}-{8^2}} \\
\omega_d=5.29 \text{ rad/s}
f_d = \frac{\omega_d}{2\pi} \\
f_d = \frac{5.29}{2\pi} \\
f_d = 0.084 \text{ Hz}
$$

(b) For supercritical damping we need the variable 'h'

$$
h = \sqrt{d^2-\omega^2}\\
h = \sqrt{8^2-6^2}\\
h = 5.29
$$

Solve the differential equation using the supercritical damped system equation and initial conditions provided 

$$
t=0,x=1,\dot{x}=0
$$

$$
x=Ae^{-(d-h)t}+Be^{-(d+h)t}\\
1=Ae^{-(2.71)0}+Be^{-(13.29)0}\\
1=A+B
$$

$$
\dot{x}=-(d-h)Ae^{-(d-h)t}-(d+h)Be^{-(d+h)t}\\
0=-2.71A-13.29B \\
$$

$$
\therefore A = 1.26\text{, } B=-0.26
$$

Hence

$$
x=1.26e^{-2.71t}+-0.26e^{-13.3t}\text{, when t=1}\\
x=0.0837 \text{ m}
$$

## Question 3

The mass m=2 kg, the spring constant is k=8 N/m, and the damping coefficient is c=12 Ns/m. The spring is unstretched when $x$=0. At t=0, the mass is released from rest with $x$=0. Determine the value of $x$ at t=2 s.

<img src = "figs\08_vibrations_dampedforced\Q3.jpg" width="50%"> <br>

### Answer

We first need to find the resting, equilibrium position

$$
\sum F: mg\sin(20)-kx-c\dot{x}=m\ddot{x} \text{, v=0, a=0}\\  
6.71-8x_0=0 \\
x_0=0.839 \\
$$

Identify the type of damping

$$
\omega = \sqrt{\frac{k}{m}} \text{, } d=\frac{c}{2m} \\
\omega = \sqrt{\frac{8}{2}} \text{, } d=\frac{12}{2(2)}\\
\omega = 2 \text{, } d=3 \\
d > \omega \therefore \text{supercritical damping}
$$

Find variables needed to solve

$$
h = \sqrt{d^2-\omega^2}\\
h = \sqrt{3^2-2^2}\\
h = 2.24
$$

Then solve differential

$$
t=0,x=0,\dot{x}=0
$$

$$
x=Ae^{-(d-h)t}+Be^{-(d+h)t}+x_0\\
0=Ae^{-(0.76)0}+Be^{-(5.24)0}+0.839\\
0=A+B+0.839
$$

$$
\dot{x}=-(d-h)Ae^{-(d-h)t}-(d+h)Be^{-(d+h)t}\\
0=-0.76A-5.24B \\
$$

$$
\therefore A = -0.981\text{, } B=0.142
$$

Hence

$$
x=-0.981e^{-0.76t}+0.142e^{-5.24t}+0.839\text{, when t=2}\\
x=0.624 \text{ m}
$$

## Question 4

A 79.8 kg test car moving with velocity $v_0$=7.33 m/s collides with a rigid barrier at t=0. As a result of the behavior of its energy-absorbing bumper, the response of the car to the collision can be simulated by the damped spring-mass oscillator shown with k=8000 N/m and c=3000 Ns/m. Assume that the mass is moving to the left with velocity $v_0$=7.33 m/s and the spring is unstretched at t=0. Determine the car’s deceleration 

(a) immediately after it contacts the barrier

(b) at t=0.08 s.

<img src = "figs\08_vibrations_dampedforced\Q4.jpg" width="50%"> <br>

### Answer

To solve both parts, we need to find the specific equation for acceleration - for which equation to solve, we need to find the type of damping. 

$$
\omega = \sqrt{\frac{k}{m}} \text{, } d=\frac{c}{2m} \\
\omega = \sqrt{\frac{8000}{79.8}} \text{, } d=\frac{3000}{2(79.8)}\\
\omega = 10.01 \text{, } d=18.8 \\
d > \omega \therefore \text{supercritical damping}
$$

Find variables needed to solve

$$
h = \sqrt{d^2-\omega^2}\\
h = \sqrt{18.8^2-10.01^2}\\
h = 15.9
$$

Solve the differential to find values for A and B

$$
t=0,x=0,\dot{x}=-7.33
$$

$$
x=Ae^{-(d-h)t}+Be^{-(d+h)t}\\
0=Ae^{-(2.9)0}+Be^{-(34.7)0}\\
0=A+B
$$

$$
\dot{x}=-(d-h)Ae^{-(d-h)t}-(d+h)Be^{-(d+h)t}\\
-7.33=-2.9A-34.7B \\
$$

Solving simultaneously

$$
A = -0.23\text{, } B=0.23
$$

Then subbing these values into the supercritically damped equation for velocity

$$
\dot{x}=-(d-h)Ae^{-(d-h)t}-(d+h)Be^{-(d+h)t}\\
\dot{x}=-(2.9)(-0.23)e^{-(2.9)t}-(34.7)(0.23)e^{-(34.7)t}\\
\dot{x}=0.667e^{-2.9t}-7.98e^{-34.7t}\\
$$

Differentiate to get acceleration

$$
\ddot{x} = -1.9e^{-2.9t}+276.9e^{-34.7t}
$$

Finding the accelerations at the specified times is then simple, subbing in.

(a) When t=0

$$
\ddot{x}=275 \text{m/s}^2
$$
<br><br>

(b) When t=0.08

$$
\ddot{x}=25.7 \text{m/s}^2
$$
<br><br>

## Question 5

The motion of a car’s suspension shown can be modeled as a damped spring–mass oscillator with m=36 kg, k=22 kN/m, and c=2.2 kNs/m. Assume that no external forces act on the tire and wheel. At t=0, the spring is unstretched and the tire and wheel are given a velocity dx/dt=10 m/s. Determine the position x as a function of time.

<img src = "figs\08_vibrations_dampedforced\Q5.jpg" width="50%"> <br>

### Answer

As the spring is not stated to be in static equilibrium, we need to find the initial displacement of the system due to its own weight.

$$
\sum F: -mg+kx+c\dot{x}=m\ddot{x} \text{, v=0, a=0}\\  
-353.16+22000x_0=0 \\
x_0=0.016 \\
$$

Identify the type of damping

$$
\omega = \sqrt{\frac{k}{m}} \text{, } d=\frac{c}{2m} \\
\omega = \sqrt{\frac{22000}{36}} \text{, } d=\frac{2200}{2(36)}\\
\omega = 24.7 \text{, } d=30.6 \\
d > \omega \therefore \text{supercritical damping}
$$

Find variables needed to solve

$$
h = \sqrt{d^2-\omega^2}\\
h = \sqrt{30.6^2-24.7^2}\\
h = 18
$$

Then solve differential

$$
t=0,x=0,\dot{x}=10
$$

$$
x=Ae^{-(d-h)t}+Be^{-(d+h)t}+x_0\\
0=Ae^{-(12.6)0}+Be^{-(48.6)0}+0.016\\
0=A+B+0.016
$$

$$
\dot{x}=-(d-h)Ae^{-(d-h)t}-(d+h)Be^{-(d+h)t}\\
10=-12.6A-48.6B \\
$$

$$
\therefore A = 0.256\text{, } B=-0.272
$$

Hence

$$
x=0.256e^{-12.6t}-0.272e^{-48.6t}+0.016
$$

## Question 6

The mass m=2 kg and the spring constant is k=72 N/m. The spring is unstretched when x=0. The mass is initially stationary with the spring unstretched, and at t=0 the force F(t)= 10sin(4t) applied to the mass. What is the position of the mass at t=2s?

<img src = "figs\08_vibrations_dampedforced\Q6.jpg" width="50%"> <br>

### Answer

The equation of motion can be written 

$$
\sum F : m\ddot{x}+kx=F(t) \\
\ddot{x}+\frac{k}{m}x=\frac{F(t)}{m} \\
\ddot{x}+\frac{72}{2}x=\frac{10\sin(4t)}{2} \\
\ddot{x}+36x=5\sin(4t) \\
$$

Then by inspection 

$$
\ddot{x}+\frac{c}{m}\dot{x}+\frac{k}{m}x=a_0\sin(\omega_0t)+b_0\cos(\omega_0t) \\
\omega = 6, \omega_0=4, d=0, a_0=5, b_0=0
$$

The complete solution can be found by summing the homogenous and particular solutions

$$
x = x_h+x_p
$$

To find the particular solution $x_p$

$$
A_p=\frac{(\omega^2-\omega_0^2)a_0+2d\omega_0b_0}{(\omega^2-\omega_0^2)^2+4d^2\omega_0^2} \\
A_p=\frac{(6^2-4^2)5}{(6^2-4^2)^2} \\
A_p =  0.25
$$

$$
B_p=\frac{-2d\omega_0a_0+(\omega^2-\omega_0^2)b_0}{(\omega^2-\omega_0^2)^2+4d^2\omega_0^2} \\
B_p =  0
$$

The particular solution is then

$$
x_p = A_p\sin(\omega_0t)+B_p\cos(\omega_0t) \\
x_p = 0.25\sin(4t)
$$

Hence

$$
x = A\sin(6 t) + B\cos(6 t) + 0.25\sin(4t)
$$

Then solve the differential with initial conditions provided

$$
t=0,x=0,\dot{x}=0
$$

$$
x = A\sin(6 t) + B\cos(6 t) + 0.25\sin(4t) \\
0 = B
$$

$$
\dot{x} = 6A\cos(6t) - 6B\sin(6t) + \sin(4t) \\
0 = 6A+1 \\
A = -0.167
$$

$$
\therefore A = -0.167 \text{, } B=0
$$

Hence

$$
x= -0.167\sin(6t)+ 0.25\sin(4t)\text{, when t=2}\\
x=0.337 \text{ m}
$$

## Question 7

The damped spring–mass oscillator is initially stationary with the spring unstretched. At t=0, a constant force F(t)=6 N is applied to the mass.

(a) What is the steady-state (particular) solution?

(b) Determine the position of the mass as a function of time.
 
<img src = "figs\08_vibrations_dampedforced\Q7.jpg" width="50%"> <br>

### Answer

(a) Using Newton II

$$
\sum F: F(t)-c\dot{x}-kx=m\ddot{x} \\
\sum F: 6-6\dot{x}-12x=3\ddot{x} \\
$$

Then rearranging into the form we are more familiar with (you may have skipped right to this step)

$$
3\ddot{x}+6\dot{x}+12x=6
$$

Because F(t) is a constant, the particular solution will also be a constant. The steady state solution is when velocity and acceleration are zero, hence

$$
12x=6\\
\therefore x_p=0.5
$$

(b) Because we have a damping term, we need to work out the type of damping in order too use the correct homogenous solution 

$$
\omega = \sqrt{\frac{k}{m}} \text{, } d=\frac{c}{2m} \\
\omega = \sqrt{\frac{12}{3}} \text{, } d=\frac{6}{2(3)}\\
\omega = 2 \text{, } d=1 \\
\omega > d \therefore \text{subcritical damping}
$$

Find variables needed to solve

$$
\omega_d=\sqrt{{\omega^2}-{d^2}} \\
\omega_d=\sqrt{{2^2}-{1^2}} \\
\omega_d=\sqrt{3} \text{ rad/s}
$$

Then solve using initial conditions provided
$$
t=0,x=0,\dot{x}=0
$$

$$
x=e^{-dt}(A\sin(\omega_dt)+B\cos(\omega_dt))\\
0=e^{-t}(A\sin(\sqrt{3}t)+B\cos(\sqrt{3}t))+0.5\\
0=B+0.5 \\
B=-0.5
$$

$$
v=e^{-dt}([A\omega_d-Bd]\cos(\omega_dt)-[B\omega_d+Ad]\sin(\omega_dt)) \\
0=e^{-t}([A\sqrt{3}+0.5]\cos(\sqrt{3}t)-[-0.5\sqrt{3}+A]\sin(\sqrt{3}t)) \\
0=A\sqrt{3}+0.5\\
A = -0.29
$$

Hence

$$
x_h=e^{-t}(-0.29\sin(\sqrt{3}t)-0.5\cos(\sqrt{3}t))
$$

Summing the homogenous and particular solution,

$$
x=e^{-t}(-0.29\sin(\sqrt{3}t)-0.5\cos(\sqrt{3}t))+0.5
$$

## Question 8

The disk with moment of inertia I=3 kgm $^2$ rotates about a fixed shaft and is attached to a torsional spring with constant k=20 Nm/rad. At t=0, the angle $\theta$=0, the angular velocity is $\frac{d\theta}{dt}$=4 rad/s, and the disk is subjected to a couple M(t)=10sin(2t) Nm. Determine $\theta$ as a function of time.

<img src = "figs\08_vibrations_dampedforced\Q8.jpg" width="50%"> <br>

### Answer

Though movement is now rotational, the equation of motion is similar to the one we have seen with terms altered

$$
I\ddot{\theta}+k\dot{\theta}=M(t) \\
\ddot{\theta}+\frac{k}{I}\dot{\theta}=\frac{M(t)}{I} \\
\ddot{\theta}+\frac{20}{3}\dot{\theta}=\frac{10\sin(2t)}{3} \\
\ddot{\theta}+6.67\dot{\theta}=3.33\sin(2t) \\
$$

By inspection

$$
\omega=\sqrt{6.67}=2.58, \omega_0=2, a_0=3.33, b_0=0, d=0
$$

The complete solution can be found by summing the homogenous and particular solutions

$$
\theta = \theta_h+\theta_p
$$

To find the particular solution $x_p$

$$
A_p=\frac{(\omega^2-\omega_0^2)a_0+2d\omega_0b_0}{(\omega^2-\omega_0^2)^2+4d^2\omega_0^2} \\
A_p=\frac{(2.58^2-2^2)3.33}{(2.58^2-2^2)^2} \\
A_p =  1.25
$$

$$
B_p=\frac{-2d\omega_0a_0+(\omega^2-\omega_0^2)b_0}{(\omega^2-\omega_0^2)^2+4d^2\omega_0^2} \\
B_p =  0
$$

The particular solution is then

$$
\theta_p = A_p\sin(\omega_0t)+B_p\cos(\omega_0t) \\
\theta_p = 1.25\sin(2t)
$$

Hence

$$
\theta = A\sin(2.58 t) + B\cos(2.58 t) + 1.25\sin(2t)
$$

Then solve the differential with initial conditions provided

$$
t=0,\theta=0,\dot{\theta}=4
$$

$$
\theta =  A\sin(2.58 t) + B\cos(2.58 t) + 1.25\sin(2t) \\
0 = B
$$

$$
\dot{\theta} = 2.58A\cos(2.58t) - 2.58B\sin(2.58t) + 2.5\sin(2t) \\
4 = 2.58A+2.5 \\
A = 0.58
$$

$$
\therefore A = 0.58 \text{, } B=0
$$

Hence

$$
\theta = 0.58\sin(2.58t)+ 1.25\sin(2t)\\
$$

## Question 9

A team of engineering students build the simple seismograph shown. The coordinate $x_i$ measures the local horizontal ground motion. The coordinate x measures the position of the mass relative to the frame of the seismograph. The spring is unstretched when x=0. The mass is 1 kg, k=10 N/m, and c=2 Ns/m. Suppose that the seismograph is initially stationary and that at t=0 it is subjected to an oscillatory ground motion $x_i$=10sin(2t) mm. What is the amplitude of the steady-state response of the mass? 

<img src = "figs\08_vibrations_dampedforced\Q9.jpg" width="50%"> <br>

### Answer

Write the equation of motion using the information provided

$$
\ddot{x}+2\dot{x}+10x=F(t)
$$

To complete the equation, F(t) needs to be calculated. Given the initial displacement provided

$$
x = 10\sin(2t)\\
\frac{dx}{dt} = 20\cos(2t)\\
\frac{dx^2}{dt^2} = -40\sin(2t) =a(t)\\
$$

Which you will notice is the oscillatory forcing function. 

Given F=ma and m=1, the full equation is

$$
\ddot{x}+2\dot{x}+10x= -40\sin(2t)
$$

Calculating terms needed 

$$
\omega=\sqrt{\frac{k}{m}}=\sqrt{\frac{10}{1}}=\sqrt{10}\\
d=\frac{c}{2m}=\frac{2}{2(1)}=1\\
a(t)=a_0\sin(\omega_0t)+b_0\cos(\omega_0t)= -40\sin(2t)\\
\therefore a_0=-40, b_0=0, \omega_0=2
$$

From here, calculating the amplitude of the steady state response is simple 

$$
E_p = \frac{\sqrt{a_0^2+b_0^2}}{\sqrt{(\omega^2-\omega_0^2)^2+4d^2\omega_0^2}} \\
E_p = \frac{\sqrt{(-40)^2}}{\sqrt{(\sqrt{10}^2-2^2)^2+4(1)^2(2)^2}} \\
E_p=5.55 \text{ m}
$$

## Question 10

An electric motor is bolted to a metal table. When the motor is on, it causes the tabletop to vibrate horizontally. Assume that the legs of the table behave like linear springs, and neglect damping. The total weight of the motor and the tabletop is 667 N. When the motor is not turned on, the frequency of horizontal vibration of the tabletop and motor is 5 Hz. When the motor is running at 600 rpm, the amplitude of the horizontal vibration is 0.25 mm. What is the magnitude of the oscillatory force exerted on the table by the motor at its 600 rpm running speed?

<img src = "figs\08_vibrations_dampedforced\Q10.jpg" width="50%"> <br>

### Answer

The equation can be written 

$$
m\ddot{x}+c\dot{x}+kx=F(t)
$$

Then divide across by m

$$
\ddot{x}+\frac{c}{m}\dot{x}+\frac{k}{m}x=\frac{F(t)}{m} \\
\ddot{x}+2d\dot{x}+\omega^2x={a(t)}
$$

Where 

$$
d=0
$$
$$
\omega^2=(2\pi f)^2=(10\pi)^2=100\pi^2 \\
\therefore \omega = 31.42
$$ 
$$
a(t)=\frac{F(t)}{m}
$$

a(t) also takes the form $a_0\sin(\omega_0t)+b_0\cos(\omega_0t)$. Either sin or cos must disappear as the representation above has only one term but it does not matter which one you 'get rid of'. 

$$
a_0\sin(\omega_0t)=\frac{F(t)}{m}
$$

The forcing frequency is

$$
600\text{ rpm} =  10\text{ rps} = 10(2\pi) \text{ rad/s} \\
\therefore \omega_0=62.83
$$

The amplitude can be written as

$$ 
E_p = \frac{\sqrt{a_0^2+b_0^2}}{\sqrt{(\omega^2-\omega_0^2)^2+4d^2\omega_0^2}} \\
0.00025 = \frac{a_0}{(31.42^2-62.83^2)} \\
a_0=-0.74
$$

Finally calculate the magnitude of the force

$$
|0.74\sin(\omega_0t)|=\frac{F(t)}{667/9.81} \\
F(t)=50.3 \text{ N}
$$