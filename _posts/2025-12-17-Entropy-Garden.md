---
title: Entropy Garden
date: 2025-12-17 22:26:00
categories: [ART, TECH_ART]
tags: []
---
## en·tro·py
*/ˈentrəpē/* • *noun*

**1.** *Physics*  
A thermodynamic quantity representing the **unavailability** of a system's thermal energy for conversion into mechanical work, often interpreted as the degree of disorder or **randomness** in the system.

> "the second law of thermodynamics says that entropy always increases with time"

**2.**  
Lack of order or **predictability**; **gradual** decline into disorder.

> Entropy is the general trend of the universe toward death and disorder.” —James R. Newman

---
I come from a family of 6, argumentative, opinionated, and curious. There is always a low pressure storm building, waiting to break out into an argument, debate, or spontaneous dance session in the kitchen.

I was first introduced to the idea of Entropy by my mother. As her parents (my Opa and Nana) began to age, the reality of living in the remote high desert of Nevada became infeasable. The property, including a well my Opa dug, first powered by a homemade windmill, then by the self-installed solar panels, required constant maintenance. My mom, the oldest, decided that we would build a house in our backyard for my Opa and Nana to move into. The [Entropy House](https://www.pinterest.com/levyrachael/entropy-house/) was born. This project, born from pragmatic love became a home for us all to experience the Entropy inherent in the process of life, death, and rebirth. 

![Windmill with Opa working](/assets/img/entropy-garden/windmill.jpg){: width="400"}
_My Opa maintaining the windmill that powered their well_

![Opa in front of windmill](/assets/img/entropy-garden/opa-windmill.jpg){: width="400"}
_The windmill, first powered by wind, then by solar_

![High desert home](/assets/img/entropy-garden/badger-street.jpg){: width="400"}
_The remote high desert home in Silver Springs, Nevada_

When Chloe asked for art submissions for her birthday gallery show, I knew I wanted to explore entropy. But I've never been confident calling myself an artist.

In high school, I applied to the Teen Arts Group (TAG) at the Seattle Art Museum to challenge that feeling of inadequacy. Lacking a typical piece of art to bring to the the interview, I brought my beat-up running shoes. I explained how the worn treads were a journal of my meditation across the many miles and places I'd been. I loved the challenge in seeing the art and meaning in something I thought was purely functional. What is art is a matter of perspective and a willingness to find the meaning. Following accceptance into the group, I knew this was the approach to art I wanted to bring. 

TAG was soooooo fun. Every Thursday we made art, ate snacks, and planned Teen Night Out: a free museum party for teens with live performances, figure painting, and tours. My favorite project as part of TAG was working with a piece from the museum's collection. I chose the elevator doors from the Chicago Stock Exchange, an exhibit I'd initially walked past without realizing it was art. 

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; margin: 2rem 0;">
  <iframe 
    src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fwww.facebook.com%2Fseattleartmuseumteens%2Fvideos%2F1561414370578080%2F&show_text=false&width=560&t=0" 
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;" 
    scrolling="no" 
    frameborder="0" 
    allowfullscreen="true" 
    allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share">
  </iframe>
</div>

So I knew my submission, to truly come from me, needed to be a little odd. I am a technical writer and spend my days writing code, creating diagrams, and responding to jira tickets. I also spend a lot of my day thinking about how to improve interactions between government Open Data and Artificial Intelligence. So I wanted a project that incooporated these parts of myself while also pushing me to think about Entropy and art and a rejection of the modern incarnation of Artificial Intelligence. 

I love algorithms and systems in school, so I started by looking at different old school styles of Artificial Intelligence that were both deterministic and stochastic while also being completely under my control, explainable, and low energy. 

I landed on `L-systems` a fun early form of AI introduced in 1968 by Aristid Lindenmayer, a Hungarian theoretical biologist and botanist at the University of Utrecht. Like how can I become a theoretical biologist whattttt. `L-systems` are a type of formal grammar where an alphabet of symbols is used to create strings a collection of clearly defined production rules. 

You can then take these strings and translate them to geometric structures to model the growth of plants. Truly an an early attempt at artificial life. 

Please interact with garden below! I created some initial templates for plants. Play with the colors, the stochasticity, line length, width, and the angles. If you are curious about creating new plants for the garden, change the rules to define your own artificial life (technical details follow below if you're curious how to do that). 

I love this because I do believe that technology is one of many tools we can use to help make our communities stronger, but I also think to do that, technology needs to be understandable, community driven, and beautiful. Enjoy!! 

## The Garden 

{% include entropy-garden/entropy-garden.html %}

## Technical Details 

L-systems are  

## Sources 

1. Bourke, Paul. “L-System Manual.” Paulbourke.net, [https://paulbourke.net/fractals/lsys/](https://paulbourke.net/fractals/lsys/).
2. “L-Systems Turtle Graphics Renderer - HTML5 Canvas - by Kevin Roast.” [https://www.kevs3d.co.uk/dev/lsystems/](https://www.kevs3d.co.uk/dev/lsystems/).

