# Dynamic Launch in LabVIEW

This LabVIEW project demonstrates dynamic launching and event-based communication between multiple subVIs. The program leverages user events to handle interactions and processes asynchronously, allowing for flexible control and execution of tasks.

## Key Features

1. **Dynamic SubVI Launching**:
   - The main program dynamically launches subVIs during runtime.
   - Each subVI runs independently, with communication to and from the main program managed through user events.

2. **Event-Based Communication**:
   - User events are used to handle value changes in the subVIs.
   - The events are registered in the main program, which listens for specific triggers, such as value changes in subVI controls (e.g., X and Y coordinates).

3. **Multi-threaded Operation**:
   - The program runs multiple threads by dynamically opening subVIs, allowing for concurrent execution.
   - This structure helps manage tasks simultaneously, improving efficiency and responsiveness.

4. **Safe SubVI Termination**:
   - Each subVI can be safely terminated using user-defined controls or external conditions.
   - SubVIs can be aborted or stopped dynamically without disrupting the main program flow.

5. **Grid Manipulation**:
   - The subVIs update a grid control, allowing for real-time display of calculations or coordinates.
   - Grid values change based on user interactions, and logical operations adjust the displayed data according to event triggers.

## Program Workflow

1. **Main Program Initialization**:
   - The main VI launches and sets up user events.
   - It dynamically calls several subVIs, passing control references and event registration to facilitate communication.

2. **SubVI Execution**:
   - SubVIs operate independently, updating their internal controls (X, Y values) and processing user-defined events.
   - Event-based updates are sent back to the main program, ensuring real-time responsiveness.

3. **Event Handling**:
   - Events such as value changes are handled by registered user events in the main VI.
   - Depending on the triggered event (e.g., "X" or "Y" value change), the main VI processes data and updates outputs (such as the grid display).

4. **Termination**:
   - The subVIs can be terminated individually based on user input or conditions defined in the main VI.
   - A stop signal is sent to each subVI when necessary, ensuring safe termination without data corruption.

## Inputs and Outputs

- **Inputs**:
  - User events, specifically changes in subVI controls (X and Y values).
  
- **Outputs**:
  - A dynamically updated grid representing changes in the subVIs.
  - Real-time event responses shown through UI elements in the main program.

## How to Use

1. Launch the main program in LabVIEW.
2. Dynamically launch subVIs to perform tasks or update the grid display.
3. Use the X and Y controls in the subVIs to trigger events.
4. Observe changes in the main program as subVIs communicate via user events.
5. Stop or abort the subVIs safely using controls provided.

## Requirements

- **LabVIEW** version XX.X or later
- Basic understanding of event-driven programming and multi-threading in LabVIEW

## Notes

- Ensure proper handling of user events to avoid potential data race conditions.
- The program allows for dynamic execution of subVIs, ensuring flexibility in multi-tasking applications.

## Code
![image](https://github.com/user-attachments/assets/80ae70da-11dc-4751-8159-9ff8713193c5)
![image](https://github.com/user-attachments/assets/d0e22898-c388-4fe4-9d3e-f5070c80e113)
![image](https://github.com/user-attachments/assets/bace11e7-d762-4902-8728-6b5ac167c3a4)
![image](https://github.com/user-attachments/assets/4caaa8c8-fef4-4850-b0a7-c4a61753c31c)

## The appearance of the running program
![image](https://github.com/user-attachments/assets/2f2efda9-bb7a-4ee1-91ec-ee06e12ea9b7)
![image](https://github.com/user-attachments/assets/34ba2b73-bc12-4c9d-8ac1-ed95088a1a41)
![image](https://github.com/user-attachments/assets/85fd32cc-e261-4d12-bd64-5f1032fe5d73)

