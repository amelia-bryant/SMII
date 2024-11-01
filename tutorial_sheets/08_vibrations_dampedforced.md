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


# Tutorial Sheet 10: Vibrations, Damped and Forced

**Topics covered are:**
- Damped vibrations
- Forced vibrations
- Rotational vibrations

**Tips**
- Even though the equations are getting longer, as long as you  make sure you know what all the parameters are, you are familiar with the equations, and how to manipulate them, you shouldn't have too much of an issue.
- Instead of calculating all the variables, you can start to recognise them directly by inspection from the equations - this can be quicker, but make you more prone to mistakes.

<br>

## Question 1 

The mass m=2 kg, the spring constant is k=72 N/m, and the damping constant is c=8 Ns/m. The spring is unstretched when $x$=0. The mass is displaced to the position $x$=1 m and released from rest.

**(a)** What is the frequency of the resulting damped vibrations? <br>
**(b)** What is the value of $x$ at t=1 s?

<img src = "figs\08_vibrations_dampedforced\Q1.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ 0.9 \text{ Hz} $$

**(b)** 

$$ x=0.0816 \text{ m} $$


## Question 2

The mass m=2 kg, the spring constant is k=72 N/m, and the damping constant is c=32 Ns/m. The spring is unstretched when $x$=0. The mass is displaced to the position $x$=1 m and released from rest.

**(a)** What is the frequency of the resulting damped vibrations? <br>
**(b)** What is the value of $x$ at t=1 s?

<img src = "figs\08_vibrations_dampedforced\Q1.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ f_d = 0.084 \text{ Hz} $$

**(b)** 

$$ x=0.0837 \text{ m} $$


## Question 3

The mass m=2 kg, the spring constant is k=8 N/m, and the damping coefficient is c=12 Ns/m. The spring is unstretched when $x$=0. At t=0, the mass is released from rest with $x$=0. Determine the value of $x$ at t=2 s.

<img src = "figs\08_vibrations_dampedforced\Q3.jpg" width="50%"> <br>

### Answer

$$ x=0.624 \text{ m} $$


## Question 4

A 79.8 kg test car moving with velocity $v_0$=7.33 m/s collides with a rigid barrier at t=0. As a result of the behavior of its energy-absorbing bumper, the response of the car to the collision can be simulated by the damped spring-mass oscillator shown with k=8000 N/m and c=3000 Ns/m. Assume that the mass is moving to the left with velocity $v_0$=7.33 m/s and the spring is unstretched at t=0. Determine the car’s deceleration 

**(a)** Immediately after it contacts the barrier <br>

**(b)** At t=0.08 s.

<img src = "figs\08_vibrations_dampedforced\Q4.jpg" width="50%"> <br>

### Answer

**(a)** 

$$
275 \text{m/s}^2
$$

**(b)** 

$$
25.7 \text{m/s}^2
$$


## Question 5

The motion of a car’s suspension shown can be modeled as a damped spring–mass oscillator with m=36 kg, k=22 kN/m, and c=2.2 kNs/m. Assume that no external forces act on the tire and wheel. At t=0, the spring is unstretched and the tire and wheel are given a velocity $\frac{dx}{dt}$=10 m/s. Determine the position $x$ as a function of time.

<img src = "figs\08_vibrations_dampedforced\Q5.jpg" width="50%"> <br>

### Answer

$$
x=0.256e^{-12.6t}-0.272e^{-48.6t}+0.016
$$


## Question 6

The mass m=2 kg and the spring constant is k=72 N/m. The spring is unstretched when $x$=0. The mass is initially stationary with the spring unstretched, and at t=0 the force F(t)=10sin(4t) applied to the mass. What is the position of the mass at t=2s?

<img src = "figs\08_vibrations_dampedforced\Q6.jpg" width="50%"> <br>

### Answer

$$ 0.337 \text{ m} $$


## Question 7

The damped spring–mass oscillator is initially stationary with the spring unstretched. At t=0, a constant force F(t)=6 N is applied to the mass.

**(a)** What is the steady-state (particular) solution? <br>
**(b)** Determine the position of the mass as a function of time.
 
<img src = "figs\08_vibrations_dampedforced\Q7.jpg" width="50%"> <br>

### Answer

**(a)** 

$$ 0.5 $$

**(b)** 

$$
x=e^{-t}(-0.29\sin(\sqrt{3}t)-0.5\cos(\sqrt{3}t))+0.5
$$

## Question 8

The disk with moment of inertia I=3 kgm $^2$ rotates about a fixed shaft and is attached to a torsional spring with constant k=20 Nm/rad. At t=0, the angle $\theta$=0, the angular velocity is $\frac{d\theta}{dt}$=4 rad/s, and the disk is subjected to a couple M(t)=10sin(2t) Nm. Determine $\theta$ as a function of time.

<img src = "figs\08_vibrations_dampedforced\Q8.jpg" width="50%"> <br>

### Answer

$$
\theta = 0.58\sin(2.58t)+ 1.25\sin(2t)\\
$$

## Question 9

A team of engineering students build the simple seismograph shown. The coordinate $x_i$ measures the local horizontal ground motion. The coordinate $x$ measures the position of the mass relative to the frame of the seismograph. The spring is unstretched when $x$=0. The mass is 1 kg, k=10 N/m, and c=2 Ns/m. Suppose that the seismograph is initially stationary and that at t=0 it is subjected to an oscillatory ground motion $x_i$=10sin(2t) mm. What is the amplitude of the steady-state response of the mass? 

<img src = "figs\08_vibrations_dampedforced\Q9.jpg" width="50%"> <br>

### Answer
$$ 5.55 \text{ m} $$


## Question 10

An electric motor is bolted to a metal table. When the motor is on, it causes the tabletop to vibrate horizontally. Assume that the legs of the table behave like linear springs, and neglect damping. The total weight of the motor and the tabletop is 667 N. When the motor is not turned on, the frequency of horizontal vibration of the tabletop and motor is 5 Hz. When the motor is running at 600 rpm, the amplitude of the horizontal vibration is 0.25 mm. What is the magnitude of the oscillatory force exerted on the table by the motor at its 600 rpm running speed?

<img src = "figs\08_vibrations_dampedforced\Q10.jpg" width="50%"> <br>

### Answer

$$ 50.3 \text{ N} $$

<br><br>