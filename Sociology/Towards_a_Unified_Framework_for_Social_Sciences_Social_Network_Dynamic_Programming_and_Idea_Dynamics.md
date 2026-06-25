# Towards a Unified Framework for Social Sciences: Social Network Dynamic Programming and Idea Dynamics

**Author**: [yefeiheng@gmail.com]  
**Affiliation**: [Affiliation]  
**Date**: June 26, 2026

## Abstract

Social phenomena—from market prices to political movements, from cultural norms to collective action—emerge from the iterative aggregation of individual decisions transmitted and transformed through social networks. Despite their apparent diversity, these phenomena share a common underlying mechanism: agents inject signals into a network, receive signals from others, process them based on internal cognitive models, and output updated signals. This iterative process, under specific structural and informational conditions, converges to macroscopic patterns observable as social regularities. In this paper, we propose a unified framework that formally describes this mechanism by combining two complementary components: *Social Network Dynamic Programming* (SNDP), which models the iterative computation over network graphs, and *Idea Dynamics* (ID), which captures the micro-level cognitive processing of information during interpersonal transmission. We show that many canonical topics in economics, political science, sociology, and related disciplines can be reformulated within this framework. We further analyze the conditions for convergence, the role of key nodes, the impact of deceptive signals, and the dark side of forced convergence through coercion. We argue that this framework provides a foundational language for integrating the social sciences and offers practical insights for network design, information transparency, and individual agency in an era of large-scale AI-mediated communication.

## 1. Introduction

A stock price jumps, a hashtag goes viral, a social movement sweeps across borders, a consumption habit becomes the new normal. Traditional explanations for such social phenomena often fall into three categories: structural narratives (economic laws, institutional design, cultural tradition), agent-centric narratives (the actions of great individuals or organized interests), or stochastic narratives (random drift or "the spirit of the times"). While each captures part of the picture, they share a common blind spot: they bypass the *intermediate process* through which countless individual micro-decisions, interacting through social networks, give rise to macroscopic patterns.

Consider the GameStop short squeeze of early 2021. Within weeks, millions of retail investors, coordinating loosely through online forums, drove the stock price from around $20 to over $480, causing billions in losses for hedge funds. No central authority issued commands; no voting determined the collective action. Each participant observed signals (forum posts, price movements, news), interpreted them, and decided whether to buy, hold, or sell. The aggregate outcome—a dramatic price spike—was not designed by anyone; it *emerged* from the iterative interaction of countless local decisions.

This paper proposes that *all social phenomena*, regardless of their domain, can be understood as the result of such an iterative computational process running on the graph of social connections. The process is governed by two interacting mechanisms: (1) the network topology and the dynamic programming-like iteration of signals (Social Network Dynamic Programming, SNDP), and (2) the cognitive transformations that information undergoes during interpersonal transmission (Idea Dynamics, ID).

The core propositions are:

1. All social phenomena arise from the convergence of individual decisions after multiple rounds of network iteration. The social network can be formalized as a graph with various graph-theoretic algorithms.
2. Society moves in the direction of the resultant vector of all individual decisions—a weighted resultant, reflecting structural inequalities in network positions and resources.
3. A minority of individuals become *key nodes* in the network, influencing a portion of decisions and thereby steering the direction of society.
4. The logic of network iteration can be explained via dynamic programming: each agent inputs a signal into the network; other agents receive it, perform an iterative computation combining their own understanding, and transmit a new signal; under appropriate conditions, this process converges.
5. Environmental changes can break existing convergences, triggering new rounds of iteration that converge to new social phenomena.
6. Economics, political science, sociology, and related social sciences all conform to this characteristic, because they fundamentally study relationships between individuals.
7. Market prices are the result of multiple rounds of iteration of all individual decisions. Highly liquid assets converge efficiently to fair value; illiquid assets, with fewer participants, are susceptible to manipulation.
8. Some issues fail to converge because differences in understanding among individuals are too large, resulting in persistent dynamic fluctuation.
9. In cases of poor connectivity, partial consensus may converge within small clusters, disconnected from broader acceptance.
10. Network structure inherently contains weight differences among individuals; an individual's resources largely determine their weight.
11. Key nodes in the network are typically those who provide value to others—emotional value, material value, or belief value.
12. Some individuals can disrupt the iteration efficiency by emitting deceptive signals. The more transparent the network, the higher the convergence efficiency.
13. Conquest and oppression can force network convergence, representing a coercive rather than consensual mode of convergence—a critical, and often dark, aspect of the model.

