# **Units & Basic Principles**

***McKay: Physics and Life***
- **The Spherical Cow:**
	- “Assume each cow is a sphere”
	- Use of basic mathematical models is incredibly useful in physics 
	- Surface area = volume$^\frac 2 3$
- **Convergent Evolution:**
	- Flight evolved so that animals could travel in air
	- Wings push down on air, and air pushes back up, overcoming the force of gravity
- **Diffusion:**
	- Diffusion: molecular transportation
	- Oxygen absorption depends on surface area, but oxygen needs depend on volume
	- Animals survive by changing their shape as they get larger (think lungs)
	- Insects absorb oxygen directly through diffusion, limiting their possible growth (thank GOD)

***McKay: Key formulas:***
![[Screenshot 2025-06-22 at 12.32.39 PM.png]]
![[Screenshot 2025-06-22 at 12.32.51 PM.png]]
![[Screenshot 2025-06-22 at 12.34.26 PM.png]]
![[Screenshot 2025-06-22 at 12.34.53 PM.png]]

***Schmidt-Nielsen: basic units***
- **Dimensions:**
	- Newtonian mechanics system
	- $M$ = mass
	- $L$ = length
	- $T$ = time
	- $ρ$ = density
	- $P$ = pressure difference
	- $r$ = radius
	- $η$ = viscosity
	- $l$ = length
	- Poiseuille’s equation:![[Screenshot 2025-06-23 at 1.09.29 PM.png]]![[Screenshot 2025-06-23 at 2.48.31 PM.png]]
- **Dimensionless qualities:** 
	- Ratios, strain, coefficient of fraction, Reynolds number
	- Mammals’ hearts are typically 0.6% of their body mass, and their blood is typically 0.5%

 ***Textbook: Notation:***
- **Significant figures:**
	- Whole numbers have at least two significant figures (even there are more than two trailing zeros)
	- When multiplying or subtracting numbers, the result should have as many significant figures as the smallest number
	- When adding or subtracting numbers, the result should have as many decimal places as the number with the least decimal places
	- Exact numbers have infinite significant figures
- **Scientific notation** has the significant figures of a number multiplied by a power of ten
- **SI (metric) units:**
	 - Time: seconds
	 - Length: meters
	 - Mass: kilograms
- **Unit conversions:**
  ![[Screenshot 2025-06-24 at 5.47.15 PM.png]]
- **Order-of-magnitude estimate:** approximate estimate with one significant figure


-------------------------------------------------------------------

# **Scaling**

***Lecture 1: Scaling:***
- **Allometric scaling:**
	- Shape and proportions change with size
	- Allometric relationships are expressed using **power laws**
		- $y = ax^b$
		- $y$ = item measured in relation to whole
		- $x$ = size of whole
		- $b$ determines the type of scaling relationship
			- **Positive allometry:** if $b > 1$ then $y$ increases faster than $x$
			- **Negative allometry:** if $b < 1$ then $x$ increases faster than $y$ 
			- **Isometry:** if $b = 1$ then $x$ and $y$ increase at the same rate
- **Combining scaling relationships:**
	- Homework on this section
	- **~** is the proportional operator
	- **Steps:**
		1. Identify relationship
		2. Find relationship between two quantities in terms of a common third quantity
		3. Take the quantity raised to $b$ and the common third quantity and solve the expression relating the two to the common quantity
		4. Plug the relationship from step 3 into the relationship in step 2
	- Example: 
		- $f = b^x$
		- $h = b^y$
		- We want: $f$ ~ $h^b$
		- Transform $h$ ~ $b^y$ to $h^y$ ~ $b$
		- Then $f$ ~ $b^x$ → $f$ ~ $b^\frac x y$
		- So $f/h$ ~ $b^\frac x y$
- **Important scaling relationships:**
	- Surface area ~ size$^2$
	- Volume ~ size$^3$
	- Mass ~ size$^3$
		- $Mass = density * volume$
		- So, mass ~ volume ~ size$^3$
	- Surface area/volume ~ size$^\frac 23$
	- Surface area/volume ~ 1/mass$^\frac 13$

***Schmidt-Nielsen: Scaling:***
- **Definition:** structural and functional consequences of changes in size or scale
- Three parameters that change when size is increased:
	- Dimensions
	- Materials
	- Design
- **Scale of animals:** 
	- Mass is the best measure of size
	- Diffusion (molecular transportation) only works efficiently over small distances
	- Convection (ventilation, circulation) is preferred in most animals
	- Respiratory pigments (hemoglobin)
	- Note: insects use diffusion
- **Isometric scaling:**
	- Things with the same proportions can be related with a **similarity ratio**
	- Isometry: geometric similarity of proportions
- **Allometric scaling:**
	- Physiological variables typically follow the equation $y = ax^b$ or $log (y) = log (a) + b (log (x))$
	- Two variables plotted on logarithmic coordinates form a straight line


-------------------------------------------------------------------

## **Modeling**

***Plotting functions:***
- $R^2$ measures how well a linear function fits the data
	- If $R^2 = 1$ then the line fits the data perfectly
- **Three main functions:**
	- Linear functions: $y = mx + b$
	- Power functions: $y = ax^b$
	- Exponential functions: $y = na^{ks}$
- **Steps of plotting data:**
	- First, find a relationship between $x$ and $y$
	- Choose an appropriate function
	- Identify constants for chosen function
