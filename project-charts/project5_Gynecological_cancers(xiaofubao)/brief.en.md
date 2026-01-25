# Project 5: Gynecological Cancer Intelligent Assistant (Xiaofubao)

## Project Background

Gynecological cancers (including cervical cancer, endometrial cancer, ovarian cancer, etc.) are major diseases threatening women's health. Patients and their families often face difficulties in obtaining information, barriers in understanding professional knowledge, and confusion in choosing treatment plans during the diagnosis and treatment process. This project aims to provide patients with gynecological cancers with professional, timely, and understandable medical information support through AI technology.

## Cancer Type Definitions

**Gynecological Cancers primarily include:**

- **Cervical Cancer**
- **Endometrial Cancer / Uterine Cancer**
- **Ovarian Cancer**
- **Vulvar Cancer**
- **Vaginal Cancer**

> **Note**: This project recommends prioritizing the three most common gynecological cancers.

---

## Project Goals

- **Lower Information Barriers**: Explain professional medical knowledge in accessible language
- **Provide Decision Reference**: Offer diagnostic information support based on authoritative guidelines
- **Emotional Support and Companionship**: Provide 24/7 information companionship through AI assistant
- **Patient Empowerment**: Help patients better understand their condition and participate in treatment decisions

## Core Value Propositions

- **Authority**: Based on authoritative medical guidelines such as CSCO (Chinese Society of Clinical Oncology)
- **Professionalism**: Covers professional content including diagnostic recommendations, drug information, genetic testing interpretation
- **Usability**: Supports natural language dialogue, multi-platform access (WeChat, Telegram, etc.)
- **Safety**: Clear disclaimer, emphasizing auxiliary nature, does not replace professional medical consultation

---

## Target Users

### Primary Users
- Gynecological cancer patients and their families
- Women concerned about gynecological health
- Patients at different diagnostic stages (pre-diagnosis, during treatment, rehabilitation period)

### Secondary Users
- Medical staff and medical students (as auxiliary tool)
- Health education workers
- Community volunteers (Blue Vests)

---

## Product Form

**Core Architecture**: RAG AI Service + Multi-platform Bots

### Recommended Implementation Method
- **Dialogue Entry Points**: WeChat Bot / Telegram Bot / Web Page
- **Backend Service**: RAG Intelligent Q&A System
- **Knowledge Base**: Structured medical knowledge base (guidelines, drugs, genetic testing, patient experience)

### Product Innovation Space (for student team exploration)

Here are some possible innovation directions, **the team is encouraged to propose their own unique ideas**:

- **Multimodal Interaction**: Support image recognition (e.g., OCR of examination reports)?
- **Personalized Recommendations**: How to provide customized information based on user's specific situation (cancer type, stage, treatment phase)?
- **Emotional Support Function**: Besides information queries, provide psychological counseling, rehabilitation advice, etc.?
- **Community Interaction**: Connect to patient groups, promote experience sharing?
- **Multi-cancer Type Routing**: How to intelligently identify the cancer type from user queries and route to corresponding knowledge base?
- **Data Security and Privacy**: How to provide personalized services without collecting privacy?

> **Important Reminder**: Please discuss your innovative ideas with Mentor in the early stages of the project to ensure the direction is feasible and aligns with charitable intentions.

---

## Technology Stack Recommendations

### RAG System
- **Community Recommendation**: Fastgpt (Chinese-friendly, ready to use)
- **Open Source Solutions**: Dify, Ragflow (more flexible, requires some development skills)
- **Custom Solution**: If the team has technical foundation, can build based on frameworks like LangChain

### Knowledge Base Management
- **Community Recommendation**: Fastgpt / Wekora / Ragflow
- **Key Considerations**:
  - How to structure the knowledge base? (By cancer type, by diagnostic stage, by content type)
  - How to pre-process medical documents to improve retrieval accuracy?
  - Need custom chunking strategy?

### Bot Integration
- **WeChat**: Can use frameworks like WeChaty, OpenAI, etc.
- **Telegram**: python-telegram-bot
- **Web Page**: Can embed FastGPT's dialogue component or build custom interface

### Optional Plugins and Optimization
- **Embedding Optimization**: Embedding model for medical domain or preprocessing plugin
- **Multi-cancer Type Routing**: Intelligently identify user intent and route to corresponding knowledge base
- **Content Security**: Sensitive word filtering, medical compliance checking

---

## Knowledge Base Resource References

### Existing Resources (refer to xiaofubao repository)

