# Twin Paradox and Proper Time Along Curves - Problems and Solutions

## Problem 1

Explain the twin paradox.

### Solution 1

The twin paradox is a thought experiment in special relativity, in which a twin makes a journey into space in a high-speed rocket and returns home to find that the twin who remained on Earth has aged more. 

This result appears puzzling because each twin sees the other twin as moving, and so, it is argued, each should paradoxically find the other to have aged more slowly. However, the situation is not symmetric, as the traveling twin has undergone acceleration, which takes them out of the class of inertial observers.

The key insight is that the traveling twin experiences acceleration during:

1. The departure phase (accelerating away from Earth)
2. The turnaround phase (decelerating and then accelerating back toward Earth)  
3. The arrival phase (decelerating to land on Earth)

During these acceleration phases, the traveling twin is not in an inertial reference frame, which breaks the symmetry of the problem.

## Problem 2

Calculate the proper time for a uniformly accelerated observer.

### Solution 2

The proper time is given by:
$$d\tau = \sqrt{-ds^2/c^2}$$

For a uniformly accelerated observer, the line element in their rest frame is:
$$ds^2 = -c^2 d\tau^2$$

Therefore:
$$d\tau = \frac{\sqrt{-ds^2}}{c}$$

The proper time is simply the time measured by the observer's own clock. For any worldline parameterized by coordinate time $t$, the proper time is:
$$\tau = \int \sqrt{1 - \frac{v^2(t)}{c^2}} \, dt$$

where $v(t)$ is the coordinate velocity as a function of coordinate time.

## Problem 3

A spaceship travels to a star 10 light-years away at a speed of 0.8c and returns to Earth. How much time has passed on Earth and on the spaceship?

### Solution 3

**Time on Earth:**
The total distance is $2 \times 10 = 20$ light-years.
At speed $v = 0.8c$:
$$\Delta t_{\text{Earth}} = \frac{20 \text{ ly}}{0.8c} = 25 \text{ years}$$

**Time on Spaceship:**
The Lorentz factor is:
$$\gamma = \frac{1}{\sqrt{1 - v^2/c^2}} = \frac{1}{\sqrt{1 - 0.8^2}} = \frac{1}{\sqrt{1 - 0.64}} = \frac{1}{\sqrt{0.36}} = \frac{1}{0.6} = \frac{5}{3}$$

The proper time (time on spaceship) is:
$$\Delta \tau = \frac{\Delta t_{\text{Earth}}}{\gamma} = \frac{25 \text{ years}}{5/3} = 25 \times \frac{3}{5} = 15 \text{ years}$$

Therefore, 25 years pass on Earth while only 15 years pass on the spaceship. The traveling twin is 10 years younger than the Earth-bound twin when they return.