- **Logarithms:**
	- If $a^c = b$ then $log_ab = c$
	- **Common rules:**
		- $log(m * n) = log(m) + log(n)$
		- $log(n^k) = k(log(n))$
		- $n^{log_nx} = x$
	- **Common logarithms:**
		- $ln = log_e$
		- $log = log_{10}$
		- $lg = log_2$
	- **Logging power functions:**
		1. $y = ax^b$
		2. $log(y) = log(ax^b)$
		3. $log(y) = log(x^b) + log(a)$
		4. $log(y) = b(log(x)) + log(a)$
		5. Then $y’ = m(x’) + d$
		6. **The plot of $log(y), log(x)$ is a straight line**
	- **Logging exponential functions:**
		1. $y = na^{kx}$
		2. $log(y) = log(na^{kx})$
		3. $log(y) = log(a^{kx}) + log(n)$
		4. $log(y) = kx(log(a)) + log(n)$
		5. Then $y’ = m(x’) + d$
		6. **The plot of the semi-log ($log(y), x$) is a straight line**

***Graphs:***
![[Screenshot 2025-06-24 at 9.44.08 AM.png]]


***Modeling:***
- **Descriptive models:** simple, applicational models of phenomenon
- **Explanatory models:** models that predict behavior based on experimental/observational data
- **Particle model:** considering a moving object as if it’s a single point (particle)
- **Position vs. time graph:** plot of an object’s position as a function of time
	- The slope is the object’s velocity at a given point

***Vectors:***
- **Scalar quantity:** physical quantity described by a single unit
	- Examples: temperature, mass, speed
	- Values can be either positive or negative
- **Vector quantity:** quantity that has both size (magnitude) and direction
	- Examples: position, velocity
	- Values can be either positive or negative
- **Vectors** are represented with **arrows:** $\vec{V}$
	- The direction of the arrow correlates with the direction of the vector
		- Arrow pointing left: negative vector
		- Arrow pointing right: positive vector
	- The length of the arrow correlates with the magnitude of the vector
- **Vector math:**
	- **Steps of vector addition:**
		1. Define which directions are $y$ and $x$
		2. Break each vector into its y- and x-components
		3. Add all x-components to find the total
		4. Add all y-components to find the total
		5. Find the total displacement of the vector using the Pythagorean theorem
	- Resultant vector: sum of two vectors
	- Multiplying a vector by a positive scalar changes the **magnitude** but not the direction
	- Multiplying a vector by a negative scalar changes the **magnitude** and the **direction**
	- Subtraction is complicated - the vector being subtracted must be flipped first 
- **Displacement vector:** vector representation of displacement
	- Drawn as a straight-line from initial position $x_i$ to final position $x_f$
	- Trigonometric functions can be used with vectors
- **Velocity vector:** vector representation of velocity
	- The direction of the arrow correlates with the direction of the vector
	- The length of the arrow correlates with the speed of the vector
	- Faster speed → steeper slope
- **Graphing vectors:**
	- Component vectors: parallel axes drawn from a given vector on a plane
		- X-component vector: projection of $\vec{A}$ along the x-axis
		- Y-component vector: projection of $\vec{A}$ along the y-axis
		- Component: scalar $A_x$ that describes a component vector $\vec{A}_x$ 
			- The absolute value of $A_x$ is the magnitude of $\vec{A}_x$ 
			- The sign of $A_x$ is positive if $\vec{A}_x$ points in the positive direction, and vice versa
			- $A_x = a(cos(θ))$ and $A_y = a(sin(θ))$ for hypotenuse $a$
		- If $\vec{D} = \vec{A} + \vec{B} + \vec{C}$ then component $D_x$ = $A_x$ + $B_x$ + $C_x$


-------------------------------------------------------------------

# **Motion & Kinematics**

***Kinematics:***
- **Kinematics:** description (not explanation) of motion
- **Kinematic variables:** position, velocity, speed
- **Steps for solving a kinematics problem:**
	1. Sketch graphs for $a_x$ and $a_y$ vs. time
	2. Find values for the x- and y-components of the initial velocity
	3. Sketch graphs of $v_x$ and $v_y$ vs. time
	4. Find values for horizontal and vertical displacement based on the component graphs
	5. Use a velocity or acceleration-based relationship to figure out the remaining variables:![[Screenshot 2025-06-27 at 9.40.41 AM.png]]
	6. Use the Pythagorean theorem to get the magnitude of acceleration, velocity, and displacement
- Or use the **kinematics equations:**![[Screenshot 2025-06-27 at 9.49.05 AM.png]]

***Motion:***
- **Motion:** change of an object’s position or orientation through time
	- **Position:** an object’s location with respect to the origin
	- **Trajectory:** path of object’s movement
	- **Displacement:** difference ($Δx$) between initial position $x_i$ and final position $x_f$
		- Equation: $Δx = x_f - x_i$
		- For time ($Δt$), the difference between $t_i$ and $t_f$ is always positive
		- Displacement is the integral of velocity
	- **Force:** cause
	- **Acceleration:** effect
	- Motion is independent of direction
- **Diagramming motion:**
	- Images of motion - i.e., frames of a video
	- If the distance between frames is **equal**, the object is moving at a **constant speed**
	- If the distance between the frames **increases**, the object is **accelerating** 
	- If the distance between the frames **decreases**, the object is **decelerating** 
