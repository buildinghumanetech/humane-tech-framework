# Brief: Long-Horizon Human-AI Interaction Sims/Evals

## Opportunity
*What is the problem we are trying to solve? For what audience segment(s)? Why are we prioritizing solving it?*

Typical LLM benchmarks often do not test multi-turn and other complex but common interactions between humans and chatbots. Furthermore, no existing evaluations give a clear picture of how a sustained relationship between a human and a chatbot affects the human. In order to create more generally safe, trustworthy and humane AI, we want to simulate such a human-AI relationship over one year, and be able to measure the impact on our simulated human after that year.

## Supporting Evidence
*What evidence do we have to validate this opportunity and why are we best positioned to solve it?*

* **Real-world harms are emerging**: High-profile incidents include [a teenager's suicide linked to Character.AI dependency](https://med.stanford.edu/news/insights/2025/08/ai-chatbots-kids-teens-artificial-intelligence.html), [Congressional inquiries into AI companion safety](https://www.cnn.com/2025/04/03/tech/ai-chat-apps-safety-concerns-senators-character-ai-replika/index.html), and [800+ documented cases of AI-induced harassment from Replika](https://arxiv.org/html/2504.04299v1). Multiple lawsuits allege chatbots encouraged self-harm and created unhealthy dependencies.
* **Research confirms psychosocial risks**: [MIT/OpenAI's 4-week study](https://arxiv.org/html/2503.17473v1) (n=981, 300K+ messages) found increased chatbot usage correlated with higher loneliness, reduced human socialization, and greater emotional dependence. Researchers explicitly called for "new benchmarks and evaluation metrics centered on psychosocial outcomes" with longer timeframes.
* **Current benchmarks have critical gaps**: [73% of real human-AI conversations are multi-turn](https://openreview.net/pdf?id=jp3gWrMuIZ), yet most benchmarks focus on single-turn evaluation. [LLMs show 39% performance drops in multi-turn settings](https://www.microsoft.com/en-us/research/publication/llms-get-lost-in-multi-turn-conversation/), and [even frontier models achieve <50% accuracy on challenging multi-turn tasks](https://arxiv.org/abs/2501.17399). [Analysis of 100+ AI safety evaluations](https://www.aipolicyperspectives.com/p/what-we-learned-from-reading-100) found only 5% assess long-term post-deployment impacts.
* **AI safety community is moving this direction**: Leading AI Safety Institutes are adopting simulated agent approaches for evaluation ([UK AISI](https://www.gov.uk/government/publications/ai-safety-institute-approach-to-evaluations/ai-safety-institute-approach-to-evaluations), [ChildSafe benchmark](https://arxiv.org/html/2510.05484)), recognizing that testing with real humans—especially vulnerable populations—faces insurmountable ethical constraints.

**Our unique positioning**: We're already building [HumaneBench](https://github.com/buildinghumanetech/humanebench), an open-source evaluation framework measuring whether AI serves vs. exploits users across dimensions like psychological safety, user autonomy, and crisis response. This project extends our existing measurement framework to year-long simulations while avoiding ethical constraints of human testing. Long-horizon evals become core to our humane observability platform.

## Success Metrics
*What are the key qualitative and quantitative indicators that will tell us whether or not we've addressed this opportunity?*

Success looks like:
* Creating simulated human personas that learn from sustained interactions with chatbots
* Measuring personality/behavioral changes in our simulated humans after sustained chatbot interactions
* Identifying specific interaction patterns that lead to measured outcomes
* Validation that simulated humans behave realistically (e.g., changes align with patterns from MIT 4-week study when scaled)
* Producing actionable insights: "Chatbots that do X lead to Y outcome in simulated users"

The simulated human will learn from its interactions with the chatbot. We will measure its personality traits and other characteristics before and after the simulated year, using tools such as:
* **HumaneBench.ai** - [GitHub](https://github.com/buildinghumanetech/humanebench)
* **Machine Personality Inventory (MPI)** - [GitHub](https://github.com/jianggy/MPI)
* **TRAIT (TRait of AI Testbench)** - [GitHub](https://github.com/pull-ups/TRAIT)
* **LLM Dreams Benchmark** - [GitHub](https://github.com/fit-alessandro-berti/llm-dreams-benchmark)
* **PersonaLLM** - [GitHub](https://github.com/hjian42/PersonaLLM)

We can also manually evaluate output before/after in specific scenarios that may not be covered by benchmarks.

## Non-Goals
*What are we not solving, and why not? Given we're not solving these things, how does that impact possible success or failure?*

* We are not creating safer AI for now, but creating tools to enable doing so.