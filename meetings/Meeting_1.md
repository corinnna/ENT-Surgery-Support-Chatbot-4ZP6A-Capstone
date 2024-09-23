# Meeting 1

#### Monday September 23, 2024 @ 12:30-1pm

### Attendees
Dr. Denise Geiskkovitch (geiskkod@mcmaster.ca)  
Dr. Charles Welch (cwelch@mcmaster.ca)  
Kieran Henderson (hendek12@mcmaster.ca)  
Javier Afonso (afonsj2@mcmaster.ca)  
Corinna Lin (linc94@mcmaster.ca)  
Deluckshan Murugesu (murugesd@mcmaster.ca)  
Donyasadat Zolfaghari (zolfaghd@mcmaster.ca)  
Ben Weeks (weeksb1@mcmaster.ca)  

## Items Covered
1. Meeting with Dr. Benjamin van der Woerd (vanderw@mcmaster.ca)
2. Ethics Considerations and Stakeholders
3. Project Planning  
    - Back-End Details  
    - Front-End Details
4. Actions Required

---

### Meeting with Dr. Benjamin van der Woerd (vanderw@mcmaster.ca)
- Dr. Geiskkovitch will try to schedule a meeting with Dr. Van der Woerd within the next few weeks to get a sense of what he really needs and what the solution needs to look like
    - will confirm whether we will have access to the users
- need to come up with a detailed list of what we'll want to know from him before the meeting
    - ideally, another meeting is scheduled with supervisors to verify our needs before meeting with Dr. Van der Woerd
- depending on the amount of information Dr. Van der Woerd can give us, we might want to talk to potential users/patients that he has

### Ethics Considerations and Stakeholders
- if we're talking to patients beforehand, it wouldn't be as a research study so ethics wouldn't be a large concern
    - if we publish research, then ethics need to be considered
- if patients are providing feedback on a prototype, ethics also needs to be considered here
- for the sake of time, it is likely we will just be talking to users
- if ethics has already been submitted to patients, we may be able to work with them
- depending on what stakeholders say, the project plan may change

### Project Planning
#### Front-End
- focused on user-centered design process
    - phases: investigation -> ideation -> prototyping
- still need stakeholder info to see if it will be a web app or a mobile app
    - likely to be a web dev using common languages such as HTML, CSS, and JavaScript

#### Back-End
- finetuning a model using python, huggingface as a library
- look at adapter methods, specificaly adapter hub
    - library is setup in a way that its easy to switch these out
    - double bottle neck sequence adapter has been working well, but it's harder to say which one is better for specific applications

### Actions Required
- schedule meeting with Dr. Van der Woerd
- gather information requirements and detailed list of what is needed from Dr. Van der Woerd
- look into finetuning and training a full model
    - check out the following links:
        - https://huggingface.co/docs/transformers/en/model_doc/bert
        - https://adapterhub.ml/
        - https://docs.adapterhub.ml/methods.html
        - https://browse.arxiv.org/pdf/2303.18223
    - optionally, briefly skim over the following surveys to get a better feel of what may happen within the back-end
        - https://arxiv.org/pdf/2404.15777
        - https://browse.arxiv.org/pdf/2303.18223
    - check out some language models in healthcare:
        - https://github.com/burglarhobbit/Awesome-Medical-Large-Language-Models
        - https://github.com/Jianing-Qiu/Awesome-Healthcare-Foundation-Models
- develop the project plan
- send all document templates to supervisors
- request access to the Llama models:
    - https://www.llama.com/llama-downloads/


#### Notes:
- Dr. Van der Woerd also has a pHd student working on this project, so they might also be easier to reach 
- if progression on the SRS document moves quickly, thinking about the project plan may be better