- **Uniform motion:** motion at a constant speed
	- An object’s motion is uniform if its position graph is a straight line
	- Denoted by $y = Cx$ where $C$ is the proportionality constant
	- For uniform motion, acceleration is zero and velocity is constant
- **Oscillating system:** object that moves back and forth around an equilibrium position
	- Examples: pendulum, guitar strings

***Velocity & speed:***
- **Speed:** ratio of distance traveled to time elapsed
	- Speed is a scalar value
- **Velocity:** ratio of displacement to time elapsed
	- Velocity is a vector value 
	- Both an object’s speed and its direction are accounted for
	- **Sign** of velocity represents an object’s **direction**
- **Instantaneous velocity:** an object’s velocity at a specific time
	- Instantaneous velocity $v_x$ at time $t$ = slope of position graph at time $t$
	- Instantaneous velocity = slope of tangent line at given time
- **Speed vs. velocity:**![[Screenshot 2025-06-24 at 5.27.08 PM.png]]![[Screenshot 2025-06-24 at 5.27.48 PM.png]]

***Acceleration:***
- **Acceleration** ($a_x$) is the ratio of velocity to time
	- It is the **derivative** or **slope** of velocity
	- Represents the rate of change of velocity
- **Equations:**
	- **Basic acceleration definition:** $Δv/Δt$ or $(v_f - v_i)/Δt$
	- **Velocity equation for constant acceleration:** $v_f = v_i + a_x(Δt)$
	- **Position equation for constant acceleration:** $x_f = x_i + v_i(Δt) + (1/2)a_x(Δt)^2$
	- **Velocity + displacement for constant acceleration:** $v_f^2 = v_i^2 + 2a_x(Δx)$
- When an object is rising or falling, **its acceleration has a downward direction**
- **Graphing acceleration:**
	- If the velocity graph is **linear**, the acceleration is **constant**
	- When an object is **speeding up:**
		- Acceleration and velocity vectors point in the **same direction**
		- Acceleration and velocity have the **same** sign
	- When an object is **slowing down:**
		- Acceleration and velocity point in **opposite directions**
		- Acceleration and velocity have **opposite** signs
- **Finding velocity from acceleration:** multiply position by total time

***Free fall:***
- Free fall: motion that occurs under the force of **gravity**
- All objects in free fall have the **same acceleration** regardless of mass
- Falling objects have negative acceleration, so the **direction of free fall is always downward**
- **General equation for free fall acceleration:** $a_{free fall} = -g = -9.8 m/s^2$
	- $g$ = acceleration due to gravity
	- $g$ is the magnitude of free fall acceleration
	- One-dimensional acceleration: $a_y = -g$
- Also, $\vec{a}_{free fall} = \vec{a}_x + \vec{a}_y$
- **Acceleration along a frictionless slope**: $a_x = ± g(sin(θ))$

***Calculus for acceleration, velocity, & displacement:***
- **Derivation:**
	- Derivative of displacement → velocity
	- Derivative of velocity → acceleration
- **Integration:**
	- Integral of acceleration → velocity
	- Integral of velocity → displacement

***Two-dimensional motion:***
- In two dimensions:
	- An object’s **displacement** is a **vector**
	- **An object’s velocity vector** = $\vec{v} = \vec{d}/Δt = d/Δt$
	- **An object’s acceleration vector** = $\vec{a} = (\vec{v}_f - \vec{v}_i)/(t_f - t_i) = Δ\vec{v}/Δt$
	- The **acceleration vector**, **velocity vector**, and **displacement** point in the **same** direction
	- If the magnitude of $\vec{v}$ changes, the object’s speed has changed
	- If the direction of $\vec{v}$ changes, the object’s direction has changed

***Projectile motion:***
- **Projectile:** object that moves in two dimensions under the influence of gravity
- The **horizontal** and **vertical** components of an object in projectile motion are **independent**
	- The initial horizontal velocity does not affect the vertical motion, and vice versa
- **For all projectile motion:**
	- The vertical component of acceleration ($a_y$) is $g$
	- The horizontal component of acceleration $a_x$ is $0$
- **Launch angle:** angle of the initial velocity ($v_i$) above the x-axis
- The **speed** of the initial velocity ($v_i$) is **always positive**
- Projectile motion is made up of uniform horizontal motion at constant velocity and uniform vertical motion at constant velocity 
	- A ball thrown upward finishes its downward motion at the initial speed:![[Pasted image 20250626192553.png]]
- **Range of a projectile:**
	- Two variables that determine range: **initial speed** and **launch angle**


-------------------------------------------------------------------

# **Forces**

***Overview of force:***
- **Force:** push or pull between two objects that causes motion
	- One object exerts force, one object receives the force
- Forces are **vectors**
- **SI unit:** newtons (N)
- **Net (total) force:** vector sum of all the forces acting on that object
- Forces can be contact (tension) or non-contact (gravity)
- An object pulled with a constant force moves with a constant acceleration (second law)
- Force is proportional to acceleration
- Whenever multiple objects are moving together, the acceleration is the same

***Newton’s Laws:***
- **First Law:** if an object’s net force is 0 N, then the object’s velocity is constant
	- Special case of the second law: $\vec{F}_{net} = m(0) = 0$
