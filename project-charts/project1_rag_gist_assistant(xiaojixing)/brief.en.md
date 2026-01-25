# Project 1: Gastrointestinal Stromal Tumor (GIST) Intelligent Assistant (XiaoJixing)

## Project Background

Gastrointestinal Stromal Tumors (GIST) are the most common mesenchymal tumors of the gastrointestinal tract, accounting for 1%-3% of all gastrointestinal malignancies. The annual incidence is approximately (10-20)/million. With advances in pathological detection techniques, the detection rate has been gradually increasing. This disease predominantly affects middle-aged and elderly populations, with a median onset age of approximately 65 years, with no significant gender differences. Approximately 50%-70% of cases occur in the stomach, followed by the small intestine (20%-30%), with the colon, rectum, and esophagus accounting for less than 10%. The biological behavior is diverse, ranging from benign to malignant, with approximately 30% being malignant tumors. The primary metastatic sites are the liver and peritoneal cavity.

Patients and their families often face difficulties in obtaining information, barriers in understanding professional medical knowledge, and confusion in choosing treatment plans during the diagnosis and treatment process. This project aims to provide GIST patients with professional, timely, and understandable medical information support through AI technology.

## Cancer Type Definitions

**Gastrointestinal Stromal Tumor (GIST) Main Characteristics:**

- **Definition**: The most common mesenchymal tumor of the gastrointestinal tract, originating from intestinal interstitial cells (Cajal cells)
- **Primary Locations**:
  - **Stomach**: 50%-70% (most common)
  - **Small Intestine**: 20%-30% (second most common)
  - **Colon, Rectum, and Esophagus**: <10%
- **Biological Behavior**: Ranges from benign to malignant, approximately 30% are malignant tumors
- **Metastatic Sites**: Primarily liver and peritoneal cavity
- **High-Risk Population**: Middle-aged and elderly populations, median onset age approximately 65 years

> **Note**: This project recommends prioritizing the most common gastric and small intestinal GISTs, with gradual expansion to other sites.

---

## Project Goals

- **Lower Information Barriers**: Explain professional medical knowledge in accessible language to help patients understand GIST diagnosis and treatment
- **Provide Decision Reference**: Offer diagnostic information support based on authoritative guidelines
- **Emotional Support and Companionship**: Provide 24/7 information companionship through AI assistant
- **Patient Empowerment**: Help patients better understand their condition and participate in treatment decisions

## Core Value Propositions

- **Authority**: Based on NCCN, ASCO authoritative medical guidelines and latest domestic diagnosis and treatment standards
- **Professionalism**: Covers professional content including diagnostic recommendations, targeted drug information, genetic testing interpretation, post-operative rehabilitation
- **Usability**: Supports natural language dialogue, multi-platform access (WeChat, Telegram, etc.)
- **Safety**: Clear disclaimer, emphasizing auxiliary nature, does not replace professional medical consultation

---

## Target Users

### Primary Users
- GIST patients and their families
- People concerned about digestive tract health
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
- **Backend Service**: RAG Intelligent Q&A System (based on FastGPT)
- **Knowledge Base**: Structured medical knowledge base (guidelines, targeted drugs, genetic testing, patient experience)

### Product Innovation Space (for student team exploration)

Here are some possible innovation directions, **the team is encouraged to propose their own unique ideas**:

- **Multimodal Interaction**: Support image recognition (e.g., OCR of pathology reports, imaging examinations)?
- **Personalized Recommendations**: How to provide customized information based on user's specific situation (tumor location, size, risk level, treatment phase)?
- **Targeted Drug Assistant**: Provide targeted drug comparison, side effect management, and other specialized functions?
- **Rehabilitation Guidance**: Besides diagnosis and treatment information, provide post-operative rehabilitation, nutrition advice, etc.?
- **Community Interaction**: Connect to patient communities, promote experience sharing?
- **Data Security and Privacy**: How to provide personalized services without collecting privacy?

> **Important Reminder**: Please discuss your innovative ideas with Mentor in the early stages of the project to ensure the direction is feasible and aligns with charitable intentions.

---

## Technology Stack Recommendations