The remainder of this paper is structured as follows. Section 2 formalizes the SNDP framework using graph theory and dynamic programming. Section 3 develops Idea Dynamics as the micro-level engine of signal processing. Section 4 integrates the two into a unified model and analyzes convergence conditions. Section 5 applies the framework to canonical phenomena in economics, political science, and sociology. Section 6 discusses edge cases, deceptive signals, and forced convergence. Section 7 examines current trends, including the impact of large language models (such as GPT-5 and Claude 4.8 in 2026) and community resilience practices. Section 8 concludes with implications for individuals and policy.

## 2. Social Network Dynamic Programming (SNDP)

### 2.1 Social Networks as Graphs

A social network can be formally represented as a graph \( G = (V, E) \), where \( V \) is the set of nodes representing individuals, and \( E \) is the set of edges representing relationships. Each edge may carry a weight \( w_{ij} \) denoting the strength of influence from node \( i \) to node \( j \). The structural properties of this graph determine the pathways and efficiency of information flow.

Key graph-theoretic metrics include:

- **Degree** \( d_i \): the number of connections of node \( i \). High-degree nodes act as natural broadcasters.
- **Path length** \( L_{ij} \): the minimum number of edges between \( i \) and \( j \). Empirical studies (Milgram, 1967; Dodds et al., 2003; Backstrom et al., 2012) consistently find average path lengths of 4–6 in large-scale social networks, implying rapid potential reach.
- **Clustering coefficient** \( C_i \): the fraction of a node's neighbors who are themselves connected. High clustering implies localized information recycling; low clustering facilitates information exit from the local group.
- **Betweenness centrality** \( B_i \): the number of shortest paths that pass through node \( i \). Nodes with high betweenness serve as bridges across otherwise disconnected communities, occupying "structural holes" (Burt, 1992).
- **Eigenvector centrality**: a node's importance weighted by the importance of its neighbors (cf. PageRank; Brin & Page, 1998).

These metrics capture the *structural weight* differences among individuals. Importantly, an individual's resources—financial capital, social capital, cultural capital, attention capital—strongly influence which network positions they can occupy and thus their effective weight in the social computation (Proposition 10, 11).

### 2.2 Dynamic Programming on Graphs

We model the social computation as an iterative process akin to dynamic programming. Let each node \( i \) at time \( t \) hold a state vector \( \mathbf{s}_i^{(t)} \) representing its current opinion, decision, or signal. At each time step, node \( i \):

1. **Receives** signals from its neighbors: \( \{\mathbf{m}_{j \to i}^{(t)} | j \in \mathcal{N}(i)\} \), where \( \mathcal{N}(i) \) is the set of neighbors of \( i \).
2. **Processes** these signals through a node-specific function \( f_i \) that combines incoming information with its own prior state and intrinsic characteristics.
3. **Updates** its state: \( \mathbf{s}_i^{(t+1)} = f_i(\mathbf{s}_i^{(t)}, \{\mathbf{m}_{j \to i}^{(t)}\}) \).
4. **Outputs** a new message \( \mathbf{m}_{i \to j}^{(t+1)} \) to its neighbors (which may be identical to or a transformation of its updated state).