- **Second Law:** if an object’s net force is not 0 N, then the object will accelerate as $\vec{F}_{net} = m\vec{a}$
	- **Component form:** $ΣF_x = ma_x$ or $ΣF_y = ma_y$
	- **Notation:**
		- $\vec{F}_{net}$ is the object’s net force
		- $m$ is the object’s mass
		- $\vec{a}$ is the object’s acceleration
	- Equation can be divided into the x- and y-components
	- $\vec{F}_{net}$ **and** $\vec{a}$ **point in the same direction**
	- If an object is slowing down, $\vec{F}_{net}$ **and** $\vec{v}$ **point in the opposite direction**
	- If an object is speeding up, $\vec{F}_{net}$ **and** $\vec{v}$ **point in the same direction**
- **Third Law:** if one object exerts a force on second object, then the second object exerts a force of equal magnitude (pointing in the opposite direction) on the first object
	- Forces always come in pairs: $F_{BA} = -F_{AB}$
	- Force pairs are always the same type of force
	- Cannot be present in the same free-body diagram
- **Steps for solving problems with Newton’s Laws:**
	1. Draw and label free-body diagrams
	2. Define a coordinate system
	3. Break all forces into their x- and y-components
	4. Apply Newton’s Second Law (or First Law) to the x-components
	5. Apply Newton’s Second Law (or First Law) to the y-components
	6. Solve for quantities of interest

***Types of force:***
- **Gravitational (Weight) Force:**
	- Non-contact force or long-range force
	- Always exerted by the earth on every object
	- Always points downward (towards the centre of the earth)
	- **Notation:**
		- Denoted with $W = mg$ 
			- $m$ = mass and $g = 9.8m/s^2$ = gravitational acceleration 
			- An object does not necessarily have an acceleration of $g$
		- Denoted with $\vec{W}_{EB}$ in free-body diagrams
			- $E$ = object exerting force
			- $B$ = object receiving force
- **Spring Force:**
	- Contact force
	- Springs can push or pull other objects
	- Denoted with $\vec{F}_{sp}$
- **Tension Force:**
	- Contact force
	- One object pulls on another object
	- Direction always points away from the object being pulled
	- Denoted with $T$
- **Normal Force:**
	- Contact force
	- Exerted by the surface that an object rests on
	- Force is exerted perpendicular to the contact surface
	- Normal refers to the direction of the force
	- Denoted with $N$
	- Normal force on an incline: ![[Pasted image 20250701141838.png]]
- **Friction Force:**
	- Contact force
	- Exerted by the surface over which an object moves
	- Always parallel to the surface 
	- Friction depends on the magnitude of the normal force
	- Denoted with $f$
	- **Types of friction:**
		- **Kinetic friction:** force that exists when an object slides across a surface
			- Direction is opposite motion
			- Magnitude = $μ_k(N)$
			- $μ_k$ is the kinetic coefficient
			- Denoted with $\vec{f}_{k}$
		- **Static friction:** force that prevents motion between an object and a surface
			- Direction is typically opposite motion
			- Occurs in response to an applied force
			- Since the object is not moving, the net force is always 0
			- Magnitude ≤ $μ_s(N)$
			- $μ_s$ is the static coefficient
			- Denoted with $\vec{f}_{s}$
		- **Rolling friction:** force experienced by a moving object in contact with a surface
			- Direction is opposite motion
			- The part of the object touching the surface is stationary
			- Magnitude ≤ $μ_r(N)$
			- $μ_r$ is the static coefficient
			- Denoted with $\vec{f}_{r}$
- **Drag:**
	- Resistive force: a force that opposes motion
	- Example: force of fluid on an object in motion
	- Points opposite the direction of motion
	- Denoted with $\vec{D}$
- **Thrust:**
	- Contact force
	- Force opposite the direction in which gas is expelled
	- Denoted with $\vec{F}_{thrust}$

***Free-body diagram:***
- Representation of all the forces acting on a single object
- Always includes:
	- A representation of the object
	- The forces acting on that object
- Never includes:
	- Forces exerted by that object on other object
	- Representations of the objects that exert forces on the main object
- Friction is only included when a) the object is in motion or b) another object is trying to push it into motion

***Numerical integration:***
- Approximating the area under the curve using rectangles (Riemann sum)
- Area of each rectangle = average acceleration * $Δt$
- Area under the curve = total area of all rectangles


-------------------------------------------------------------------

# **Impulse & Momentum**

***Overview:***
- Collision: short-duration interaction between two objects
	- Inelastic collisions: collisions where two objects stick together and move with a common final velocity
- Impulsive force: large force exerted during a short period of time
	- Effect of an impulsive force is proportional to the area under the force-time curve
	- Denoted as $\vec{J} = \vec{F}_{avg}(Δt)$
	- $F_{avg}$ is defined as the constant force that has the same area under the force-time curve as the real curve
- Average force needed to stop an object is inversely proportional to the duration of the collision 
- System of objects: objects that move together?
	- Internal forces: forces that act between objects in the system
	- External forces: forces that come from agents outside the system

***Impulse-Momentum Theorem:***
- Momentum: product of an object’s mass and velocity
	- Denoted as $\vec{p}$
	- Equations for momentum: 
		- $\vec{F}_{avg}(Δt) = m\vec{v}_f - m\vec{v}_i$
		- $\vec{p} = m\vec{v}$
		- $\vec{F}_{net} = m\vec{a} - m(\frac{Δ\vec{v}}{Δt})$
		- $\vec{F}_{net} = m(\frac{d\vec{p}}{dt})$
	- Total momentum ($\vec{P}$) is the vector sum of the momentum of each object
