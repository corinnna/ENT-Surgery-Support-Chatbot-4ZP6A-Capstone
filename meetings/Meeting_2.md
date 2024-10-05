# Meeting 2

#### Tuesday October 1, 2024 @ 3:30 - 4:30pm

### Attendees
Dr. Denise Geiskkovitch (geiskkod@mcmaster.ca)  
Dr. Charles Welch (cwelch@mcmaster.ca)  
Dr. Benjamin van der Woerd (vanderw@mcmaster.ca)  
Lomesh Choudhary (choudhl@mcmaster.ca)  
Kieran Henderson (hendek12@mcmaster.ca)  
Javier Afonso (afonsj2@mcmaster.ca)  
Corinna Lin (linc94@mcmaster.ca)  
Deluckshan Murugesu (murugesd@mcmaster.ca)  
Donyasadat Zolfaghari (zolfaghd@mcmaster.ca)  
Ben Weeks (weeksb1@mcmaster.ca)  

## Items Covered
1. Informed Consent and Scalability in Medicine
2. Overall Goal and Some Project Specifications
3. Logging and Login System
4. Data and Security
5. Testing
6. Legal/Functional Requirements and Documentation

---

### Informed Consent and Scalability in Medicine
- informed consent doesn't exist for complex surgeries with significant risks
    - often times when patients talk with their surgeon, they don't fully understand their procedure, and are unaware of all risks involved
    - they may think that their questions are "stupid" and hesitate to ask questions or come up with questions when they are unable to inquire about them
- medicine is very 1-1, making it very difficult to scale effectively
    - patients usually book 1-1 appointments + telemedicine is not widespread
- the procedure always involves an endoscopic portion, however, whether there will be an "open portion" is always decided the day of based on given circumstances
    - patients are consented for both surgical approaches, so it is crucial that they are aware of the risks associated with each approach

### Overall Goal and Some Project Specifications
- use this website (chat-bot) to improve the informed consent process and help iron out patient misunderstandings and inquiries
    - patients may feel more comfortable asking a chatbot questions compared to an actual human (potentially less judgement)
    - hopefully provide answers that are sufficient enough such that patient's don't need to follow up with the surgeon
- back-end wise: build a large language model (LLM) that answers questions related to the procedure or post-op procedure
- differs from a FAQ because:
    - patients can ask whatever they want (relative to the operation), and many answers baked into LLMS are pretty good
    - target users are 50-85 years old + on average people's medical literacy is ~13 years old, so many unexpected questions may be asked
    - patients can ask follow up questions, and the model can reword answers to aid with clarification
- appearance wise: simplistic, McMaster branding guidelines
- at the minimum, it should be bilingual (french and english), however, we need to look into our back-end frameworks for more info

### Logging and Login System:
- ideally the conversations between patients and LLM are logged
    - if they are, will the patient's awareness of this affect their interaction and the questions they ask?
- Dr. Van der Woerd can review conversations to ensure that no innapropriate/incorrect answers were given by the LLM before the procedure
- main purpose of login system is to track who's using the system
    - as of right now, only Dr. Van der Woerd's staff, patients + their families will be using the system, so he can just share login details with users
    - potentially link phone numbers to account

### Data and Security
- Dr. Van der Woerd and Lomesh will provide research documents, textbooks, and self-created documents regarding the specific procedure performed
    - helps to reassure patients that the information is verified by Dr. Van der Woerd (a trusted source)
- likely no patient medical information/data, all the LLM really needs to know is the size (>5cm?)
    - if patient medical information is used, many more privacy and security concerns are introduced
- if LLM responds based on patient background, it can actually be detrimental sometimes
    - many highly specific terms that anyone not in this specific field wouldn't understand
- LLM wouldn't ask for patient's information either since we can walk them through the decision making process (one approach vs. the other)
    - regardless LLM isn't making the decision, just informing them of both procedures (never makes a diagnosis, always refers patient to doctor for such inquiries)
- Dr. Van der Woerd can provide figures from a laryngology textbook
    - if only a few figures, we can just create a classifier for it
        - likely only to be 1-2 figures
- specific low level questions will not be the focus of the chatbot (may potentially fallback to Llama model for these types of questions)
    - LLM will be restricted to questions that are related to the procedure and should have a guardrail to guide patients back to topic
    - won't answer irrelevant questions 

### Testing
- once we have a functional prototype, Dr. Van der Woerd can cherry-pick a few of his patients that he already operated on to test the software
    - get feedback based on ease of use, usefulness etc.

### Legal/Functional Requirements and Documentation
- if patient's dont feel like their questions were adequately answered, they should be referred back to their surgeon
    - have a system that automatically sends a message to the medical office stating that the patient did not get relevant answers (potentially include transcript)
- likely shouldn't need to put a disclaimer directly before patient's use the software stating that they are talking to a bot not a human
    - if put at the beginning, patient's may not trust it as much
        - considering we're training the LLM on specific and good data, it should be alright, given that we properly test it
    - it still needs to be clear to the patient that they are chatting with a bot not a human
- no cultural considerations
- document everything since it is relevant clinically, and will be compiled into a clinical journal
    - info on the model being used, prompts used in the back-end, sources used etc. (ideally formatted as a scientific study)