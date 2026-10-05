# Task 2 — Formalize Constraints

| Constraint ID | Constraint | Formal Expression |
|---|---|---|
| C1 | Barrier must not open while a train is present. | Train_Present → ¬Barrier_Open |
| C2 | Barrier must close when an approaching train is detected. | Train_Approaching → Barrier_Closed |
| C3 | Warning signals must be active when a train is approaching. | Train_Approaching → Warning_Active |
| C4 | Barrier must remain closed while the train is passing. | Train_Passing → Barrier_Closed |
| C5 | Barrier may open only after the train has completely cleared the crossing. | Barrier_Open → Train_Cleared |
| C6 | Road traffic must not be allowed while a train is present. | Train_Present → ¬Road_Traffic_Allowed |
| C7 | Barrier must not open when sensor readings are unreliable. | Sensor_Failure → ¬Barrier_Open |
| C8 | Communication loss must not cause the system to enter an unsafe open-barrier condition. | Communication_Lost → ¬Unsafe_Barrier_Open |
