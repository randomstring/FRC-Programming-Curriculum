<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. PID</a></li>
<li><a href="#sec-2">2. math/pysics has many equations describing the real world, they seem very precise</a></li>
<li><a href="#sec-3">3. lets say we want to program a car's cruise control to drive at exactly 35mph</a></li>
<li><a href="#sec-4">4. what happens when anything changes?</a></li>
<li><a href="#sec-5">5. Real Wold</a></li>
<li><a href="#sec-6">6. Error. Here in the real world we have</a></li>
<li><a href="#sec-7">7. Step 0 Bang-Bang</a></li>
<li><a href="#sec-8">8. Step 1.  add some P</a></li>
<li><a href="#sec-9">9. When P is not enough</a></li>
<li><a href="#sec-10">10. Introducing I</a></li>
<li><a href="#sec-11">11. P + I controllers</a></li>
<li><a href="#sec-12">12. D controllers</a></li>
<li><a href="#sec-13">13. Resources</a></li>
</ul>
</div>
</div>

# PID<a id="sec-1" name="sec-1"></a>

# math/pysics has many equations describing the real world, they seem very precise<a id="sec-2" name="sec-2"></a>

# lets say we want to program a car's cruise control to drive at exactly 35mph<a id="sec-3" name="sec-3"></a>

-   say very specifically we want to be able to climb into a specific car and know exactly how far we need to push the accellerator to go 35mph on a specific road under controlled conditions
-   what do we need to know?
    -   weight of the car
    -   power output of engine
    -   incline/decline
    -   aeodynamic drag
    -   map of power at each point of accellerator's position
    -   altitude (affects aerodynamics)
    -   wind
    -   friction of tires ( inflation level, tread wear, road composition)
-   now calculate the drag, friction, inertia of car determine exact power needed
-   Tada!

# what happens when anything changes?<a id="sec-4" name="sec-4"></a>

-   disaster

# Real Wold<a id="sec-5" name="sec-5"></a>

-   any drivers in the room? do you do any of this to drive at a set speed? No.
-   what do we do?
    -   glance at the speedometer and press harder or lighter on the accellerator. Maybe even the brakes.
    -   Repeat until you're driving the right speed
-   is that hard? no
-   does it take a long time to learn this in a new car? no.
-   can robots drive this way? yes.

# Error. Here in the real world we have<a id="sec-6" name="sec-6"></a>

-   what we want (travel at 35 mph)
-   what actually is  (traveling at 0mph)
-   the difference is what we will call the error
-   to get what we want we want to minimize the error, idealy go to zero.

# Step 0 Bang-Bang<a id="sec-7" name="sec-7"></a>

-   if we're going too slow, 100% throttle
-   if we're going too fast, 0% throttle
-   This is called a Bang-Bang controller.
-   it works!  (kinda)
-   can we do better? yes.
-   bang-bang controllers are sometimes all you need. Shooter flywheel speed for example.

# Step 1.  add some P<a id="sec-8" name="sec-8"></a>

-   what if instead of just 100% or 0% throttle, we adjust our
    throttle according to how far off we are from our desired speed?
-   P stands for proportional
-   Units?   how to translate 35mph to slow into 20% throttle?
    
    error = desired<sub>speed</sub> - current<sub>speed</sub>
    
    Trottle = P \* error
    
    P = ???

-   We have no idea what P should be. What happens if we guess? 
    -   P = 10  
        
        Throttle = Min(1.0, P \* error)    # throttle can't go over 100%
        
        any error over 0.1 mph will result in full or zero throttle, essentially a bang-bang controller
    
    -   P = 1
        
        any error over 1 mph will result in full or zero throttle, better.
    
    -   P = 0.1 ? 
        
        any error over 10mph will result in full or zero throttle.
        errors in between result in moderation in the throttle.
        
        This might work!
        
        We don't even need to know if the driver had breakfast.

-   what happens if conditions change a little?
    -   we're going uphill, downhill
    -   we put premium unleaded in the tank this week
    -   the system adapts, and keeps applying more Throttle until we reach the correct speed
-   what if we change something big? new motor? pull a trailer?
    -   might keep working
    -   need to test it, what was ballance before might not be anymore
        or else we'd use the same P value for all speed controllers

# When P is not enough<a id="sec-9" name="sec-9"></a>

-   Undershooting and overshooting the goal
-   Sometimes P will overshoot and occilate
-   <graph>
-   Sometimes P doesn't provide enought "umph" to get us all the way to our goal, or it can take a long time.
-   <graph>
-   can we do better? Yes.

# Introducing I<a id="sec-10" name="sec-10"></a>

-   I is for Integral
-   remeber we used the current error times our P value for our proportional controller
-   I uses the total history of past errors
-   Now we have to keep track of error<sub>total</sub>, all the errors we've seen.
-   In calculus this would be a continuous function, however we're doing descrete calculations, say every 20ms or so

-   total<sub>error</sub> = total<sub>previous</sub><sub>error</sub> + current<sub>error</sub>

-   <graph>  
    -   This is the area under the curve
    -   (This will be become more clear once you've taken Calculus)
-   <graph with negative error>

K for "Kostant"

Throttle = Ki \* total<sub>error</sub>

-   <graph>
-   what does this do? If our controller get's stuck, the accumulated error pushes us towards the right throttle.
-   don't use just I controllers

# P + I controllers<a id="sec-11" name="sec-11"></a>

-   P controllers are pretty good by themselves
-   I element can help speed up when we're far off the target and give that final nudge when P can't finish the job
-   <graph comparing, P, I, and P +I>

# D controllers<a id="sec-12" name="sec-12"></a>

-   

# Resources<a id="sec-13" name="sec-13"></a>

-   <https://www.youtube.com/watch?v=UR0hOmjaHp0>
-   <https://www.youtube.com/watch?v=XfAt6hNV8XM>
-   <https://www.youtube.com/watch?v=pTuPhJ0DJB8>