The global state of the network evolves through repeated application of these local update rules. Under certain conditions (discussed in Section 4), the network converges to a stable configuration \( \mathbf{S}^* = \{\mathbf{s}_i^*\} \), which constitutes the observable macroscopic social phenomenon.

This framework is *distributed*: no node requires global information to perform its local computation, yet the aggregate outcome can exhibit global order. This matches the logic of dynamic programming, where a complex problem is decomposed into a sequence of locally solvable subproblems whose solutions combine to yield the global optimum.

### 2.3 Key Nodes and Influence Amplification

In the graph, some nodes exert disproportionate influence on the final convergence. A *key node* is defined operationally as a node whose state change or signal emission, if modified, would significantly alter the convergence trajectory of a substantial portion of the network. Formally, key nodes tend to have high values on centrality measures and/or high edge weights to other influential nodes.

Key nodes influence the iteration in three ways (Proposition 3, 4):

- **Signal injection**: With larger reach, their initial signals achieve higher "concentration" in the network.
- **Signal amplification**: By retransmitting signals from peripheral nodes, they grant those signals a larger effective audience.
- **Signal modulation**: They add commentary, reframe issues, and attach emotional valence, altering the probability that the signal will be accepted and further transmitted by others.

Empirically, key nodes are often those who provide value to others—emotional value (social cohesion and support), material value (access to resources), or belief value (interpretive frameworks) (Proposition 12). A community organizer who simultaneously provides emotional care, job connections, and policy interpretation exemplifies a multi-value key node with high network resilience.

## 3. Idea Dynamics: The Micro-Processing Engine

If SNDP provides the skeleton—the network structure and the iterative logic—*Idea Dynamics* (ID) provides the flesh: the cognitive micro-mechanisms by which individuals process signals in each iteration.

### 3.1 The Transformation Triad

When an individual receives a signal (an idea, a piece of information, a decision), they do not pass it on verbatim. Instead, three cognitive operations typically occur (cf. Bartlett, 1932; Allport & Postman, 1947; Kashima, 2000):

1. **Compression**: Details are stripped away; only the most salient or emotionally striking elements are retained. A 3000-word policy analysis becomes "the government plans to raise taxes."
2. **Assimilation**: The information is interpreted through pre-existing cognitive schemas, beliefs, and biases. Confirmation bias (Nickerson, 1998) leads individuals to accept congenial information and reject or reinterpret uncongenial information.
3. **Emotional tagging**: The affective experience during reception is encoded and often becomes the primary content transmitted. Fear, anger, amusement, and warmth are potent carriers of ideas.

These operations constitute the node-specific function \( f_i \) in the SNDP model. The same input signal can produce vastly different outputs depending on the receiver's cognitive priors and emotional state. This explains why, in social iteration, the original signal frequently mutates—not due to malice, but due to the inherent nature of human information processing.

### 3.2 Propagation Fitness and Memetic Selection

Because of the transformation triad, not all ideas propagate equally. An idea's *propagation fitness* depends on its ability to survive compression, align with widespread cognitive schemas, and evoke strong emotions. This aligns with the concept of *memetic selection* (Dawkins, 1976; Blackmore, 1999) and the observation that simplicity, emotional resonance, and compatibility with existing beliefs are key predictors of viral spread (Berger & Milkman, 2012; Vosoughi et al., 2018).

For instance, during the early COVID-19 pandemic, the slogan "Wear a mask, save lives" spread widely because it was concise (compression-friendly), activated the schema of personal responsibility (assimilation), and evoked both fear and solidarity (emotional tagging). Conversely, nuanced public health guidance often failed to propagate because it broke down under compression and lacked strong emotional hooks.

### 3.3 Critical Thresholds and Cascade Dynamics

Idea Dynamics also provides the micro-foundation for the nonlinear "tipping point" phenomena observed in social cascades (Granovetter, 1978; Schelling, 1978). As more individuals in one's local network adopt a certain decision (e.g., joining a protest, buying a product, using a hashtag), the perceived social proof lowers the psychological threshold for the individual to follow suit. Each additional adopter makes the next adoption incrementally more likely, creating a positive feedback loop.