- Impulse-momentum theorem: $\vec{j} = \vec{p}_f - \vec{p}_i = Δ\vec{p}$
	- An impulse delivered to an object causes the object’s momentum to change
	- So $\vec{p}_f = \vec{p}_i + \vec{j}$

***Law of Conservation of Momentum:***
- The total momentum of a system affected by only internal forces is conserved (i.e., it does not change)
- If $\vec{F}_{net} = 0$, the total momentum of a system does not change
- Law of conservation: $\vec{p}_f = \vec{p}_i$
	- Total initial momentum equals the total final momentum

***Key equations:***
- **Momentum:** $\vec{p} = m\vec{v}$
- **Momentum… also:** $\vec{F}_{avg}(Δt) = m\vec{v}_f - m\vec{v}_i$
- **Impulse:** $\vec{J} = \vec{F}_{avg}(Δt)$
- **Impulse-momentum:** $\vec{J} = Δ\vec{p}$


-------------------------------------------------------------------

# **Springs, Stress, Strain, & Stretch**

***Spring Force:***
- Denoted with $\vec{F}_{sp}$
- Contact force
- **Spring force replaces normal force**
- **Movement:**
	- Springs can push or pull other objects
	- Stretch or compression of the spring is possible
	- When a spring is relaxed, it is at equilibrium 
- **Displacement:** 
	- Displacement = distance $Δl$
	- Spring force is given by **Hooke’s Law:** $S = -kΔl$
		- $k$, the spring constant, corresponds to the slope on the spring force graph
		- Stretch occurs away from equilibrium (hence the negative)
		- Hooke’s Law only applies for certain materials over a certain range of displacement (the linear region, not the elastic region)

***Stretch:***
- Pliant materials: materials that experience intense deformations from small forces
- Rigid materials: materials that experience small deformations from large forces
- Stretch of an object is given by **Young’s modulus**: $Y = \frac{stress}{strain}$
	- Two objects of the **same material** experiencing the same forces will always have the **same** Young’s modulus
- Restoring force: $F = \frac{YA}L(ΔL)$

***Stress & Strain:***
- **Strain relates to strain as follows** $F/A_0 = Y(Δl/l_0)$
	- Stress = $F/A$ = force over area (force applied on an object over its original surface area)
	- Strain = $ln(Δl/l_0 + 1)$ = material’s change in length over its original length
	- $Y = \frac{stress}{strain}$
- **Engineering stress and strain:**
	- Engineering stress: $F/A_0$ (force applied on an object over its original surface area) 
		- Units: $N/m^2$
	- Engineering strain: $Δl/l_0$ (material’s change in length over its original length)
		- No units - it is a pure value
- **True stress and strain:**
	- True stress: $F/A$ (force applied on an object over its current surface area)
	- True strain: $ln(Δl/l_0 + 1)$ (material’s change in length over its original length)
- Slope of the linear region of a stress-strain curve is Young’s modulus ($k = \frac{YA}L$)
- **Tensile strength:** largest stress a material can endure (what I’m under right now)
	- Given by $\frac{F_{max}}A$
	- A material with a large tensile strength can sustain large forces without breaking
	- A material with a large strain on its tensile strength can stretch to large lengths away from equilibrium


-------------------------------------------------------------------

# **Torque**

***Torque:***
- **Torque is the ability of a force to rotate an object**
	- Denoted as 𝜏
	- Vector product: $\vec{𝜏} = \vec{r}\vec{F_⊥}$
	- Magnitude: $|\vec{𝜏}| = |\vec{r}||\vec{F_⊥}|sin(θ)$
		- $θ$ is the angle between $\vec{r}$ and $\vec{F}$
	- Units: Nm
	- Torque is in 3D
- **Torque** depends on three factors:
	- The magnitude of the force causing the rotation
	- The distance from the pivot to the point at which force is applied
		- Pivot point: 
		- **Torque at the pivot point is always 0**
	- The angle at which the force is applied
- **Directions of torque:**
	- Torque is **positive** if the force on the object is **counterclockwise**
	- Torque is **negative** if the force on the object is **clockwise**
- **Line of action:** line from the point where force is applied
- **Moment arm:** perpendicular line from the line of action to the pivot
- **Net torque** = sum of all torque exerted by all forces
- An object in **static equilibrium** does not necessarily have a net torque of 0
	- However if net torque is 0, then the net force is also 0
	- For an object in equilibrium, the torque at every point is 0

***Solving torque problems:***
1. Draw an extended free-body diagram showing the forces
2. Choose a pivot point
3. For static equilibrium, net torque and net force are both 0
4. Use these equations to solve for torque and force

***Center of mass:***
- **Center of mass:**
	- Property of an object 
	- Does not change unless the distribution of mass changes
	- Located on a line of symmetry at the physical balance point
- Weight force of an object acts at that object’s center of mass


-------------------------------------------------------------------

# **Work & Energy**

***Energy:***
- Energy cannot be created nor destroyed
- Total energy, the sum of all the energies present in a system, is denoted as $E$
- When objects move, one kind of energy can be transformed into another
- Units of energy: joules (Nm)

