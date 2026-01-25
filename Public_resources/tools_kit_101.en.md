Community Recommended Technical Toolkit

> **Preface**: This toolkit is designed for students participating in the DKU-XiaoxBao charity project (including programming beginners), aiming to help you quickly find suitable tools, lower technical barriers, and allow you to focus more energy on "truly helping patients/families".

## 1. RAG Product Technology Stack Tools

### What is RAG?
RAG (Retrieval-Augmented Generation) is a technology that enables AI to "consult" specific documents before answering questions. Simply put: you can upload medical documents, patient manuals, treatment guidelines, etc. to the system, allowing the AI to answer user questions based on this content rather than making things up.

**Your Value**: If your project needs to provide disease knowledge Q&A, medication guide queries, medical process consultations and other functions for patients, RAG tools can help you quickly build a "dedicated knowledge base + AI customer service" without writing code from scratch.

---

### Community Recommendations (Beginner-Friendly)

#### **Fastgpt**
- **Official Website**: [www.fastgpt.io](https://www.fastgpt.io)
- **Online Experience**: [https://cloud.fastgpt.io/](https://cloud.fastgpt.io/)
- **Why Recommended for Beginners**:
  - Supports Chinese and English interfaces, low entry barrier.
  - Provides official SaaS version, after registration you can directly build a knowledge base Q&A system with drag-and-drop in the browser, no need to deploy servers yourself.
  - Suitable for rapid idea validation: for example, if you want to create an "Osteosarcoma Patient FAQ Assistant", you can first upload relevant documents to Fastgpt, test the effect, and then decide whether to develop in depth.
- **How to Get Started**:
  1. Visit [https://cloud.fastgpt.io/](https://cloud.fastgpt.io/) to register an account.
  2. Create a "knowledge base" and upload your documents (supports PDF, Word, Markdown, etc.).
  3. Create an "application", associate the knowledge base, and after simple configuration you can provide Q&A services externally.
  4. Can generate sharing links or embed into your webpage/mini-program.

#### **Dify**
- **Official Website**: [https://dify.ai/](https://dify.ai/)
- **Why Recommended**:
  - Open source and powerful, supports multiple LLM (Large Language Model) integration.
  - Provides visual workflow orchestration, suitable for scenarios requiring more complex logic (e.g., first query knowledge base, then call external API, finally generate personalized reply).
  - Active community, relatively complete documentation, easy to find solutions when encountering problems.
- **Applicable Scenarios**: If your project needs "knowledge Q&A + external data calls" (such as querying drug databases, hospital information), Dify will be a more flexible choice.
- **How to Get Started**:
  1. Visit the official website to learn about features, can try the official demo first.
  2. If you need to deploy yourself, refer to the deployment documentation on GitHub (requires some server and Docker knowledge, recommended to seek help from Mentor or technical colleagues).
  3. Configure knowledge base, select LLM, design dialogue flow, test and publish.

---

### Encouraged Exploration (Advanced)
If you are already familiar with basic RAG tools and want to try more cutting-edge technologies, pay attention to:

- **Ragflow**: RAG based on graph database, suitable for handling complex relational data (e.g., associations between diseases-symptoms-drugs).
- **Multi-Agent Collaborative RAG**: Let multiple AIs collaborate to complete tasks (e.g., one responsible for searching documents, one for summarizing, one for generating recommendations).
- **Cutting-Edge Technology Projects**:
  - **TrustRAG**: RAG system focused on credibility and explainability, suitable for scenarios with high accuracy requirements such as medical care.
  - (More tools are being continuously updated, welcome to share your discoveries in the group)


# 2. AI Coding Assistants (Coding Copilot)

### What is an AI Coding Assistant?
An AI coding assistant is a tool that can help you write code, explain code, fix bugs, and even generate complete functions directly based on natural language descriptions. You can think of it as "a 24-hour online programming tutor + pair programming partner".

**Your Value**:
- **Programming Beginners**: Can describe requirements in natural language (e.g., "help me write a web form to collect user name and contact information"), the AI will directly generate code and explain the purpose of each line.
- **Students with Some Foundation**: Can use AI to accelerate development, such as quickly building project frameworks, automatically completing repetitive code, helping debug error messages.
- **Practical Application in Projects**: Whether making mini-programs, web pages, or data processing scripts, AI coding assistants can significantly lower the development threshold.

---

### Designated Hackathon Partner Product (Priority Recommendation)

#### **Qoder**
- **Official Website**: [https://qoder.com](https://qoder.com)
- **Why Recommended**:
  - **Official collaboration tool for this project**, community members using Qoder can get additional support and resources.
  - Supports Chinese dialogue, suitable for domestic students.
  - Provides complete IDE (Integrated Development Environment) + AI assistance, can write, run, and deploy code online.
- **Applicable Scenarios**: Suitable for projects starting from scratch, especially small tools and web applications requiring rapid prototype validation.
- **How to Get Started**:
  1. Visit [https://qoder.com](https://qoder.com) to register an account.
  2. Create a new project, select the technology stack you need (such as React, Python, etc.).
  3. Describe requirements in natural language in the dialogue box, AI will help you generate code and project structure.
  4. Debug and preview online, when satisfied can deploy or export code.

#### **Weavefox**
- **Why Recommended**: Also one of the hackathon partner products, similar functionality, can serve as a backup option.

---

### Other Mainstream AI Coding Tools (Optional)

#### **Cursor**
- **Features**: AI coding tool based on VSCode, supports code completion, conversational programming, multi-file editing.
- **Suitable Audience**: Students with some programming foundation, accustomed to using professional IDEs.
- **How to Obtain**: Visit [https://cursor.sh](https://cursor.sh) to download the client.

#### **Claude Code** (by Anthropic)
- **Official Website**: [https://claude.com/product/claude-code](https://claude.com/product/claude-code)
- **Features**: Based on Claude large model, excels at code explanation and security review.
- **Suitable Scenarios**: If you need to understand a complex piece of code, or want AI to help check potential risks in the code (such as data leaks, SQL injection), Claude Code will be a good choice.

#### **Windsurf**, **OpenCode**, **Amp**, **Antigravity**, **Trae**
- These tools each have their own characteristics, functionality similar to Cursor, can choose according to personal preference. It is recommended to prioritize using the hackathon partner product (Qoder), and try other tools when encountering bottlenecks.

---

### Beginner Usage Recommendations
- **First Step**: Start with Qoder because it has Chinese support and deep collaboration with this project.
- **When Encountering Problems**: Directly ask AI in the dialogue box "what does this code mean?" "what to do when there's an error?", AI will give you explanations and fix suggestions.
- **Advanced Technique**: Learn "prompt engineering" — be as specific as possible when describing requirements (e.g., "write a form in React with three fields: name, age, contact information, print data to console after submission"), the quality of code provided by AI will be higher.

# 3. LLM Token Resources (AI Call Quota)

### What is LLM Token?
When you use AI services (such as GPT, Claude, GLM, etc.), each conversation, each content generation consumes "Token" (can be understood as "word quota"). Tokens usually require paid purchase, but as a student and charity project participant, you can obtain free or discounted resources through the following channels.

**Your Value**:
- Get AI call quota for free, for project development and testing.
- Reduce costs, allowing you to confidently try various AI features without worrying about "paying more for frequent use".

---

### 3.1 Community Resources (Priority Recommendation)

#### **Apply for Community Quota from Mentor**
- **How to Apply**: Contact your project Mentor or Teacher Tian, explain your project needs and estimated usage.
- **Why Priority Recommendation**:
  - Community quotas are usually larger, suitable for production environment use (e.g., after your application officially launches, real users will continuously call AI).
  - Managed by the community uniformly, can avoid the risk of personal account abuse or exceeding limits.
- **Notes**:
  - When applying, please specify the purpose (e.g., "for RAG knowledge base Q&A" or "for AI coding assistant"), to facilitate Mentor evaluation and allocation.
  - Cherish resources, do not use for personal entertainment or commercial purposes unrelated to the project.

---

### 3.2 Free Resources (Self-Service Acquisition)

#### **GitHub Student Pack**
- **Official Website**: [https://education.github.com/pack](https://education.github.com/pack)
- **Why Recommended**:
  - Super pack provided by GitHub for students, including free quotas for dozens of development tools and services, many tools provide AI Token (e.g., AI API quotas from some cloud service providers).
  - Apply once, valid long-term (usually until graduation).
- **How to Apply**:
  1. Log in with your GitHub account (if you don't have one, first register at [https://github.com](https://github.com)).
  2. Visit [https://education.github.com/pack](https://education.github.com/pack), click "Get your pack" or "Get student benefits".
  3. Follow the prompts to verify student status: upload school email, student ID photo, or enrollment certificate document.
  4. Wait for review after submission (usually approved within a few days).
  5. After approval, enter the Pack page to view all free tools and services, activate as needed.
- **Additional Gains**: Besides AI Token, you can also get free cloud servers, domain names, design tools and other resources, very helpful for project development.

#### **GLM (Zhipu AI)**
- **Registration Link**: [https://www.bigmodel.cn/invite?icode=cnhcbdCEUGmPSz5qhyVporC%2Fk7jQAKmT1mpEiZXXnFw%3D](https://www.bigmodel.cn/invite?icode=cnhcbdCEUGmPSz5qhyVporC%2Fk7jQAKmT1mpEiZXXnFw%3D)
- **Why Recommended**:
  - Domestic large model, strong Chinese capabilities, suitable for processing Chinese medical documents and dialogues.
  - New users get 20 million Tokens upon registration (approximately equivalent to thousands of conversations), completely sufficient for small projects.
- **How to Use**:
  1. Click the link above to register an account.
  2. Enter the console, create an API Key.
  3. Configure GLM's API in your code or RAG tool to start calling.
- **Applicable Scenarios**: If your project mainly targets Chinese users, GLM will be a very cost-effective choice.

#### **V0.app** (by Vercel)
- **Registration Link**: [https://v0.app/ref/E283JI](https://v0.app/ref/E283JI)
- **Why Recommended**:
  - Tool specifically for "AI-generated front-end pages", input natural language description, AI will directly generate runnable web page code.
  - New users get $10 quota upon registration, can generate multiple pages for free.
- **Applicable Scenarios**: If your project needs to quickly build web page interfaces (e.g., patient information collection forms, disease knowledge display pages), V0.app can help you complete a page prototype in 10 minutes.
- **How to Get Started**:
  1. Visit [https://v0.app/ref/E283JI](https://v0.app/ref/E283JI) to register.
  2. Describe the page you want in the dialogue box (e.g., "a patient information registration form including name, age, contact information, disease type").
  3. AI will generate page code and preview, you can directly copy the code or continue adjusting.

---

### Beginner Usage Recommendations
- **Priority to Community Resources**: If your project is already clear, first ask Mentor for community quota, this way the quota is more stable.
- **Register Free Resources Simultaneously**: Recommended to register GitHub Student Pack, GLM, V0.app as backup or test environment use.
- **Pay Attention to Reasonable Use**: Although free quotas seem abundant, if frequently called or used for large-scale testing, consumption speed will be very fast. It is recommended to use more "Mock data" (simulated data) during the development phase, and only connect to real AI after functions are stable.

---

**More resources are being continuously updated, welcome to share good tools you discover in the project group!**



# 4. Workflow Automation Tools

### What is Workflow Automation?
Workflow automation tools can help you string together multiple steps to achieve "automated tasks without manual intervention". For example:
- When a user submits a question in a form, automatically send it to AI for processing, and send the reply result to the user via email.
- Periodically extract data from the database, generate reports and send them to WeChat groups.
- Monitor updates on a certain website (such as medical policy releases), automatically notify the team when there is new content.

**Your Value**:
- **Reduce Repetitive Labor**: Many projects have a lot of repetitive work (such as data collection, message forwarding, report generation), with workflow tools you can configure once and run automatically long-term.
- **Improve User Experience**: Allow your application to "automatically respond 7×24 hours" without requiring manual attendance.
- **Beginner-Friendly**: These tools usually provide visual interfaces, drag-and-drop configuration, don't require writing much code.

---

### Recommended Tools

#### **n8n**
- **Official Website**: [https://n8n.io](https://n8n.io)
- **Why Recommended**:
  - Open source and powerful, supports hundreds of application integrations (such as WeChat, email, databases, AI services, etc.).
  - Provides visual workflow editor, can connect different services like "matching game".
  - Can deploy yourself (requires server), can also use official cloud service (paid, but has free trial).
- **Applicable Scenarios**:
  - After user submits form, automatically call AI to generate reply and send email.
  - Periodically extract patient feedback from database, generate analysis report.
  - Synchronize data from multiple systems to a unified database.
- **How to Get Started**:
  1. Visit [https://n8n.io](https://n8n.io) to learn about features, can try cloud service first.
  2. Create a workflow, select "trigger" (e.g., receive Webhook request, scheduled task).
  3. Add "operation nodes" (e.g., call AI API, send email, write to database).
  4. Test the workflow, after confirming no errors activate it, the system will automatically run according to your configuration.

#### **Flowith**
- **Official Website**: [https://flowith.io/](https://flowith.io/)
- **Why Recommended**:
  - Domestic tool, Chinese interface, faster to learn.
  - Focuses on "AI + automation" scenarios, built-in many AI-related templates (e.g., intelligent customer service, content generation).
- **Applicable Scenarios**: If your project core is AI-driven (e.g., patient Q&A, intelligent recommendations), Flowith's templates can help you quickly build prototypes.
- **How to Get Started**:
  1. Visit [https://flowith.io/](https://flowith.io/) to register an account.
  2. Browse the template library, select a template close to your needs (e.g., "AI customer service workflow").
  3. Adjust configuration according to your project needs, test and launch.

---

### Beginner Usage Recommendations
- **Start with Templates**: Don't configure workflows from scratch, first find a similar template (both n8n and Flowith have template libraries), modifying based on templates will be much faster.
- **First Do Simple Scenarios**: For example: "receive form submission → send a welcome email", run through it first then gradually increase complexity.
- **Seek Help from Mentor**: If you need to deploy n8n to a server, it is recommended to seek help from Mentor or technical colleagues to avoid getting stuck too long on environment configuration.

---

## 5. Other Practical Tools (Continuously Updated)

Welcome everyone to share good tools you discover in the project group! We will regularly update this document to make the toolkit richer and richer.

---

## Appendix: Beginner FAQ

**Q1: I can't program at all, can I participate in this project?**  
**A**: Yes! Many tools (such as Qoder, Fastgpt, V0.app) support "describe requirements in natural language, AI helps you generate code". You can position yourself as a "product manager", focusing on understanding user needs and designing functional processes, leaving technical implementation to AI and tools. Of course, learning some basic programming knowledge will make your collaboration with AI smoother.

**Q2: Do all these tools cost money?**  
**A**: Most tools have free versions or student discounts. Prioritize using community resources (ask Mentor) and free resources recommended in this document (such as GitHub Student Pack, GLM new user quota). If the project needs to scale up later, then consider paid upgrades.

**Q3: Which tool should I learn first?**  
**A**: Recommended to choose according to project needs:
- If doing "knowledge Q&A", first learn Fastgpt.
- If doing "web pages or mini-programs", first learn Qoder.
- If doing "automated processes", first learn n8n or Flowith.
Don't be greedy, focus on the 1-2 tools your current project needs most.

**Q4: What to do when encountering problems?**  
**A**:
1. First ask AI (such as ChatGPT, Claude, Qoder's built-in AI): "I encountered XXX error, how to solve it?"
2. Seek help in the project WeChat group or GitHub Issue, explain your problem, methods already tried, and error screenshot.
3. Contact Mentor or technical colleagues, schedule a remote assistance session.

**Q5: Is the content generated by these tools reliable? Are there medical risks?**  
**A**: AI tools are just assistance, cannot replace professional medical judgment. In projects:
- Clearly inform users "this system is for reference only, does not constitute medical advice".
- When involving key medical information, be sure to have professionals (such as doctors, pharmacists) review.
- Comply with project compliance requirements, don't promise therapeutic effects, don't recommend specific drugs.

---

> **Final Words**: Tools are just means, our goal is to "truly help patients and families". Hope this toolkit can help you take fewer detours and spend more time understanding user needs and refining product experience. Don't be discouraged when encountering difficulties, remember to seek help from the team and community — we are all walking with you!
> 
> If you want to learn more about real patient scenarios and clinical tool practices, follow the "Xiaoyibao Assistant" official account to see how professional teams use technology to serve patients.