The #MeToo movement in 2017 exemplified this dynamic. An initial tweet by Alyssa Milano triggered a cascade not because her message was novel—Tarana Burke had coined the phrase a decade earlier—but because the network had reached a state of high latent readiness. Each public disclosure lowered the inhibition threshold for observers, accelerating the cascade until it became a global phenomenon.

## 4. The Unified Model: Convergence, Divergence, and Deception

### 4.1 Formalizing the Unified Framework

The unified model posits that social reality is the result of:

\[
\mathbf{S}^{(t+1)} = F(\mathbf{S}^{(t)}; G, \{f_i\})
\]

where \( \mathbf{S} \) is the global state, \( G \) is the social graph, and \( \{f_i\} \) are the individual processing functions characterized by Idea Dynamics. The process iterates until \( \mathbf{S}^{(t+1)} \approx \mathbf{S}^{(t)} \) (convergence).

### 4.2 Conditions for Convergence

Drawing on the dynamic programming analogy and the properties of iterative algorithms, we identify two necessary conditions for global convergence to a single consensus:

1. **Algorithmic compatibility**: The node functions \( f_i \) must not be based on mutually incompatible fundamental axioms. If two subgroups operate on incommensurable foundational premises (e.g., "life begins at conception" vs. "bodily autonomy is paramount"), each may internally converge to a stable state, but the global system will oscillate between polarized equilibria without a unified convergence (Proposition 8).

2. **Sufficient network connectivity**: The graph \( G \) must be connected enough for cross-group signal exchange. When the network fragments into densely connected clusters with few inter-cluster edges, each cluster independently converges to a local consensus, but no global consensus forms (Proposition 9). Empirically, different social media platforms often exhibit non-overlapping trending topics, indicating modularized local convergence.

Environmental changes—such as technological disruptions, economic crises, or pandemics—can break existing convergences by altering the constraints under which node functions operate, thereby resetting the iterative process (Proposition 5). The post-COVID shift in remote work norms is a recent large-scale example: a previously stable consensus ("remote work is infeasible for most jobs") was shattered by an exogenous shock, and new norms converged over subsequent years. By 2026, approximately 28% of full-time work in the U.S. is fully remote, a roughly fourfold increase from 2019, illustrating a new convergence.

### 4.3 Deceptive Signals and Transparency

Proposition 13 introduces a crucial complication: some nodes may strategically emit deceptive signals to manipulate the iteration. Deceptive signals pollute the information environment, analogous to noise in a communication channel, reducing the signal-to-noise ratio and slowing or distorting convergence.

The impact of deception is directly moderated by *network transparency*: the degree to which signal sources are traceable, authenticity is verifiable, and deceptive actors face detectable consequences. In transparent networks, deceptive signals are more easily identified and filtered out, preserving convergence efficiency. In opaque networks, deception can significantly warp the emergent social reality.

The proliferation of advanced generative AI models (GPT-5, Claude 4.8 as of mid-2026) has dramatically lowered the cost of producing convincing deceptive signals. An individual can generate hundreds of personalized, high-persuasiveness messages in minutes. This has spurred regulatory efforts such as the EU AI Act's transparency provisions and experiments with digital watermarking and content provenance tracking—all attempts to maintain sufficient network transparency for functional social computation.

### 4.4 Forced Convergence: The Dark Side of the Model

Proposition 14 addresses the most ethically charged aspect of the framework: convergence achieved not through distributed consensus but through coercion. Throughout human history, many instances of apparent social stability were products of conquest, oppression, and the violent suppression of dissenting signals.

