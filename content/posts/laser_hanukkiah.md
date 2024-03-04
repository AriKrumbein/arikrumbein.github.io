+++
title = 'Laser Hanukkiah'
date = 2024-02-27
draft = true
type = 'post'
+++

At last! I'm excited to announce something that I'm working on!

Last year, [my friend Ben](https://www.benvlehmann.com/about) saw this, 

![Jewish Space Laser Switch](/static/images/JewishSpaceLaser.png)

and decided that what would go great with that was, well, a Jewish Space Hanukkiah. And thus, this beautiful frankenstein was born.

- This year, he decided he wanted to go bigger, and he enlisted yours truly to make it happen. 
- I'm truly crap when it comes to physics, and have *no* understanding of thermodynamics, but I *do* have 3D printing and design experience, so I'm in charge of the design and the aesthetics of the project.
  - Not a great decision, when you consider my aesthetic sensibilities, which are very utilitarian 😂

# Outline of project blog
- The lasers
  - Upgrading past green
  - Color
  - intensity
- Thermals
  - Thermo 101
  - How much heat do we need to get rid of?
    - Things we know: max operating temps, power outputs
  - Strategies
    - Heatsinking
      - pitfalls: Many Thermal Resistance coefficients are missing flowrate information
    - Fans
    - Thermal design of menorah
- (later) Design of containment cages
- (later) design of adjustment apparatus

## The Lasers
- Last year, Ben used some cheap 50mW green laser modules to get the project up and running
  - this year, we're leaning away from the Christmas-y theme and going with Blue lasers instead.
- Also a safety concern: cheap green lasers throw a *lot* of infrared light
  - This is where I admit that the learning curve is *steeeeeep*
  - had to tap into my high school chemistry knowledge banks to remember emissions spectra
  - For those of you not fortunate enough to remember: visible light is made up of different bands, which mix to form the colors you see
  - Laser modules pump out photons in a specific *range*
  - Cheap green light lasers derive their beam from an IR laser, doubling the frequency along the way to produce something green
    - problem: the process is very inefficent and throws off a bunch of IR light
    - Many green lasers also don't have IR filters, which is *bad* for your eyes
    - Learn more: https://hackaday.com/2018/08/31/science-shows-green-lasers-might-be-more-than-you-bargained-for/
- All this to say: we want something both more powerful, while still staying safe

### So what are we looking at?
- While we could go for something that evokes Darth Maul's Hanukkiah, blue is cool so let's do that
- Well... turns out blue lasers are actually *much* harder to come by [for reasons people much smarter than me can explain much better](https://www.youtube.com/watch?v=AF8d72mA41M&ab_channel=Veritasium).
- Things that resemble blue fall in roughly 450nm - 490nm
- That narrows it down to: 447, 450 and 488
- and lookie here, we've got some options!

### How bright do we want to be?
- One of my favorite XKCD comics is very appropos here: https://what-if.xkcd.com/13/
- Goal: light a room with this thing
  - ChatGPT says you want ~10-20 lm/sq^2
  - Let's say it's a 10x10 room, 100ft^2 * 10lm/ft^2 = 1000lm
  - Luminous Flux (lm)=Radiant Flux (W)×Luminous Efficacy (lm/W)
  - Radiant Flux (W) = Luminous Flux (lm) / Luminous Efficacy (lm/W)
  - W = 1000lm / 

Well...
![What if we tried more power?](https://what-if.xkcd.com/imgs/a/13/laser_pointer_more_power.png)

That's enough to light the room, I guess!

## Thermals
### Getting rid of heat
- this thing will look great in your window, but without proper thermals, it will look like that for 5 minutes before it starts smoking
- Welcome to thermo 101!
- Name of the game is heat disapation
  - we want to get rid of at much hot air as we can, or this 3D-printed plastic is going to shrink or worse, burn
- 

### 




---
laser max op: 85C
ambient ~25C
deltaT = 60C -> 50C

Peak laser power: 3.5W -> 4W

Goal: at 50C above ambient, we need to dissapate AT LEAST 4W.
- At what temperature will the system equilibrate? Let's get below that number.
- Where Q_input == Q_output
- 

Thermal resistance coefficient <<<<<< 12.5C/W IF Ambient air tempature stays the same

If we're good at zero airflow, we're good

## Homework
Structually sound
- room for cables
- airflow

Heat resistance in plastic?

Can fit ~170mm fan?