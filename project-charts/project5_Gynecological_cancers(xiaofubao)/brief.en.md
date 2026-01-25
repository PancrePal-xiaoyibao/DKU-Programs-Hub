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

Based on **real gynecological cancer patient pain points**, here are innovation directions grounded in clinical needs and leveraging AI Coding Skill ecosystem:

#### **Innovation Scenario 1: Multi-Channel Patient Information Integration & Smart Reminder System**

**Patient Pain Points**:
- Gynecological cancer patients need to manage multiple hospital appointments, chemotherapy/radiotherapy schedules, medication times, and follow-up dates
- **Information fragmentation**: Hospital apps, WeChat, SMS, paper appointment cards, medical records scattered across systems
- **Easy to miss critical events**: Forget medication → abnormal blood counts; miss follow-up → treatment delay; missed lab collection → inaccurate assessment
- **Family members lack visibility**: Spouses/children need real-time patient status but cannot see unified information view

**Innovation Implementation**:
- **Multi-source data aggregation**: Hospital EHR + pharmacy systems + insurance platforms + patient manual input
- **Unified patient timeline**: Treatment calendar, medication schedule, test checklist, key milestones
- **Context-aware smart reminders**: 
  - Not just "Take medication tomorrow"
  - Instead: "Tomorrow 8:00 AM, take nausea medication with warm water after breakfast; expect side effects: dizziness (manageable with rest)"
  - Route-aware: "Chemotherapy tomorrow at 2:00 PM at Hospital X, 45-minute drive from home, parking available, bring insurance card"
- **Family access with privacy control**: Patient controls what information family members can see (full vs. summary view)
- **Compliance monitoring**: Track medication adherence, identify at-risk patients 3-5 days before problems emerge
- **Wearable integration**: Optional: Connect to Apple Watch/Fitbit to monitor vital signs between hospital visits

**Expected Impact**: 
- Treatment adherence ↑85% (from forgetfulness)
- Doctor early risk detection 3-5 days ahead (prevent hospitalization)
- Reduced treatment interruptions and complications
- Decreased family caregiver anxiety

**AI Coding Skills to Leverage**:
- Hospital-EHR connector, pharmacy-integration, insurance-data-connector
- n8n-wechat-automation for smart reminders
- Sequential-thinking for dependency awareness (e.g., "need blood test before chemo dose adjustment")

---

#### **Innovation Scenario 2: Personalized Treatment Plan Explanation & Decision Support System**

**Patient Pain Points**:
- **Lack of understanding**: "Why did doctor choose chemotherapy + radiotherapy instead of immunotherapy alone?" - Cannot see decision logic
- **Multi-center confusion**: Seek second opinions → Hospital A recommends Plan A, Hospital B recommends Plan B → Patient paralyzed by conflicting advice
- **Anxiety from delayed information**: CT/MRI scan today → results in 1-2 weeks → 14 days of uncertainty and worst-case thinking
- **Cost opacity**: "How much will my entire treatment cost? What does insurance cover?" - Leads to treatment abandonment or financial hardship

**Innovation Implementation**:
- **Multi-option treatment comparison**: Generate 3-5 treatment schemes (chemotherapy, immunotherapy, combination, radiotherapy, targeted therapy) with:
  - Efficacy rate %, median overall survival, progression-free survival curves
  - Side effect profiles and severity likelihood
  - Cost breakdown (drug cost, administration, monitoring, supportive care)
  - Insurance coverage estimate, out-of-pocket cost
  
- **Guideline-based personalized recommendations**: 
  - Start with NCCN/ESMO/CSCO base recommendations for patient's cancer type/stage
  - Adjust based on patient factors (age, kidney function, cardiac function, performance status, genetic mutations)
  - Incorporate "real-world evidence": "Patients similar to you chose Plan A (52%) vs Plan B (48%); outcomes were..."
  
- **Patient-friendly explanation**: Medical terms → plain language with visual aids
  - Instead of: "EGFR-positive NSCLC with exon 19 deletion"
  - Say: "Your lung cancer has a particular genetic change that responds well to targeted drugs; response rate is 70%"
  
- **AI-assisted result interpretation** (optional but valuable):
  - Upload CT/MRI → AI model gives preliminary assessment within 30 minutes (no need to wait for radiologist)
  - Shows tumor size change, new lesions, confidence score
  - Reduces anxiety from waiting
  
- **Cost transparency and planning**:
  - Itemized cost breakdown by treatment phase
  - Insurance coverage simulation: "If insurance covers 70%, your out-of-pocket = 30万 over 6 months"
  - Financial aid resources and options