In graph-theoretic terms, forced convergence occurs when a subset of nodes, through overwhelming power, effectively prunes the edges of or silences the output functions of other nodes. The resulting macro-state may appear stable, but it is a *pseudo-convergence*. The silenced signals remain latent; once the coercive force weakens, they re-enter the network, often causing rapid and destabilizing cascades.

Distinguishing between consensual convergence (iterative, distributed, based on voluntary signal processing) and forced convergence (coercive, centralized, based on signal suppression) is essential for both analytical accuracy and normative judgment. The model describes both, but does not equate them.

## 5. Applications Across the Social Sciences

### 5.1 Economics: Price Formation as Iterative Computation

Proposition 7 states that market prices are the result of multiple rounds of iteration of all individual decisions. This formulation directly parallels the neoclassical concept of price discovery through supply and demand, but with an explicit network structure.

For highly liquid assets such as large-cap stocks on major exchanges, the network is vast, dense, and fast—millions of nodes (traders, algorithms) processing information and submitting orders with minimal latency. Each transaction price becomes the new state input for the next round of decisions. Convergence is rapid, and the resulting price efficiently aggregates dispersed information (Fama, 1970).

Conversely, for illiquid assets with few participants (e.g., micro-cap stocks, certain cryptocurrencies with concentrated ownership), the network graph is sparse and low-degree. A small number of nodes can dominate the computation, leading to prices that are easily manipulated and diverge from fundamental values. This matches the empirical observation that illiquid markets are more prone to manipulation and extreme volatility.

### 5.2 Political Science: Polarization and Gridlock

Political polarization can be understood as a failure of convergence due to algorithmic incompatibility. When two ideological communities operate on incommensurable foundational axioms, each internally converges to a stable, internally consistent worldview. Cross-community signals are systematically rejected by the receiving side's processing functions as invalid or hostile, resulting in no effective cross-group iteration. The macro state persists in dynamic oscillation between two polar equilibria.

The abortion debate in the United States exemplifies this pattern. Despite decades of public discourse, the distribution of public opinion has remained remarkably stable, with only narrow fluctuations, because the two sides' core premises are logically disjoint. The 2022 overturning of *Roe v. Wade* did not produce a new national consensus but rather intensified the oscillation, with state-level policies diverging sharply.

### 5.3 Sociology: Norm Diffusion and Local Consensus

The diffusion of social norms (e.g., etiquette, hygiene practices, smoking bans) follows the iterative convergence model. An initial innovation (using a fork, banning indoor smoking) is introduced by a small set of early adopters. Observers in their networks, influenced by social proof and the perceived benefits, gradually adopt the practice, lowering thresholds for the next wave. Over time, the behavior becomes a new norm—a stable macroscopic pattern.

However, when network connectivity is poor, norms may diffuse only within local clusters, leading to fragmented social realities. For instance, etiquette or moral standards that are taken as universal within a particular subculture may be entirely unknown or rejected in the broader society. This is the structural basis for the phenomenon of "echo chambers" and "filter bubbles" (Pariser, 2011; Sunstein, 2001).

## 6. Current Trends and Future Directions

### 6.1 AI-Augmented Nodes and the Transformation of Iteration

As of 2026, large language models (LLMs) such as GPT-5 and Claude 4.8 are deeply integrated into daily communication. Individuals increasingly use AI tools to compose social media posts, interpret complex events, and craft persuasive arguments. This effectively augments the node function \( f_i \) with a powerful external processor.

The implications are dual-edged:

- **Democratization of influence**: An individual with strong values and clear communication goals can, with AI assistance, amplify their signal quality and reach, potentially becoming a key node in their domain more rapidly than previously possible.
- **Proliferation of deceptive signals**: Malicious actors can generate vast quantities of highly convincing false content at near-zero marginal cost, degrading network-wide signal quality unless counterbalanced by robust transparency mechanisms.

### 6.2 Community Resilience: Designing Networks for Healthy Iteration