***Potential energy:***
- Potential energy is energy stored for later transfer or transformation
- **Rules of potential energy:**
	- Potential energy depends on the **position** of an object
	- Only **changes** in potential energy are significant
	- Potential energy can only be defined when force is internal and conservative
- Potential energy of a conservative force is the negative work done by that force: $ΔU_F = -W_F$
- Relating potential energy to conservative forces:
	- System must be defined
		- **Example system definition:** 
			- System A: box 
				- $ΔU = 0, W_{net} = W_s, Δk$
				- $W_s = Δk$
			- System B: box and spring
				- $ΔU = U_s, W_{net} = 0, Δk$
				- $0 = Δk + ΔU_s$

***Types of energy:***
- **Kinetic energy:**
	- Denoted as $K$
	- Energy of motion
	- The heavier and faster an object is, the more kinetic energy it is
	- Kinetic energy is **never negative**
	- Kinetic energy can be related to work: $W = ΔK = K_f - K_i$
	- Kinetic energy can also be related to kinematics: $K = \frac{1}2mv^2$
	- **Types of kinetic energy:**
		- Translational kinetic energy: energy of an object moving in a straight line
		- Rotational kinetic energy: energy of an object rotating on a fixed axis
- **Gravitational energy:**
	- Denoted as $U_g$
	- Potential energy
	- Associated with an object’s height above the ground
	- As an object descends, the energy is converted into kinetic energy
	- Related to work as $U_{gf} = U_{gi} + mgΔy$ where $W = mgΔy$
	- Gravitational potential energy of an object: $U_g = mgy$
- **Elastic energy:**
	- Denoted as $U_s$
	- Potential energy
	- Associated with the stretch of an object
	- Related to work as $ΔU_s = W$
	- Elastic potential energy of a spring at a distance $x$ from equilibrium: $U_s = \frac{1}2kx^2$
- **Thermal energy:**
	- Denoted as $E_{th}$
	- Change in thermal energy vs. friction: $ΔE_{th} = f_kΔx$
	- Related to kinetic energy
		- Sum of kinetic and potential energies of the object’s molecules
- **Chemical energy:**
	- Denoted as $E_{chem}$
	- Associated with chemical bonds

***Energy transformations:***
- Transformations of energy within a system
- Examples:
	- $E_{chem} → U_g$
	- $K → E_{th}$
	- $E_{chem} → E_{th}$
	- $U_s → K → U_g$

***Energy transfers:***
- **Energy transfers:** exchange of energy between system and environment 
	- **Types of energy transfers:**
		- **Work:** mechanical transfer of energy due to a force that pushes or pulls on a system 
			- Work is a **scalar quantity**
			- Work occurs when a force is applied on an object over a distance
			- Work is only done by a force **outside** of the system
		- **Heat:** non-mechanical transfer of energy due to differences in temperature between a system and its surroundings
- **Net work:**
	- Net work is the sum of the work done by the forces acting on a system
	- Net work is relative to net force: $W_{net} = F_{net}dcos(θ)$
- **Work and energy equation:** $W = ΔE = E_f - E_i$
	- Work done on a system = the changes of total energy in the system
	- Vice versa, total energy of a system changes based on the amount of work done on it
	- The larger the displacement or force on a system, the more work is done 
		- **So** $W = F_∥d = Fdcos(θ)$ where $θ$ is the angle between force and displacement
			- Sign of $W$ is determined by $cos(θ)$ since force and displacement are always positive
			- If force and displacement point in opposite directions, the work will be negative
			- If force and displacement point in the same direction, the work will be positive
			- Without displacement, there is no work done
			- Forces perpendicular to displacement exert no work
			- If the part of the object that experiences force does not experience displacement, there is no work done
	- Units of work: joules (Nm)
- **Work per system equation:**  $W_{net} = Δk + ΔU$
- **Law of conservation of energy:** $ΔE = 0$
	- The total energy of an isolated system (where no energy transfers occur) is conserved

***Conservative forces:***
- A force is **conservative** if the work done by the force is **reversible**
- **Examples:**
	- Spring force is conservative because it can do positive and negative work 
		- Associated with spring potential energy: $U_s = 1/2 kx^2$
	- Gravitational weight is also conservative because it can do positive and negative work 
		- Associated with gravitational potential energy: $U_g = mgy$ for height $y$

***Gait:***
- **Gait:** pattern of limb movement during locomotion
- Humans have two primary gaits:
	- **Walking:** at least one foot is on the ground at all times
		- For anyone walking at their maximum speed, **Froude = 0.5**
	- **Running:** both feet are sometimes off the ground
- **Examples:** transverse gallop, rotary gallop, half bond
- **Froude:** $\frac{K}U_g = \frac{\frac{1}2mv^2}{mgy} = \frac{v^2}{gy}$
	- Froude’s number is unitless

***Resilience:***
- **Resilience** = work done by ($W_{by}$) the material as it relaxes **divided by** work done on ($W_{on}$) the material as it is stretched or compressed
	- In other words, **resilience** is the energy returned by the material **divided by** the energy put into the material
	- Generally, $W_{on} = -W_{by}$
- **Resilience is always ≤ 1**
- **Examples:**
	- A material that returns to its original position has a larger numerator and is more resilient
	- A material that is permanently deformed has a larger denominator and is less resilient
	- A larger resilience means that less elastic potential energy is converted into thermal energy 
