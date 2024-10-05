# Meeting 3

#### Friday October 4, 2024 @ 9 - 9:15am

### Attendees
Dr. Mehdi Moradi (moradm4@mcmaster.ca)  
Kieran Henderson (hendek12@mcmaster.ca)  
Javier Afonso (afonsj2@mcmaster.ca)  
Corinna Lin (linc94@mcmaster.ca)  
Deluckshan Murugesu (murugesd@mcmaster.ca)  
Donyasadat Zolfaghari (zolfaghd@mcmaster.ca)   

## Items Covered
1. Data and LLM concerns
2. Computational Power
3. SRS Clarifications
4. Actions Required
---

### Data and LLM concerns
- make sure to actually fine-tune the LLM (llama), don't just prompt the model without modifying it
- fully retraining the model is out out of our scope and timeline
- it's easy to get sidetracked by the complexities of retraining and tuning a LLM, so sometimes people end up just sending a prompt to an already existing LLM - avoid this

### Computational Power
- where are we gonna train the model?
    - talk to Dr. Welch regarding the plan and if we need to rent school resources
    - can talk to Dr. Moradi if resources are needed
- use fine-tuning methodologies within manageable computational costs

### SRS Clarifications
- need to specify that we have a login system and user security
    - how will this be encrypted?
    - can use fake accounts to simulate real situation if needed
    - need to make sure that all our data is secure - including user information, database, logs
        - specify who has access to this data
- compliance can be user privacy
    - what levels of standards must we follow in user privacy?
    - encrypting patient information, privacy, user management
    - what are our safety issues and compliance systemics?

### Actions Required
- talk with Dr. Welch regarding computational requirements for training LLM, proceed accordingly