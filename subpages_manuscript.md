
# My Detailed Research Interest

(This section should include my understanding of an ideal paradigm.)

# The Broad Goal
Confucius said "朝闻道，夕死可矣。", which translates to "When you know about the truth of the world in the morning, you won't regret dying in the evening." In the general-purpose AI field, we've made great achievements in making agents that can reason, solve pen-and-paper problems, and generate authentic multimedia assets, but one part missing is the interpretation of AI's "working principle" in a way that we can truly appreciate, apart from a true but not inspiring claim like "predicting the next token", or "procedurally denoising an image". I envision an ideal piece of AI to be like a calculator or a computer program, where we can:
* Understand its design philosophy and implementation details.
* Tweak its internals precisely for our customized needs.
* Have great confidence regarding its behavior, including what is expected, possible and impossible.
* Hand-calculate what AI does and end up with the same outcome by following the same instruction.
* Update a piece of knowledge and functionality easily and precisely without unwanted side-effects.
* Learn from how AI solves problems and boost our independent problem-solving capability.

If our AI can achieve these, then I would claim that I "have no regret". However, existing AI systems are far from perfect from this aspect. Take LLM as an example: its high-level working principle is a black box and opaque to us; we can only "talk" to it for expressing our needs without direct control; reliability and safety is not guaranteed but measured with success rate; producing or updating a model takes tremendous amount of resource, whose necessity is questionable with respect to what we get; its working principle (fitting large corpus) is not helpful to the general public and tend to make humans lazier rather than wiser.

I think the reason why the problem hasn't been solved for so long is because we're trapped in a local optimum: data-driven methods appear to be more effective than human-specified rules due to the big data we have access to, just like when we have a large pool of petroleum we can drill, we won't have the motivation to develop sustainable energy.

Despite the convenience of automatic training from data, it also traps us from cleanly solving the problems listed above. For example, when we want to make the model more efficient and transparent by making it reason in concepts instead of tokens, we first have to think whether there is a lot of data examples regarding reasoning in concepts, and in most cases, there isn't, so the idea does not work. Therefore, cleanly solving deep learning's structural problems by patching deep learning methods is not possible.

What's worse is that the AI research field has a lot of inertia: when deep learning methods appear to be successful, researchers swarm to this field and push the SOTA further and further. They add more and more patches to ease the problems and give an illusion that the direction is promising and improvement is unbounded. On the other hand, if a researcher decides to try a different paradigm to cleanly address the limitations, they will find much more setbacks, like a much longer trial and error procedure, or the fact that their work is unlikely to beat deep learning SOTA immediately. These setbacks can easily discourage them and send them back to the mainstream direction. As a consequence, now when we talk about AI, we are almost talking about deep learning exclusively.

# My Interpretation of Intelligence
There are many theories regarding what intelligence is and what intelligence we should build. For example, some think that intelligence can be emerged, some think that intelligence can only be imitated from human behavior, and some think that intelligence can only be achieved through specific neural connections like the one in our brain. My opinion is that it is easier to talk about intelligence in a practical sense since we can at least specify its intended behavior. For example, we would rather have an AI that has limited capabilities and actually helps us with our work, than an oracle that knows everything but refuses to help.

In this sense, I'd like to argue that intelligence we want cannot be solely achieved through automatic evolution or "learning from environment". Imagine that we expose everything to AI but only hide the existence of "popsicle", then it is impossible for AI to know the existence of it by interpolating among other desserts it knows, like chocolate, cake, or chocolate cake. In fact, "popsicle" is accidentally invented very long time ago when a person accidentally put a stirring stick in a cup of coffee outdoors in winter. To be able to discover it from scratch, AI has to simulate the whole world in the atom level, which is not only impractical but also leads to another problem: AI may come up with other types of desserts also due to "accidents" in a simulated world, but non of them is relevant to us in the real world. Therefore, to count a piece of intelligence as practical, a fundamental requirement is that it matters to us and adhere to what we know and care.