### RAG System
- **Community Recommendation**: FastGPT (Chinese-friendly, ready to use, closely integrated with XiaoxBao community)
- **Open Source Solutions**: Dify, Ragflow (more flexible, requires some development skills)
- **Custom Solution**: If the team has technical foundation, can build based on frameworks like LangChain

### Knowledge Base Management
- **Community Recommendation**: FastGPT / Wekora / Ragflow
- **Key Considerations**:
  - How to structure the knowledge base? (By tumor location, by diagnostic stage, by content type)
  - How to pre-process medical documents to improve retrieval accuracy?
  - Need custom chunking strategy?

### Bot Integration
- **WeChat**: Can use frameworks like WeChaty, OpenAI, etc.
- **Telegram**: python-telegram-bot
- **Web Page**: Can embed FastGPT's dialogue component or build custom interface

### Optional Plugins and Optimization
- **Embedding Optimization**: Embedding model for medical domain or preprocessing plugin
- **Multi-location Routing**: Intelligently identify user intent and route to corresponding knowledge base
- **Content Security**: Sensitive word filtering, medical compliance checking

---

## Knowledge Base Resource References

### Existing Resources (refer to XiaoxBao Community Projects)

The XiaoxBao community already has multiple oncology AI assistant projects (such as XiaoPiBao, XiaoFuBao). You can:
- Understand knowledge base structure design ideas
- Refer to medical document chunking and preprocessing methods
- Learn how to organize knowledge bases for multiple cancer types

**Knowledge Base Structure Example**:
```
Knowledge_base/
├── 01_guidance/          # Diagnosis and treatment guidelines
│   ├── 01_gastric_gist/
│   ├── 02_small_intestine_gist/
│   └── 03_other_site_gist/
├── 02_drugs/             # Targeted drug information base
├── 03_genetic/           # Genetic testing information
├── 04_surgery/           # Surgery-related information
└── 05_patients_expertise/ # Patient experience sharing
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
- Collect and organize medical knowledge resources (diagnosis and treatment guidelines, targeted drug information, etc.)
- Perform document preprocessing and knowledge base import
- Build RAG Q&A system (based on FastGPT) and test accuracy
- Output: Working RAG knowledge base, basic dialogue capability

### Phase Three: Bot Development and Integration (2-3 weeks)
- Develop WeChat/Telegram Bot or Web interface
- Integrate RAG backend service
- Implement multi-location routing, dialogue management, and other functions
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

- **Feature Completeness**: Complete core dialogue function, support knowledge Q&A for at least 2 tumor locations
- **User Experience**: Seed user test feedback satisfaction ≥ 80%
- **Content Accuracy**: Pass medical expert review, key information accuracy ≥ 95%
- **Service Availability**: System runs stably, response time < 5 seconds
- **Innovation Highlights**: Implement at least 1 unique innovative feature

---

## Reference Resources

- **GitHub Repository**: Refer to other oncology project repositories in XiaoxBao community
  - For learning knowledge base structure and RAG preprocessing methods
  - **Note**: Don't copy code directly, implement yourself after understanding the ideas

- **Medical Resources**:
  - NCCN Clinical Guidelines (GIST section)
  - ASCO Oncology Guidelines
  - National Cancer Center GIST-related materials
  - Authoritative medical journals and databases

- **Technical Tools**: Refer to [tools_kit_101.md](../../public_resources/tools_kit_101.md)

---

## Recommended Team Division

- **Product Manager**: Requirement analysis, user research, product design
- **RAG Engineer**: Knowledge base construction, FastGPT system setup and optimization
- **Frontend/Bot Developer**: Dialogue interface development, bot integration
- **Content Operations**: Medical content collection, review, and update

---

## Contact and Support

- **Mentor Guidance**: Contact your project mentor for professional advice
- **Medical Review**: Medical content must be submitted to PMC for review
- **Technical Support**: Seek help in project group or GitHub Issue when encountering technical problems
- **Reference Projects**: Can consult initiators of other XiaoxBao community projects for experience

---

## Encouraging Words

This is a very meaningful project, your work will directly help real GIST patients and families. Don't worry about technical barriers, the community and Mentor will support you. **Most importantly: maintain empathy for patients, start from their real needs, and create a truly useful product.**

**Let technology warm life, let information light up hope** 💝