**Expected Impact**: 
- Patients understand treatment rationale → increased treatment commitment and compliance
- Doctors save 30% decision-making time (auto-generated comparison)
- Reduced anxiety from multi-center consultation conflicts (see what evidence base supports each option)
- Patients make informed cost decisions, reduce treatment abandonment
- Real-world evidence data accumulates for future guideline improvements

**AI Coding Skills to Leverage**:
- jina-ai-mcp for deep text understanding of medical literature
- sequential-thinking for multi-angle reasoning about treatment options
- image-ai-analysis for automatic CT/MRI interpretation
- cost-tracking-and-projection skills
- multi-center-mcp for anonymized patient outcome sharing

---

#### **Innovation Scenario 3: Real-Time Treatment Side-Effects Monitoring & Intelligent Alert System**

**Patient Pain Points**:
- Gynecological cancer treatments cause frequent, serious side effects (bone marrow suppression, nausea, diarrhea, fatigue, cardiac toxicity, neuropathy)
- **Silent onset**: Serious side effects develop gradually; patients cannot detect early warning signs
- **Delayed intervention**: Patient discovers problem → contacts doctor → waits for appointment → receives care. By then, condition may be severe.
- **Passive management**: Patient hopes side effects go away; medical team is reactive, not proactive
- **No continuous monitoring**: Only data points are at clinic visits (1-2 weeks apart); what happens in between is invisible

**Innovation Implementation**:
- **Multi-source real-time data ingestion**:
  - Wearable devices: Heart rate, body temperature, sleep duration/quality, activity level, step count
  - Patient-reported outcomes (PRO): Daily 2-minute check-in on symptom severity (nausea, fatigue, pain, appetite, mood)
  - Hospital systems: Automatic lab data push (CBC, liver function, kidney function, cardiac markers) when tests are done
  
- **AI toxicity prediction model**:
  - Machine learning model trained on clinical trial data and real-world evidence
  - Predicts 24-48 hour side-effect risk based on wearable + PRO + lab data
  - Outputs: Risk score (0-100), risk level (Low/Medium/High), confidence score
  - Accuracy >90% sensitivity, >85% specificity (minimize false alarms)
  
- **Risk stratification and smart interventions**:
  - **High risk**: Instant alert to patient (WeChat notification with guidance) + alert to doctor. Recommend urgent hospital visit.
  - **Medium risk**: Alert to patient with home management recommendations + follow-up PRO check-in next day
  - **Low risk**: Summary in daily report, monitor continuously
  
- **Clinical decision support for doctors**:
  - Dashboard showing: Patient risk heatmap, trend analysis, recommended dose adjustment or supportive therapy
  - Example: If bone marrow suppression risk rising → suggest G-CSF prophylaxis; if cardiotoxicity risk rising → refer to cardiology
  
- **Feedback loop for model improvement**:
  - Patient validates prediction outcome: "Did the predicted side effect actually occur? How severe was it?"
  - Use validation data to continuously retrain and improve model

**Example Metrics and Thresholds**:

| Side Effect | Monitoring Indicators | Data Source | Alert Threshold | Intervention |
|-------------|-------------------|-------------|-----------------|--------------|
| Bone marrow suppression | WBC count, hemoglobin, platelets | Lab auto-push | WBC<2000 or Plt<50,000 | Doctor alert, possible dose reduction, G-CSF consideration |
| Nausea/vomiting | Daily symptom score, food intake, weight | PRO check-in + wearable activity | Score>3 or weight↓3% in 1 week | Antiemetic escalation, nutrition consultation |
| Cardiac toxicity | Heart rate variability, activity level | Wearable sensors | Abnormal HRV pattern or ejection fraction imaging | Cardiology referral, troponin monitoring |
| Fatigue | Activity level drop, sleep quality | Wearable tracking | Activity↓>30% in 7 days OR sleep<5 hours/night | Exercise prescription, energy management coaching, anemia check |
| Neuropathy | Pain score, hand/foot sensitivity | Daily PRO | Symptoms interfering with ADL | Dose delay, nerve support therapy, physical therapy |

**Expected Impact**: 
- Early detection 24-48 hours before symptoms become severe
- Reduce serious complications by 65-80% (through proactive intervention)
- From passive "hope it goes away" → active real-time monitoring
- Better dose optimization through continuous data feedback
- Improved quality of life (faster symptom management)
- Real-world data accumulation for future toxicity models

**AI Coding Skills to Leverage**:
- wearable-data-integration (Apple Health, Fitbit, hospital devices)
- patient-reported-outcomes (PRO) framework
- hospital-data-connector for lab result auto-ingestion
- sequential-thinking for root cause analysis ("Why is WBC dropping? Chemotherapy cumulative effect? Infection? Bone marrow fibrosis?")
- radiotherapy-toxicity-predictor or similar models
- n8n-wechat-automation for real-time alerts
- doctor-dashboard-generator for clinical decision support

