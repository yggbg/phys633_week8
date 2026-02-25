# Week 6 Exercises


## Part 1: Chaos

In this part of the exercise, we are going to investigate the obrbit of a zero-mass particle in a Sun-Jupiter system. You may follow the exercise in [Week 03 exercise](https://andrewcumming.github.io/phys633/week3-exercise/). Here we approximate the mass of Jupiter to be $\mu_2 = \mathcal{G}M = 10^{-3}$, so that the semi-major axis of Jupiter orbit is $a =1$. While Jupiter's orbit is known to be slightly eccentric, here we assume $e=0$.

**Note:** In the following notations, $x$, $y$, $\dot{x}$, and $\dot{y}$ are quantities in the rotating frame of Sun-JUpiter system. **REBOUND** takes intital conditions in initial frame. Use *Murray* Eqn. (3.10) & Eqn. (3.11) to transform. And if you wan to transform back to rotating frame, which you will need in egenerating surface section plot, consult with Eqn.(3.30) & Eqn.(3.31). As you can see in (1), initial conditions matters to the orbital evolution.

**Hint:** In **REBOUND**, `sim.move_to_com()` function allow you to move to the centre of mass frame. **After defining** the Sun-Jupiter system and **before** defining the particles, using this function makes the analysis easier.

1) Orbits are sensitive to initial conditions. Now place 2 particles with the same semi-major axis ($a_0 = 0.8$), eccentricity ($e_0 = 0.4$) and longitude of pericentre ($\bar{\omega} = 295^\circ$) but with slightly different initial mean longitudes ($\theta = 293^\circ$ and $\theta = 293.5^\circ$). Run the simulation for 1 period of Jupiter's orbit. Can you see the deviation?

2) Set 2 particles with different locations $x_0 = 0.55$ and $x_0 = 0.56$. Both with $y0 = 0$ and $\dot{x_0} = 0$, with $\dot{y} > 0$ determined from the solution of *Murray & Dermott* Eq. (9.5) with CJ = 3.07. Run simulation for long time (~300 Jupiter orbits). Can you spot the difference between a regular orbit and a chaotic orbit? Plot $a$ and $e$ with time. Compare the result with Fig. 9.4 and 9.6 in *Murray*. 

3) Once you manage to find a regular orbit and a chaotic orbit, now place 1 more particle at each initial location with tiny separation ($\Delta x_0 \sim 10^{-5}$) from the particle already there. Plot $a$ of the 2 particles at the same location, after how many orbit periods can you see the divergence? 

4) Plot the maximum Lyapounov characteristic exponent $\gamma$ where
$$
d_i = d_0 \exp~\gamma(t_i - t_0)
$$
in which $d_i$ is the seperation in phase space at time $t_i$. Can you see the difference between a regular orbit and a chaotic orbit?

5) Plot the surface of section for the trajectory of all 4 particles whenever $y = 0$ with $\dot{y} > 0$. Compare to the plot as shown in *Murray* Fig. 9.5 and Fig. 9.7. Is the shape as expected as being close to a resonance orbit?

6) Investigate the relation between the number of "islands" displayed in the surface section plot and resonance ratio. 

7) Choose a different orbital resonance ratio from Fig. 9.16 for each group and run the simulations. Plot the surface section as in (5). Upload your $x$, $\dot{x}$ [here](https://docs.google.com/spreadsheets/d/15RUfNkGNQk1gt9__fYm0785cu7k5rjrya2pjnki3jEY/edit?usp=sharing). Let's make a big plot togather! (**Hint:** Remember that the surface section plot gives you position and velocity in rotaing frame! Look into the graph to find your initial $x_0$ and $y_0$.)

