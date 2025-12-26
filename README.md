
 Unity Hackathon Demo: What You’ll Build
🎯 GOAL:
Make a working demo in Unity where you can:

Pick an engineer

Choose 3 traits

Assign them to a project

See a funny outcome based on that combo

That’s it. If you show this loop working, you win.

🛠️ Unity To-Do Checklist
🔧 SETUP (1–2 hrs)
 Install Unity Hub + create project using 2D Core Template

 Add a Canvas (this lets you build UI)

 Create a main scene (call it GameScene)

 Add background image or just a solid color

🎮 UI SETUP (Click-based)
 Text box at top: “Assign Your Engineer”

 Dropdown to select an engineer (3–5 predefined)

 Trait picker: 3 toggles or dropdowns (choose from 8–10 traits)

 Button: “Start Project”

 Outcome log box: shows result of project

 Optional: chaos meter (just a UI bar or emoji)

👷‍♂️ ENGINEERS
 Create a list of 5 engineers with:

Name

Bio (optional)

Empty trait slots

 Display engineer info when selected

🧠 TRAITS (Make these as string data first)
 8–10 trait options (e.g. Perfectionist, Speedrunner, Paranoid)

 Each trait has modifiers (speed, safety, chaos, stress)

 Store traits in a scriptable object or just use simple arrays

🤖 OUTCOME ENGINE (Fake AI via rules!)
 Create a basic logic table:

Trait + project → outcome

 Outcome types:

Success

Partial success

Failure

Absurd death

 Display text in outcome box

e.g. “Speedrunner Ravi finished the bridge in record time—then fell off it.”

✍️ CONTENT YOU NEED TO WRITE
 Engineer names (5)

 Trait descriptions (10)

 Project types (3–4)

 10+ event outcomes (success/failure/death)

🧪 STRETCH GOALS (Only if time allows)
 Track engineer stress or mood (emoji or color)

 Engineers can quit or rebel

 Chain reactions (failure causes chaos in next project)

 Save and reload engineer states

🗂 Suggested Folder Structure
pgsql
Kopioi
Muokkaa
/Assets
  /Scripts
    Engineer.cs
    TraitSystem.cs
    OutcomeEngine.cs
  /UI
    Canvas, Buttons, TextBoxes
  /Data
    Traits.json (or scriptable objects)
    Engineers.json
  /Scenes
    GameScene.unity
Let me know if you want:

Unity prefab templates (UI layout)

Sample scripts for engineers + trait logic

Event text templates

You got this. Now go be dangerous 💻🛠️🔥
# mvp
# mvp