---

#### **Additional Innovation Directions** (encourage team creativity)

- **Multimodal Interaction**: OCR of pathology/lab reports + voice input for hands-free queries during treatment
- **Emotional Support**: Psychological assessment + coping strategy recommendations + mental health resources + peer support matching
- **Community Features**: Peer support groups by cancer type/treatment stage, experience sharing database, buddy matching
- **Genomic Integration**: Interpretation of gene testing results (BRCA, MSI, TMB) + precision medicine recommendations
- **Rehabilitation Guidance**: Exercise plans (aerobic + resistance + flexibility), nutrition recommendations, fertility preservation options
- **Treatment Timeline Visualization**: Visual tracking of treatment progress with milestones, expected outcomes, recovery phases
- **Drug Interaction Checker**: Verify medication compatibility with current chemotherapy + supportive drugs
- **Clinical Trial Matching**: Help patients find relevant clinical trials based on their cancer profile and location
- **Follow-Up Surveillance Plan**: Automated scheduling for post-treatment imaging, lab work, and follow-up visits
- **Pregnancy/Fertility Counseling**: Special module for young patients concerned about fertility after treatment

> **Important Reminder**: 
> - **Ground innovations in real patient needs**: Before coding, interview actual patients/caregivers about their pain points
> - **Leverage AI Coding Skills**: Use RAG, multi-modal processing, wearable integration, messaging platforms (WeChat/Telegram) from the skill ecosystem
> - **Discuss with Mentor early**: Ensure your innovation is feasible, privacy-compliant, and aligns with charitable mission
> - **Prioritize MVP**: Focus on 1-2 core innovations for the first version; expand later based on user feedback
> - **Reference**: See AI_Coding_Innovation_Skill_Trends.md in Public_resources for detailed architecture examples and code samples

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

- **Feature Completeness**: Complete core dialogue function, support knowledge Q&A for at least 2-3 cancer types
- **Innovation Implementation**: Successfully implement at least 1 of the above innovation scenarios with functional MVP
- **User Experience**: Seed user test feedback satisfaction ≥ 80%
- **Content Accuracy**: Pass medical expert review, key information accuracy ≥ 95%
- **Service Availability**: System runs stably, response time < 5 seconds
- **Compliance**: Full medical disclaimer, privacy protection, and charitable mission alignment documentation

---

## Reference Resources

- **GitHub Repository**: https://github.com/PancrePal-xiaoyibao/xiaofubao.git
  - For learning knowledge base structure and RAG preprocessing methods
  - **Note**: Don't copy code directly, implement yourself after understanding the ideas

- **AI Innovation Reference**: See `Public_resources/AI_Coding_Innovation_Skill_Trends.md` for:
  - Detailed architecture diagrams of the three innovation scenarios above
  - Python code examples and implementation patterns
  - Real-world data metrics and thresholds
  - Community skill ecosystem components

- **Medical Resources**:
  - CSCO Clinical Guidelines (Chinese Society of Clinical Oncology)
  - NCCN Guidelines (National Comprehensive Cancer Network)
  - National Cancer Center related materials
  - Authoritative medical journals and databases

- **Technical Tools**: Refer to [tools_kit_101.md](../../Public_resources/tools_kit_101.md)

---

## Recommended Team Division

- **Product Manager**: Requirement analysis, user research, product design, innovation strategy
- **RAG Engineer**: Knowledge base construction, RAG system setup and optimization, retrieval accuracy improvement
- **Backend/Bot Developer**: Dialogue interface development, bot integration, wearable/hospital data connectors
- **Frontend Developer**: User interface design, mobile/web app development, data visualization
- **Content Operations**: Medical content collection, review, and update, patient interview coordination
- **QA/Testing**: Medical accuracy verification, user acceptance testing, edge case handling

---

## Contact and Support

- **Mentor Guidance**: Contact your project mentor for professional advice on innovation feasibility
- **Medical Review**: Medical content must be submitted to PMC for review
- **Technical Support**: Seek help in project group or GitHub Issue when encountering technical problems
- **Reference Repository**: Can consult Sam, initiator of xiaofubao project, for experience with knowledge base structure and RAG implementation

---

## Encouraging Words

This is a very meaningful project. Your work will directly help real patients navigate their cancer journey with better information and support. Don't worry about technical barriers - the community, mentors, and the AI Coding Skill ecosystem will support you. 

**The most important thing is to start with empathy for patients and their families.** Interview them about their real struggles. Build features that solve their actual problems, not features that sound cool in presentations. A simple, truly useful tool for patients is infinitely more valuable than a complex tool no one understands.

**Let technology warm life, let information light up hope** 💝
