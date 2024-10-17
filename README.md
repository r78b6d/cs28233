java c
MATHS 3023/4123/7107 Partial Differential Equations  Waves
Written Assignment 4
Due: 5.00 pm Monday 14 October
When presenting your solutions to the assignment, please include some explanation in words to accompany your calculations. It is not necessary to write a lengthy description, just a few sen- tences to link the steps in your calculation. Messy, illegible or inadequately explained solutions may be penalised. The marks awarded for each part are indicated in boxes.
This assignment has 2 question(s), for a total of 30 marks.
1.  Recall that the Earth’s surface is divided into tectonic plates.  These plates move slowly (a few centimetres per year) to cause earthquakes, and form. mountains and ocean trenches. The moving plates reflect convective motion in the Earth’s mantle of hot liquid rock between the core and the surface. Chapman and Proctor (1980) created a pde model of the motion in the liquid rock that encapsulates key physical processes.  The model is written in terms of a temperature gradient u(x,t) = θx, restricted to one lateral space dimension.  The (scaled) governing pde is

for non-dimensional parameter r characterising the rate of heat flowing through the mantle layer from the Earth’s core to the surface.  In this assignment, we explore solutions of this pde when solved subject to boundary conditionsu(0, t) = u(L,t) = uxx(0, t) = uxx(L,t) = 0.                                  (2)5           (a)  Use second-order centred finite-difference approximations to create a spatial discretisa-tion of the nonlinear pde (1).  Check your discretisation using taylor() in Matlab. What terms in your taylor() output confirm a consistent discretisation? What is the leading error of the equivalent pde for your discretisation?Hint:  For such a fourth order pde it is usually easiest to code the fourth derivative as two second-order derivatives. That is, introduce a field v(x,t) defined to be v := uxx , so that uxxxx  = vxx.  In Matlab’s algebra you would additionally define  syms  v(x), set v(x)=   ...   a discrete approximation to uxx, and then use taylor() to report on a discrete approximation to vxx  in terms of v(x),v(x+h),v(x−h).
•  Check each of the three terms separately.
•  simplify() and collect( ... ,  h) help to simplify and organise the output.
• List your Matlab code and its output.7          (b)  Write a Matlab script. that uses the finite-difference formulae from part (a) to simulatethe pde (1) subject to bcs (2) on a spatial domain of length L = 2π for 0 ≤ t ≤ 10
and r = 1.5. Use random initial conditions uj (0) ∈ [−1, 1] and n = 30 grid points.
Run your code many times and observe that a smooth pattern emerges after time t ≈ 1. Notice that this pattern sometimes changes over longer timest > 1. Include a plot that shows a noticeable nontrivial pattern evolving over lon代 写MATHS 3023/4123/7107 Partial Differential Equations & Waves Written Assignment 4R
代做程序编程语言ger times.
•  I don’t recommend that you use a mass matrix for this assignment. Instead, solve odes for the interior points only (see Question 1(e) from Workshop 7, for example).
•  Use bcs (2) to obtain the boundary values needed when evaluating the finite-difference approximations of v = uxx and uxxxx = vxx.
•  Make sure your plots are properly labelled with an informative caption or title.
•  Make sure you document your code.  The minimum documentation includes  a description of the script. and any functions, author name, date, and a description of any input and output arguments.
•  Submit one Matlabscript. that includes code added for the next part (c).
6          (c) Append Matlab code that:
i. uses fsolve() to find and plot nontrivial equilibria of this nonlinear system, then
ii. uses eigs() to determine the stability of the found equilibria.Run your code using the same parameters as part (b) for many different initial guesses to fsolve(). Include a plot of one stable and one unstable equilibrium solution in your report, together with the maximum eigenvalue for each. Explain why each equilbrium is stable or unstable.
•  I found some equilibria using initial guesses of the form. asin(kx) for different values of a and k.
•  Check the message output by fsolve() to make sure it has successfully converged to a solution.
•  As usual, make sure your plots are clearly labelled.
• Include the code for this part in the script. that you submit for part (b).2.  Consider free-surface flow of water above a flat impermeable boundary, as shown in figure 1.Figure 1: Free-surface flow above a flat impermeable boundary.
As derived in course notes, the velocity potential  satisfies Laplace’s equation

subject to boundary conditions

where ˆ(η)(ˆ(x), t(ˆ)) is the vertical displacement of the free surface.
Consider waves of amplitude a on the free surface. Scaling variables by

yields the nondimensional pde and boundary conditions
where ∈ = a/d.4           (a)  Suppose the wave amplitude is small in comparison to the depth, so that ∈ = a/d ≪ 1.
Substitute the expansions

into the nondimensional equations (4a)–(4d) to obtain the leading-order linearised prob- lem for φ 1  and η 1 .3           (b)  Seek a product form. solution φ1  = F(y)ei(kx−ωt) by substituting into the leading-order
pde and boundary condition on y = —1, and solving for F(y). You should obtain

for some constant C.5           (c)  Now use the two free-surface boundary conditions to find the dimensionless dispersionrelation for this problem, ie, the relationship between the wavenumber k and angular frequency W such that there are non-trivial solutions.  Hence write down a formula for the dimensionless wave speed c.









         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