The reference repository has completed RAG preprocessing of part of the basic knowledge base, you can:
- Understand knowledge base structure design ideas
- Refer to medical document chunking and preprocessing methods
- Learn how to organize knowledge bases for multiple cancer types

**Knowledge Base Structure Example**:
```
Knowlege_base/
├── 01_guidance/          # CSCO Clinical Guidelines
│   ├── 01_cervical_cancer/
│   ├── 02_endometrial_cancer/
│   └── 03_ovarian_cancer/
├── 02_drugs/             # Drug Information Base
├── 03_genie/             # Genetic Testing Information
└── 04_patients_expertise/ # Patient Experience Sharing
```

### What You Need to Do
- **Don't copy directly**: After understanding the structure, design your own knowledge base according to your product positioning
- **Supplement new content**: According to project needs, supplement more medical resources, patient cases, etc.
- **Optimize and innovate**: How to make the knowledge base better support your innovative features?

---

## Project Implementation Recommendations

### Phase One: Requirement Analysis and Design (1-2 weeks)
- Deeply understand target users' pain points (recommended to interview patients or family members)
- Determine core feature priorities (what should MVP include?)
- Design product interaction flow and dialogue logic
- Output: Product requirement document, interactive design prototype

### Phase Two: Knowledge Base Construction and RAG Setup (2-4 weeks)
- Collect and organize medical knowledge resources
- Perform document preprocessing and knowledge base import
- Build RAG Q&A system and test accuracy
- Output: Working RAG knowledge base, basic dialogue capability

### Phase Three: Bot Development and Integration (2-3 weeks)
- Develop WeChat/Telegram Bot or Web interface
- Integrate RAG backend service
- Implement multi-cancer type routing, dialogue management, and other functions
- Output: MVP version for external testing

### Phase Four: Testing and Optimization (2-3 weeks)
- Invite seed users (patients, family members, medical staff) to participate in testing
- Collect feedback and rapid iteration
- Improve disclaimer, privacy protection and other compliance content
- Output: Stable working product version, user manual

---

## Important Compliance Requirements

### Medical Disclaimer (Required)
- Clearly state this tool is an **information assistant**, not a medical diagnostic tool
- All treatment decisions must consult professional doctors
- Users must bear responsibility for information verification and use
- AI technology carries information bias risks

### Privacy Protection (Required)
- Comply with Personal Information Protection Law
- Do not actively collect patient privacy data (name, ID number, specific condition details, etc.)
- If any information needs to be collected, must obtain prior approval from DKU/CMC/Foundation

### Charitable Intentions (Required)
- This project is permanently free, no commercial diversion
- Do not recommend specific drugs or medical institutions
- Do not promise any therapeutic effects

---

## Recommended Success Metrics

- **Feature Completeness**: Complete core dialogue function, support knowledge Q&A for at least 2 cancer types
- **User Experience**: Seed user test feedback satisfaction ≥ 80%
- **Content Accuracy**: Pass medical expert review, key information accuracy ≥ 95%
- **Service Availability**: System runs stably, response time < 5 seconds
- **Innovation Highlights**: Implement at least 1 unique innovative feature

---

## Reference Resources

- **GitHub Repository**: https://github.com/PancrePal-xiaoyibao/xiaofubao.git
  - For learning knowledge base structure and RAG preprocessing methods
  - **Note**: Don't copy code directly, implement yourself after understanding the ideas

- **Medical Resources**:
  - CSCO Clinical Guidelines (Chinese Society of Clinical Oncology)
  - National Cancer Center related materials
  - Authoritative medical journals and databases

- **Technical Tools**: Refer to [tools_kit_101.md](../../Public_resources/tools_kit_101.md)

---

## Recommended Team Division

- **Product Manager**: Requirement analysis, user research, product design
- **RAG Engineer**: Knowledge base construction, RAG system setup and optimization
- **Frontend/Bot Developer**: Dialogue interface development, bot integration
- **Content Operations**: Medical content collection, review, and update

---

## Contact and Support

- **Mentor Guidance**: Contact your project mentor for professional advice
- **Medical Review**: Medical content must be submitted to PMC for review
- **Technical Support**: Seek help in project group or GitHub Issue when encountering technical problems
- **Reference Repository**: Can consult Sam, initiator of xiaofubao project, for experience

---

## Encouraging Words

This is a very meaningful project, your work will directly help real patients and families. Don't worry about technical barriers, the community and Mentor will support you. **Most importantly: maintain empathy for patients, start from their real needs, and create a truly useful product.**

**Let technology warm life, let information light up hope** 💝
