# Computer System Block Diagram

## ASCII Diagram (GitHub Friendly)
```
┌─────────────────────┐           ┌─────────────────────────────────┐         ┌─────────────────────┐
│  🖱️  Keyboard /Mouse│           │               🖥️ CPU            │         │       🖨️ Output     │
│  🎤  Microphone     ├───────►│  ┌ ──────────────┐ ┌─────────────┐ │────────►│  📺 Monitor         │
│  📷  Camera         │           │ │ Control Unit │ │    ALU       │         │  🔊 Speakers        │
│  ⌨️  Other Devices  │           │ └────────────┘  └─────────────┘ │         │  📄 Printer         │
└─────────────────────┘            │       ▲         ▲               │         └─────────────────────┘
Input Unit                         │       │          │              │         Output Unit
                                   │  ┌──────────────┐│              │
                                   │  │ Memory Unit  │◄┘             │
                                   │  │ (RAM, Cache) │               │
                                   │  └──────────────┘               │
                                   └─────────────────────────────────┘
                                    Processing Unit
```

---

## Explanation of Each Component

### 1. Input Unit (🖱️ Keyboard, Mouse, Microphone, Camera, etc.)
- **Purpose:** Accepts data and instructions from the user or external devices.
- **Examples:**
  - **Keyboard / Mouse** — text and command input.
  - **Microphone** — audio input.
  - **Camera** — image/video capture.
  - **Other Devices** — scanners, touchscreens, etc.
- **Function:** Converts user inputs into a digital form that the computer can process.

---

### 2. CPU (🖥️ Central Processing Unit)
The **brain of the computer**, responsible for processing and controlling all operations.

#### a. Control Unit (CU)
- **Role:** Directs data flow between CPU, memory, and peripherals.
- **Tasks:** Fetches instructions, decodes them, and manages execution order.

#### b. Arithmetic Logic Unit (ALU)
- **Role:** Performs mathematical (addition, subtraction, multiplication, division) and logical operations (comparisons, AND, OR, NOT).
- **Importance:** Executes the actual data processing tasks.

#### c. Memory Unit (RAM, Cache)
- **RAM:** Temporary storage for active processes and data.
- **Cache:** Small, high-speed memory for frequently used instructions/data.
- **Function:** Stores instructions and intermediate results during processing.

---

### 3. Output Unit (🖨️ Output Devices)
- **Purpose:** Displays or delivers processed data to the user.
- **Examples:**
  - **Monitor** — visual display.
  - **Speakers** — audio output.
  - **Printer** — hard copy of documents.
- **Function:** Converts digital results into human-readable form.

---

## How Data Flows
1. **Input Unit** receives data from the user.
2. Data is **processed in the CPU**, with the Control Unit directing the flow, ALU handling computations, and Memory Unit storing temporary data.
3. The **Output Unit** presents the processed results.
