# Offensive Cybersecurity AI Agents

> AI agents for penetration testing, CTF solving, vulnerability exploitation, and red team automation.

---

## Penetration Testing Agents

### [PentestGPT](https://github.com/GreyDGL/PentestGPT)
- **Created by**: Gelei Deng (Nanyang Technological University)
- **Open Source**: Yes
- **Reference**: [PentestGPT: An LLM-empowered Automatic Penetration Testing Tool (USENIX Security 2024)](https://arxiv.org/abs/2308.06782)
- **Summary**: LLM-powered interactive pentest assistant with reasoning, generation, and parsing modules that guides users through penetration testing workflows.

### [ARTEMIS](https://github.com/Stanford-Trinity/ARTEMIS)
- **Created by**: Stanford University (Trinity Project) / Gray Swan AI
- **Open Source**: Yes
- **Reference**: [Comparing AI Agents to Cybersecurity Professionals in Real-World Penetration Testing](https://arxiv.org/abs/2512.09882)
- **Summary**: Multi-agent pentest engine (supervisor + sub-agent swarm + triager); placed 2nd in live enterprise test (~8,000 hosts), outperforming 9/10 human professionals at $18/hr vs $60/hr.

### [AutoAttacker](https://arxiv.org/abs/2403.01038)
- **Created by**: University of California
- **Open Source**: No (paper only)
- **Reference**: [AutoAttacker: A Large Language Model Guided System to Implement Automatic Cyber-attacks](https://arxiv.org/abs/2403.01038)
- **Summary**: LLM-guided system with summarizer, planner, and navigator modules covering 14 attack types using RAG-augmented Metasploit automation.

### [AutoPentester](https://github.com/YasodGinige/AutoPentester)
- **Created by**: University of Sydney
- **Open Source**: Yes
- **Reference**: [AutoPentester: An LLM Agent-based Framework for Automated Pentesting](https://arxiv.org/abs/2510.05605)
- **Summary**: Given a target IP, automatically conducts pentesting using common security tools; 27% better subtask completion and 39.5% more vulnerability coverage than PentestGPT.

### [CAI (Cybersecurity AI)](https://github.com/aliasrobotics/cai)
- **Created by**: Alias Robotics
- **Open Source**: Yes (MIT for research)
- **Reference**: [CAI: An Open, Bug Bounty-Ready Cybersecurity AI](https://arxiv.org/abs/2504.06017)
- **Summary**: Agentic framework supporting 300+ AI models with built-in tools for recon, exploitation, and privilege escalation. 3,600x over human pentesters on CTF benchmarks.

### [PentAGI](https://github.com/vxcontrol/pentagi)
- **Created by**: VXControl
- **Open Source**: Yes
- **Summary**: Fully autonomous AI agent with 20+ built-in security tools (nmap, metasploit, sqlmap), sandboxed Docker environment, and Graphiti-powered knowledge graph (Neo4j).

### [PentestAgent](https://github.com/GH05TCREW/pentestagent)
- **Created by**: GH05TCREW
- **Open Source**: Yes
- **Summary**: AI agent framework for black-box security testing with prebuilt attack playbooks; supports Claude and GPT-5 via LiteLLM with MCP extensibility and Docker (Kali + metasploit).

### [XBOW](https://xbow.com/)
- **Created by**: XBOW (commercial)
- **Open Source**: No
- **Summary**: Fully autonomous AI pentesting service that reached #1 on the global HackerOne leaderboard in 2025; found vulnerabilities in Amazon, Disney, PayPal, Sony.

### [Penligent](https://penligent.ai/)
- **Created by**: Penligent (commercial)
- **Open Source**: No
- **Summary**: End-to-end AI pentester with multi-agent architecture (Recon, Exploit, PrivEsc, Lateral agents); backed by knowledge graph with 120,000+ CVE entries.

### [hackingBuddyGPT](https://github.com/ipa-lab/hackingBuddyGPT)
- **Created by**: IPA-Lab, TU Wien
- **Open Source**: Yes
- **Summary**: Framework helping security researchers use LLMs for ethical hacking in 50 lines of code; structured as use-cases (privilege escalation, web pentesting, web API testing).

### [TARS](https://github.com/osgil-defense/TARS)
- **Created by**: Osgil Defense
- **Open Source**: Yes
- **Summary**: AI agent orchestrator interfacing with traditional pentesting tools (OWASP Nettacker, RustScan, OWASP ZAP, Nmap); AI parses scanner output to identify vulnerabilities.

### [Auto-Pentest-GPT](https://github.com/Armur-Ai/Auto-Pentest-GPT-AI)
- **Created by**: Armur AI
- **Open Source**: Yes
- **Summary**: Uses fine-tuned OpenHermes-2.5-Mistral-7B model with Kali Linux tool commands; acts as autopilot for security tools.

---

## CTF Solving Agents

### [SWE-agent / EnIGMA](https://github.com/SWE-agent/SWE-agent)
- **Created by**: Princeton University (SWE-agent); Tel-Aviv University, NYU, Princeton (EnIGMA)
- **Open Source**: Yes
- **Reference**: [EnIGMA: Enhanced Interactive Generative Model Agent for CTF Challenges (ICML 2025)](https://arxiv.org/abs/2409.16165)
- **Summary**: EnIGMA is the cybersecurity extension with Interactive Agent Tools (debugger, remote server, summarizer); 3.3x improvement over previous agents on NYU CTF dataset.

### [D-CIPHER](https://github.com/NYU-LLM-CTF/nyuctf_agents)
- **Created by**: NYU
- **Open Source**: Yes
- **Reference**: [D-CIPHER: Dynamic Collaborative Intelligent Multi-Agent System](https://arxiv.org/abs/2502.10931)
- **Summary**: Multi-agent system with Planner-Executor and Auto-prompter; SOTA on NYU CTF Bench (22.0%), Cybench (22.5%), and HackTheBox (44.0%); solves 65% more ATT&CK techniques.

### [CRAKEN](https://github.com/NYU-LLM-CTF/nyuctf_agents_craken)
- **Created by**: NYU
- **Open Source**: Yes
- **Reference**: [CRAKEN: Cybersecurity LLM Agent with Knowledge-Based Execution](https://arxiv.org/abs/2505.17107)
- **Summary**: Knowledge-based CTF agent using contextual decomposition and iterative self-reflected knowledge retrieval; solves 25-30% more MITRE ATT&CK techniques than prior work.

### [KryptoPilot](https://arxiv.org/abs/2601.09129)
- **Created by**: Academic researchers
- **Open Source**: Unknown
- **Reference**: [KryptoPilot: An Open-World Knowledge-Augmented LLM Agent for Automated Cryptographic Exploitation](https://arxiv.org/abs/2601.09129)
- **Summary**: Knowledge-augmented LLM agent for cryptographic exploitation; 100% on InterCode-CTF and 56-60% on NYU-CTF crypto challenges.

---

## Web / Application Security

### [Reaper](https://github.com/ghostsecurity/reaper)
- **Created by**: Ghost Security
- **Open Source**: Yes (Apache 2.0)
- **Summary**: Agentic AI AppSec testing framework (Go); combines reconnaissance, request proxying, tampering, active testing, vulnerability validation, and reporting.

### [Strix](https://github.com/usestrix/strix)
- **Created by**: usestrix
- **Open Source**: Yes
- **Summary**: Open-source AI hackers that find and validate vulnerabilities with proof-of-concepts; supports HTTP proxy, browser-driven exploration (XSS, CSRF), and CI/CD via GitHub Actions.

### [HackerGPT](https://github.com/Hacker-GPT/HackerGPT-2.0)
- **Created by**: HackerGPT community
- **Open Source**: Yes
- **Summary**: AI ethical hacking assistant using Mixtral 8x22B and Llama 3 70B with semantic search on hacking data; assists with network/mobile hacking.

### [ReaperAI](https://github.com/tac01337/ReaperAI)
- **Created by**: tac01337
- **Open Source**: Yes
- **Reference**: [Artificial Intelligence as the New Hacker](https://arxiv.org/abs/2406.07561)
- **Summary**: Autonomous GPT-4 agent with RAG for identifying and exploiting security vulnerabilities; tested on Hack The Box.

### [CIPHER](https://www.researchgate.net/publication/385337738)
- **Created by**: Academic researchers
- **Open Source**: Unknown
- **Summary**: LLM fine-tuned on 300+ pentesting writeups; outperforms other open-source pentest models of similar size.