- **Graphs:**
	- In a **force** vs. **displacement** graph, **resilience** = the area under the unloading curve **divided by** the area under the loading curve

***Potential energy curves:***
- The **distance** from the **potential energy curve** to the **energy line** is the object’s **kinetic energy**
- The object **cannot** be at a position where the **potential energy curve** is **above** the **energy line**
- When the **energy line** and the **potential energy curve cross**, the object’s **direction reverses**
- Any local **minimum** in the potential energy curve represents **stable equilibrium** 
- Any local **maximum** in the potential energy curve represents **unstable equilibrium** 


-------------------------------------------------------------------

# **Summary of Dynamics**

***Solving energy problems:***
1. Draw a picture and coordinate system
2. Define the system
3. Apply the work-energy theorem 
4. Define initial and final states
5. Identify work and energy terms that equal 0 
6. Solve for desired variables

***Solving dynamics problems:***
- If a question asks about force and **acceleration**, use **Newton’s laws**
- If a question asks about a force applied over a **cross-sectional area** or a **change in length**, use **stress and strain**
- If a question refers to **where force is applied on an object**, or the **perpendicular** component to force, use **torque**
- If a question refers to the **time over which a force is applied**, use **impulse and momentum** 
- If a question refers to the **distance over which a force is applied**, the **parallel** component to force, or the **velocity**, use **work and energy**


-------------------------------------------------------------------

# **Thermodynamics**

***First Law of Thermodynamics:***
- For systems in which only the thermal energy changes, the change in thermal energy equals the energy transferred from the system as work and/or heat:
	- $ΔE_{th} = W + Q$
		- Adiabatic processes: $Q = 0$ 
	- **Net work** from external forces done on the gas = the **area under the $pV$ curve**
		- The work will be **positive** when the gas is **compressed** (volume gets smaller)
		- The work will be **negative** when the gas expands (**volume** gets larger)
		- **Reading $pV$ curves - see $pV$ under *Gasses:** ![[Screenshot 2025-07-23 at 9.51.59 AM.png]]

***Chemical energy:***
- **Chemical energy:** potential energy associated with the interactions between the atoms and kinetic energy of electrons within the atoms
- **Negative forces** are **attractive forces**
- **Positive forces** are **repulsive forces**
- **Photodissociation:** breaking of molecular bonds through light absorption 
- **Bond energy:** minimum energy required to break a bond
- **Chemical energy equation**, for $N$ reactions performed: $ΔE_{chem} = NΔE_{reaction}$
- **In a potential energy graph for atoms**, the closer the bond is to the y-axis, the closer the atoms are to each other:
	- Bond length exists where the energy is 0

***Matter:***
- **Three states of matter: liquid, gas, solid**
	- **Gas:** particles are in random motion
	- **Liquid:** particles are weakly bonded
	- **Solid:** particles are tightly bonded
- **Atomic mass number:** $A=$ number of protons $+$ number of neutrons
- **Moles:** $1$ mole of a substance $= N_A = 6.022 * 10^{23}$ particles
	- Particles can be **monatomic** or **diatomic**
	- Number of moles in a substance with $N$ particles $= \frac{N}{N_A}$

***Gasses:***
- **Ideal gas model:** model of a gas where no energy is lost during collisions between particles
	- Speed of an atom in an ideal gas: $v_{rms} = \sqrt{\frac{3k_BT}m}$
- **Ideal gas law:** $pV = nRT$ for:
	- $p =$ **pressure** ($Pa$ or $N/m^2$)
	- $V =$ **volume** ($m^3$)
	- $n =$ **number of particles** 
	- $R = N_Ak_B = 8.31$
	- $T =$ **temperature** ($K$)
- For **ideal gas processes**, the ideal gas law is a **constant**
- **Changes in an ideal gas** are represented in $pV$ **diagrams**:
	- Each point represents a different state of the gas
	- Changes are represented by the trajectories between points

***Thermal stuff:***
- **Heat:** the transfer of energy in a system due to a temperature difference between the system and the environment
- **Volume thermal expansion:** $ΔV = βV_iΔT$ for $β=$ coefficient of volume expansion
- **Linear thermal expansion:** $ΔV = αL_iΔT$ for $α =$ coefficient of linear expansion 
- **Specific heat:** amount of heat that raises $1 kg$ of a substance by $1 K$
	- $Q = McΔT$
- **Phase transitions:** change in thermal energy but not in temperature
	- **Condensation point:** gas → liquid
	- **Boiling point:** liquid → gas
	- **Freezing point:** liquid → solid
	- **Melting point:** solid → liquid
	- A system at the melting point is in **phase equilibrium** 
- **Heat of transformation:** amount of heat energy that causes 1kg to undergo a phase change
	- Heat $L$ required for an entire system of mass $M$ to undergo a phase change: $Q = ML$
- **Thermal energy:**
	- **Thermal energy** is the sum of kinetic and potential energies of the object’s molecules
- **Energy & temperature:**
	- **Higher temperature** means **higher kinetic energy**, since atoms move faster in a hot object
	- Higher temperature also means higher potential energy 
	- Temperature is the **average** energy of the atoms in a system
	- **Kelvin:** 0º corresponds to the point where the kinetic energy of the system’s atoms is 0 
	- Relationship between **temperature** and **kinetic energy:** $T = \frac{2K}{3k_B}$ for $k_B = 1.38 * 10^{-23}$
		- $v_{rms} = \sqrt{\frac{3RT}{M_{mol}}}$
	- Relationship between **temperature** and **thermal energy:** $ΔE_{th} = \frac32(Nk_BΔT)$
	- **Energy reservoirs:** environments whose temperatures do not change if heat is transferred between the environment and a system 

