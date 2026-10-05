# Task 3 — Constraint Violations

| Constraint ID | Formal Constraint | Violation Scenario | What Went Wrong? | How Do We Know It Is Violated? |
|---|---|---|---|---|
| C1 | Train_Present → ¬Barrier_Open | Train_Present = TRUE and Barrier_Open = TRUE. | The barrier opened while a train was still present. | The condition requires the barrier to be NOT open when a train is present. |
| C2 | Train_Approaching → Barrier_Closed | Train_Approaching = TRUE and Barrier_Closed = FALSE. | An approaching train was detected but the barrier remained open. | The implication requires the barrier to be closed. |
| C3 | Train_Approaching → Warning_Active | Train_Approaching = TRUE and Warning_Active = FALSE. | A train was approaching but warning signals were not activated. | The required warning condition is false. |
| C4 | Train_Passing → Barrier_Closed | Train_Passing = TRUE and Barrier_Closed = FALSE. | The train was passing while the road barrier was open. | The constraint requires the barrier to remain closed. |
| C5 | Barrier_Open → Train_Cleared | Barrier_Open = TRUE and Train_Cleared = FALSE. | The barrier opened before the train completely cleared the crossing. | The barrier is open while the required clearing condition is false. |
| C6 | Train_Present → ¬Road_Traffic_Allowed | Train_Present = TRUE and Road_Traffic_Allowed = TRUE. | Road traffic was allowed while a train was present. | The constraint requires road traffic not to be allowed. |
| C7 | Sensor_Failure → ¬Barrier_Open | Sensor_Failure = TRUE and Barrier_Open = TRUE. | The barrier opened even though the train-detection sensor had failed. | The formal constraint requires the barrier to remain closed. |
| C8 | Communication_Lost → ¬Unsafe_Barrier_Open | Communication_Lost = TRUE and Unsafe_Barrier_Open = TRUE. | Communication with the control center was lost while the system entered an unsafe barrier-open condition. | The required safe condition is violated. |