A promising practical application of the framework lies in the deliberate design of resilient community networks. Pilot projects in various cities have established "community information liaison" systems: trusted local residents trained to verify and relay critical information during crises. These liaisons effectively serve as designed key nodes with high local trust (value provision), improving the network's immunity to rumors and reducing the likelihood of panic cascades.

Such interventions can be understood as *network structural optimization*: proactively placing high-quality nodes in strategic positions (bridging structural holes, anchoring local clusters) to enhance the collective computation's accuracy and robustness.

### 6.3 Toward Algorithmic Transparency

The threat of deceptive signals has spurred policy initiatives aiming to increase network transparency. The EU AI Act's mandatory labeling of AI-generated content, digital provenance standards, and independent algorithm auditing are all efforts to adjust the structural parameters of the social graph to favor honest signals. These represent the beginning of a societal conversation about how to govern the "computational environment" of public discourse without infringing on fundamental rights.

## 7. Conclusion

This paper has argued that a wide range of social phenomena across economics, political science, and sociology can be understood within a unified framework combining Social Network Dynamic Programming and Idea Dynamics. The framework describes society as a distributed computational system in which individuals, occupying nodes in a weighted graph, continuously process and retransmit signals based on internal cognitive mechanisms. Under conditions of algorithmic compatibility and sufficient connectivity, the network converges to stable macro-patterns that we recognize as social regularities. Convergence can be disrupted by environmental shocks, degraded by deceptive signals, or forcibly imposed by coercion.

Understanding this mechanism is not merely an academic exercise. It offers practical guidance: to influence the direction of society, one should seek to become a key node that provides genuine value to others; to protect the integrity of social computation, one must advocate for and practice transparency; and to avoid being misled, one must remain aware of the iterative nature of information and the transformations it undergoes.

The framework is not a panacea. It does not replace the rich substantive insights of individual social science disciplines, nor does it claim that all social phenomena can be reduced to network computation. But it provides a common language and a foundational model that can bridge disciplinary silos and offer actionable insights for navigating an increasingly complex and AI-mediated social world.

## References

- Bartlett, F. C. (1932). *Remembering*. Cambridge University Press.
- Berger, J., & Milkman, K. L. (2012). What makes online content viral? *Journal of Marketing Research*, 49(2), 192–205.
- Blackmore, S. (1999). *The Meme Machine*. Oxford University Press.
- Brin, S., & Page, L. (1998). The anatomy of a large-scale hypertextual Web search engine. *Computer Networks and ISDN Systems*, 30(1–7), 107–117.
- Burt, R. S. (1992). *Structural Holes: The Social Structure of Competition*. Harvard University Press.
- Dawkins, R. (1976). *The Selfish Gene*. Oxford University Press.
- Dodds, P. S., Muhamad, R., & Watts, D. J. (2003). An experimental study of search in global social networks. *Science*, 301(5634), 827–829.
- Fama, E. F. (1970). Efficient capital markets: A review of theory and empirical work. *Journal of Finance*, 25(2), 383–417.
- Granovetter, M. (1978). Threshold models of collective behavior. *American Journal of Sociology*, 83(6), 1420–1443.
- Kashima, Y. (2000). Maintaining cultural stereotypes in the serial reproduction of narratives. *Personality and Social Psychology Bulletin*, 26(5), 594–604.
- Milgram, S. (1967). The small world problem. *Psychology Today*, 1(1), 60–67.
- Nickerson, R. S. (1998). Confirmation bias: A ubiquitous phenomenon in many guises. *Review of General Psychology*, 2(2), 175–220.
- Pariser, E. (2011). *The Filter Bubble*. Penguin Press.
- Schelling, T. C. (1978). *Micromotives and Macrobehavior*. W. W. Norton.
- Sunstein, C. R. (2001). *Republic.com*. Princeton University Press.
- Vosoughi, S., Roy, D., & Aral, S. (2018). The spread of true and false news online. *Science*, 359(6380), 1146–1151.