Practical intelligence should not only reflect the material world, but also reflect human society and culture. For example, the English language can be perceived as a terrible language due to its mixed source of words, inconsistency between spelling and pronunciation, and many unnecessary grammatic rules and exceptions. However, we never attempted to change these characteristics but instead pass it on to the next generation and explicitly maintain those flawed designs. This is because from a practical sense, it is much cheaper to adapt to these flaws than requiring the whole humanity to adapt to a new rule simultaneously. Therefore, many randomly made-up things become truths to the human beings, and we regard an AI as intelligent if it can adapt to the same made-up thing, even if there appear to have a better alternative. This also proves that an AI should not undergo arbitrary self-improvement or evolution, since if it invents x87 instead of x86, Linuy instead of Linux, it will struggle to adapt to the existing ecosystem and appear much less practical to human beings.

## "Anchors" as the backbone of a practical AI

Therefore, I think a practical AI should be made of "anchors" and "interpolation". "Anchors" refer to any fact or object agreed by human beings, from a type of dessert to a lemma in mathematics. It serves as a backbone of the AI to establish mutual understanding with human beings, and allow AI to come up with solutions and creations comprehensible to human beings. "Interpolation" refers to the ability to solve unseen but similar problems while being backed by the "anchors".

(Here we should talk about LLM and how the "anchors" in LLMs are implicitly encoded and prone to careless weight updates)

## "Convenience" and "As-is": not a binary choice but a smart fusion
We want convenience as a user to let AI infer the missing piece or clamp to a well-known concept automatically, and we want explicitness as a developer to debug and understand what the AI is doing.

Sometimes as a user, we also want AI to tell us whether we're asking for something weird instead of letting it silently correcting our mistakes or executing the malformed request as-is. This is a good improvement on "mutual-understanding" while keeping the request simple and straightforward. To achieve this, we want AI to know about the priors of its task, like what is common and what is rare.

The ideal way of taking advantage of both is to have an interpretation layer between a convenient representation and an as-is representation.

One potential problem is that the convention may shift over time, and the interpretation layer may need to be updated accordingly. This is under the assumption that the "as-is" representation is fixed.

Another potential problem is that the "as-is" representation also needs to drift over time because of the "prior" drift as our demands change over time.

For example, we used to classify Pluto as a planet, but now it is classified as a dwarf planet, so the as-is representation needs to be updated accordingly so that AI does not associate Pluto when talking about planets.

## Challenges

These will be elaborated in the "My Long-Term Research Plan" section, with potential solutions proposed.

* The working principle of the ideal AI to solve a problem end-to-end and interact with the IO. This is obvious for LLMs since they solve problems by generating text, but not obvious for a non-deep-learning-based AI.
* Even if the working principle is clear, it is challenging to build an AI by filling the anchors and rules for interpolation so that it can adapt to different contexts and demands. (This may be partially automated since we now have oracle-like LLMs that can help us with repetitive work.)
* When we want to maintain the AI and change a part of it over time, we may encounter problems like leaving inconsistencies in the system.

# My Preliminary Understanding of the Current AI Field

(This section should cover the problems we encounter)



# My Long-Term Research Plan

I'm heading for the "ideal AI" described above. The working principle can be described as "a graph of concepts". Concepts are sparsely connected according to their closeness in relationship.

There are many critical questions I need to answer to achieve this goal.

Question:
## How to achieve end-to-end problem solving, including interacting with the IO?



## How to utilize the relationships between the concepts?

## How to actually do actions? Do we have algorithms for all tasks or do we let AI to "act on impulse"?

## How to maintain the AI systematically and efficiently?



My plan may undergo major revisions as the research goes on, or even prove infeasible. However, I believe that the deep-learning-free paradigm is gradually becoming feasible since now we have LLMs as oracles to help us with the large amount of manual effort that used to require exclusive human labor. Also, in the worst-case scenario the idea will be a high-level LLM problem solving cache where solved problem variants can be solved efficiently with rule-based systems while unsolved problems can be solved by an LLM and turned into a new rule-based solver.

Now let me talk about what "high-level working principle" is in my understanding.

This contradicts with the idea that intelligence is something that can be fully achieved through interacting with environment, or evolution, or is something simple and beautiful (objecting "xxx is all you need" idea).

The relationship between concepts and actions




Apart from listing what I expect from an ideal AI, I also have some ideas regarding how it can be achieved.









# My Short-Term Research Plan
