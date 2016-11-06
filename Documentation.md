# Lunar Hopper Documentation
### ox\_pulse() vs ox\_Pulse() 
Both functions are used to prime the catalyst bed with a pulse of oxygen. This requires the pressure in the system to be at a certain level, otherwise the oxygen will not react with the catalyst.

ox_pulse() checks to see if the pressure alright before opening the solenoids, but Pressurisation() is never called before doing so. This means that the oxygen will never be fired at the catalyst, so the hopper won't take off.

Therefore ox\_Pulse() should be used over ox\_pulse().