***Diffusion:***
- **Diffusion:** net movement of particles from more concentrated areas to less concentrated areas
	- **Brownian motion:** random walk performed by particles during diffusionx
		- After starting at the origin, there is an equal probability of going in any given direction
		- Changes in directions occur with each collision
	- **Distance** of movement is generally defined by $r = \sqrt{(r^2)_{avg}}$
	- For **3D movement**, distance is defined by $r = \sqrt{6Dt}$ for the diffusion constant $D = \frac{1}2v_{rms}d_{mfp}$
		- This is based on $x _{rms}= \sqrt{Ld_{mfp}}$ 
	- Time to move a distance $L$ is defined by $t = \frac{L^2}{6D}$
	- **Fick’s Law:** for $N$ molecules occupying volume $V$, their concentration is $c = \frac{N}V$
		- Rate of molecule transfer: $\frac{N}Δt = (\frac{DA}L)Δc$


-------------------------------------------------------------------

# **Final Exam**

***Exam layout:***
- 13-14 multiple choice and 5-6 open response
- 4 multiple choice & 1 open response from this week


-------------------------------------------------------------------

# **Key equations**

***Displacement:*** 
- **Total displacement:** $Δx = x_f - x_i$

***Acceleration:***
- **Definition:** $Δv/Δt$ or $(v_f - v_i)/Δt$
- **Solving for velocity with time:** $v_f = v_i + a_x(Δt)$
- **Solving for velocity with x:** $v_f^2 = v_i^2 + 2a_x(Δx)$
- **Solving for x:** $x_f = x_i + v_i(Δt) + (1/2)a_x(Δt)^2$
- **Free fall:** $\vec{a}_{free fall} = \vec{a}_x + \vec{a}_y$
- **Free fall slope:** $a_x = ± gsin(θ)$

***Newton’s Laws:***
- **First Law:** $\vec{F}_{net} = m(0) = 0$
- **Second Law:** $\vec{F}_{net} = m\vec{a}$
- **Third Law:** $F_{BA} = -F_{AB}$

***Impulse & Momentum***
- **Impulse:** $\vec{J} = \vec{F}_{avg}(Δt)$
- **Momentum:** $\vec{p} = m\vec{v}$
- **Momentum… also:** $\vec{F}_{avg}(Δt) = m\vec{v}_f - m\vec{v}_i$
- **Impulse-momentum:** $\vec{J} = Δ\vec{p}$

***Stress & Strain:***
- **Hooke’s Law for spring force:** $S = -kΔl$
- **Young’s modulus**: $Y = \frac{stress}{strain}$
- **Strain relates to strain as** $F/A_0 = Y(Δl/l_0)$ **where:**
	- Stress = $F/A$
	- Strain = $ln(Δl/l_0 + 1)$

***Torque:***
- **Torque of a force:** $\vec{𝜏} = \vec{r}\vec{F_⊥}sin(θ)$

***Energy & Work:***
- **Law of conservation of energy:** $ΔE = 0$
- **Kinetic:**
	- **Kinetic energy vs. work:** $W = ΔK = K_f - K_i$
	- **Kinetic energy vs. kinematics:** $K = \frac{1}2mv^2$
- **Gravitational:**
	- **Gravitational energy vs. work:** $U_{gf} = U_{gi} + mgΔy$ where $W = mgΔy$
	- **Gravitational potential energy:** $U_g = mgy$
- **Elastic:**
	- **Elastic energy vs. work***: $ΔU_s = W$
	- **Elastic potential energy of a spring:** $U_s = \frac{1}2kx^2$
- **General work:**
	- **Work vs. energy:** $ΔE = W$
	- **Work vs. force:** $W = Fd$ and $W = F_∥d = Fdcos(θ)$
	- **Work vs. velocity:** $W_{net} = \frac{1}2mv_f^2 - \frac{1}2mv_i^2$
	- **Pre- and post-work equation:** $K_f + U_f + ΔE_{th} = K_i + U_i + W$
	- **Work per system equation:**  $W_{net} = ΔK + ΔU$
- **Change in thermal energy vs. friction:** $ΔE_{th} = f_kΔx$
- **Froude:** $\frac{K}{U_g} = \frac{\frac{1}2mv^2}{mgy} ~ \frac{v^2}{gy}$


-------------------------------------------------------------------

# **Diagrams**

***Gas laws:***

![[Pasted image 20250722173311.png]]


***Energy diagrams:***

![[Pasted image 20250722170530.png]]


***Collisions transfer energy from faster molecules to slower molecules:*** 
 
 ![[Pasted image 20250722122315 1.png]]


***Reaction coordinate graph:*** 
For the bonds to break, energy must rise to $E_a$, the **activation energy**

![[Pasted image 20250722093114 1.png]]
![[Pasted image 20250722094146 1.png]]![[Pasted image 20250722094358 1.png]]


***Potential energy curves:***

![[Screenshot 2025-07-18 at 11.26.31 AM.png]]
![[Screenshot 2025-07-18 at 11.26.58 AM.png]]
