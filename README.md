# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Date:25.10.2025
# Name : Rakshitha M
# Register no: 212223060220
# Aim: 
To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

# AI Tools Required: 

* Lovable AI,ChatGPT



# Explanation: 
Prompt:
"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."

# Procedure:
1. Define the core requirements of a personal productivity assistant.
2. Identify and construct appropriate prompts for each task using an LLM (e.g., ChatGPT).
3. Simulate natural user interaction through a simple interface or command-line system.
4. Collect feedback or inputs from users and adapt responses accordingly.
5. (Optional) Integrate basic memory to simulate preference adaptation.

# Output (Example Response by LLM):
Personal Productivity Assistant Features:
1. Daily Task Manager:
o Accept tasks via natural language (e.g., "Remind me to call mom at 6 PM").
o Organize tasks by priority and deadline.
o Provide daily summaries and pending items.
2. Smart Scheduler:
o Schedule events and set reminders using contextual understanding.
o Notify user of overlapping appointments or free time slots.
3. Wellness Tips Generator:
o Suggest daily wellness advice (hydration, exercise, screen-time breaks).
o Adapt suggestions based on past user preferences and responses.

# OUTPUT

## 1. Target User Profile

The system is designed around a detailed user profile to ensure highly personalized and context-aware responses. Key profile elements—such as a fixed wake-up time (6 AM) and a preferred study pattern (2-hour focused blocks)—serve as crucial scheduling constraints and wellness triggers. The friendly, casual, and caring tone (achieved through carefully engineered LLM prompts) is a core UI element, ensuring user interaction feels supportive rather than transactional.

## 2. Functional Mechanics and Core Roles

Aura's functionality is partitioned into four interdependent modules, each addressing a critical aspect of personal management. The efficiency of these roles relies on a preliminary NLU step that consistently extracts three key entities from every user input: ACTION, TIME, and PRIORITY.

**1. Task Manager (Data Operations)**

This module handles the CRUD (Create, Read, Update, Delete) operations for tasks. Once NLU processes the input, the Task Manager executes the command, serializing the resulting data (Task Description, DateTime, and Urgency Level) into the temporary session memory. The system must assign a default Priority if none is explicitly mentioned (e.g., "Add a task" might default to medium).

**2. Smart Scheduler (Temporal Logic)**

* The Scheduler is the system's reasoning engine, dedicated to optimizing the user's timeline. It performs complex logic, including:

* Time Block Allocation: Mapping user-defined study patterns (e.g., 2-hour blocks) to available free time slots.

* Conflict Detection: Checking if a newly requested event overlaps with existing scheduled tasks (e.g., meetings or fixed wake-up time).

* Proactive Balancing: As requested in the user input, it automatically inserts essential break events (sleeping, walking, listening to music) between focused blocks to prevent burnout, guided by the Wellness Coach's triggers.

**3. Wellness Coach (Emotional & Contextual Triggers)**

This module employs simple sentiment analysis and keyword spotting ("tired," "stressed," "unfocused") to activate immediate, encouraging responses. It delivers short, positive motivational lines and prescribes profile-preferred activities (hydration, short walks, stretching) to recalibrate focus. The use of limited, strategically placed emojis enhances the human-like, caring interaction.

**4. Quick Query Helper (Knowledge Retrieval)**

This module interfaces with a general knowledge model (like an LLM API) to answer specific productivity or planning questions ("What's a good 2-hour study plan?"). The key constraint is to ensure the tone remains within Aura's friendly and encouraging persona, providing actionable advice rather than academic essays.

## 3.System Logic Flowchart Structure

The interaction loop within Aura follows a precise sequence to ensure the right module is engaged after the initial NLU stage. Given the limitations of generating a true diagram, the process is detailed structurally below.

**Aura Interaction Flow Structure**

**Step 1: User Input Received**

The cycle begins when the user sends a message.

**Step 2: Primary Classification Engine (Router)**

The Router performs quick, keyword-based analysis to determine the user's immediate intent.
```
IF (Input contains keywords: "tired," "stressed," "unfocused")
    → Route to Wellness Coach
ELSE IF (Input contains keywords: "what is," "how to," "tell me about")
    → Route to Quick Query Helper
ELSE (Implies a task or scheduling request)
    → Route to NLU Processor
```
**Step 3: NLU Processor (Intent & Entity Extraction)**

If the input is a task or schedule request, the NLU module parses the message to extract key data and the user's command.

Extract Entities: ACTION, TIME/DATE, PRIORITY.

Determine Intent: ADD, LIST, UPDATE, DELETE, SCHEDULE.

**Step 4: Action Execution Layer (Task/Schedule)**

The system routes the processed intent to the specific management module.

A. Task Manager Execution
```
IF Intent is LIST/DELETE/UPDATE
    → Route to Task Manager (Access Session Memory)
ELSE IF Intent is ADD
    → Route to Task Manager (New entry to Session Memory)
```

B. Smart Scheduler Execution
```
IF Intent is SCHEDULE
    → Route to Smart Scheduler.
        - Scheduler Logic Checks:
            1. Check for profile constraints (6 AM wake, 2hr blocks).
            2. Check for existing overlaps/conflicts.
            3. Insert Break Events (for balance).
            4. Save final result to Session Memory.
```
**Step 5: Response Generation**

After execution, the system crafts a reply.

Select appropriate confirmation phrase based on the executing module and extracted entities.

Apply Tone and Emoji rules (friendly, max 3 emojis).

**Step 6: Output to User**

The final, personalized response is delivered.

**Memory Simulation (Temporary Session Store)**

Aura utilizes a temporary, session-based memory store. This simulated database, or Session Memory, is crucial for maintaining context within a single user session. It is designed to be highly reliable but non-persistent, enforcing the rule of recalling only tasks added during the current chat. This keeps the assistant focused and avoids overwhelming the user with external, fabricated data.

![pp1](https://github.com/user-attachments/assets/dc47808f-4334-47e8-a64d-801b1a56da80)



## 4.Proactive Reminders (The Two-Hour Loop)

The requirement to set recurring reminders (like drinking water every hour between 4 AM and 9 PM, but implemented with a 2-hour interval) demonstrates the need for a scheduled event loop within the system. This loop must:

Establish a start time (4:00 AM) and end time (9:00 PM).

Calculate the necessary delay (2 hours).

Execute the message (e.g., "Time to hydrate!") and reset the 2-hour timer, stopping only when the end time is reached.

This proactive intervention, distinct from user-input tasks, solidifies Aura’s role as an attentive productivity buddy rather than just a simple digital notepad.

# OUTPUT IMAGE

<img width="1479" height="629" alt="Screenshot 2025-10-25 195636" src="https://github.com/user-attachments/assets/9d9fb88c-e06b-401a-ad46-8566ea01fb3b" />
<img width="1474" height="495" alt="Screenshot 2025-10-25 195522" src="https://github.com/user-attachments/assets/63b0bbd4-bb9a-41d3-85de-e1353007ca4d" />








# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
