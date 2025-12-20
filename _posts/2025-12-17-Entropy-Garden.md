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

My mother first introduced me to the idea of entropy. As her parents (my Opa and Nana) began to age, the reality of living in the remote high desert of Nevada became untenable. Their property required constant maintenance including a well, first powered by a homemade windmill, then by solar panels my Opa installed himself. 

My mom, the oldest of her siblings, decided to build a house in our backyard for my Opa and Nana to move into. Thus, the [Entropy House](https://www.pinterest.com/levyrachael/entropy-house/) was born. This project, born from pragmatic love, became a home for us all to experience the entropy inherent in the process of life, death, and rebirth. 

![Windmill with Opa working](/assets/img/entropy-garden/windmill.jpg){: width="400"}
_My Opa maintaining the windmill that powered their well_

![Opa in front of windmill](/assets/img/entropy-garden/opa-windmill.jpg){: width="400"}
_The windmill

![High desert home](/assets/img/entropy-garden/badger-street.jpg){: width="400"}
_The remote high desert home in Silver Springs, Nevada_

When Chloe asked for art submissions for her birthday gallery show, I knew I was going to take this moment to start my own blog (welcome :\)) and I wanted to explore entropy. I also wanted to continue to work on my persistent doubt that I'm not creative enough to be an artist.

I have been doing this work for a long time. In high school, I applied to the Teen Arts Group (TAG) at the Seattle Art Museum to challenge that feeling of inadequacy. Lacking a piece of art to bring to the interview, I brought my beat-up running shoes. I explained how the worn treads were a journal of meditation across the many miles and places I'd been. I loved the challenge of finding art and meaning in something purely functional. 

I continued to do that as part of TAG, advocating for creative projects at our events that were accessible to those who didn't connect to art in more traditional mediums.  My favorite project as part of TAG was showcasing a piece from the museum's collection. I chose the elevator doors from the Chicago Stock Exchange, an exhibit I'd initially walked past without even realizing it was part of the museum. 

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

So I knew my submission, to truly come from me, needed to be a little odd. I am a software engineer and spend my days writing code, creating diagrams, and responding to Jira tickets. I also spend a lot of my day thinking about how to improve interactions between government Open Data and Artificial Intelligence (deeply conflicted about this). I wanted a project that incorporated these parts of myself while pushing me to think about entropy, art, and my complicated relationship with the modern AI.

I started by looking at older styles of Artificial Intelligence that were deterministic *and* stochastic, explainable, low energy, and understandable. 

I decided on `L-systems` an early form of AI introduced in 1968 by Aristid Lindenmayer, a Hungarian theoretical biologist and botanist at the University of Utrecht. `L-systems` are a type of formal grammar where an alphabet of symbols is used to create strings using a collection of clearly defined production rules. You can then take these strings and translate them to geometric structures to model the growth of plants. I loved that this technique was able to create artificial life using only a few clearly defined and understandable rules. 

Please interact with garden below! I created some initial templates for plants. Play with the colors, the stochasticity, line length, width, and the angles. If you are interested in creating new plants for the garden, change the rules to define your own artificial life (technical explaination follows below if you're curious how to do that). 

I believe that technology is one of many tools we can use to help make our communities stronger. But I also want technology to be understandable, community driven, and beautiful. Enjoy!! 

## The Garden 

{% include entropy-garden/entropy-garden.html %}

## Explanation

### What Are L-Systems?

An `L-system` (Lindenmayer system) consists of three components:

- **Alphabet**: A set of symbols (e.g., `F`, `+`, `-`, `[`, `]`)
- **Axiom**: The initial string (e.g., `F`)
- **Production**: Rules: Rules that define how each symbol transforms (e.g., `F -> FF+[+F-F-F]-[-F+F+F]`)

The system works by iteratively applying the production rules. Each generation, every symbol in the string is replaced according to its rule. After several generations, you get a complex string that encodes a branching structure.

### Turtle Graphics Interpretation
The string is interpreted using "turtle graphics," where an imaginary turtle walks and draws

| Symbol | Action                                            |
| ------ | ------------------------------------------------- |
| `F`    | Move forward and draw a line                      |
| `+`    | Turn right by the specified angle                 |
| `-`    | Turn left by the specified angle                  |
| `[`    | Save current position and angle (push to stack)   |
| `]`    | Restore saved position and angle (pop from stack) |

The `[` and `]` brackets create branching: the turtle "remembers" where it was, explores a branch, then returns to continue the main stem.

### Deterministic vs. Stochastic

**Deterministic L-systems** produce the same output every time—the same rules always generate the same plant.

**Stochastic L-systems** introduce randomness by providing multiple possible replacements for a symbol. Each time a rule is applied, one option is chosen at random. This creates natural variation: no two plants are exactly alike. 

### Example: A Simple Bush

```
Axiom: F
Rule:  F -> FF+[+F-F-F]-[-F+F+F]
Angle: 25
```

Generation 0: `F`  
Generation 1: `FF+[+F-F-F]-[-F+F+F]`  
Generation 2: `FF+[+F-F-F]-[-F+F+F]FF+[+F-F-F]-[-F+F+F]+[+FF+[+F-F-F]-[-F+F+F]...`

After 4-5 generations, the string encodes a complex branching structure that resembles a bush.

### Creating Your Own Plants

Try modifying these parameters in the garden above:

- **Angle**: Smaller angles (15-25) create denser plants; larger angles (35-45) create more spread
- **Iterations**: More iterations = more complexity (but slower rendering)
- **Rules**: Add more branches with `[+F]` or `[-F]`, create asymmetry with different angles
- **Randomness**: Add percentage to create natural variation in angles and lengths

---

## Sources 

1. Bourke, Paul. “L-System Manual.” Paulbourke.net, [https://paulbourke.net/fractals/lsys/](https://paulbourke.net/fractals/lsys/).
2. “L-Systems Turtle Graphics Renderer - HTML5 Canvas - by Kevin Roast.” [https://www.kevs3d.co.uk/dev/lsystems/](https://www.kevs3d.co.uk/dev/lsystems/).
3. “L-System.” Wikipedia, 4 Jan. 2021, [https://en.wikipedia.org/wiki/L-system](https://en.wikipedia.org/wiki/L-system).
4. “Theory of Computation - Home.” Wooster.edu, 2017, [https://csweb.wooster.edu/dbyrnes/cs220/](https://csweb.wooster.edu/dbyrnes/cs220/). Accessed 19 Dec. 2025.
