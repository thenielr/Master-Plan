---
title: Week 1 – Control & Instrumentation Daily Practice
type: daily_problem_set
tags: [instrumentation, control, problem-solving, PID, sensors]
duration: 40min
related_concepts: [[PID tuning]], [[4-20mA loop]], [[DP transmitter]], [[sensor selection]], [[loop control]], [[level measurement]], [[valve authority]], [[MATLAB]], [[signal troubleshooting]]
---

> ⚙️ **Objective**: Solve one practical instrumentation/control design problem daily to sharpen engineering judgment and real-world diagnostic skills.

---

## 📅 Day 1 – Temperature Loop Troubleshooting
You’re called to troubleshoot a heating system. The loop uses a [[Type J thermocouple]], a [[4-20mA transmitter]], and a [[PID controller]] regulating a steam valve. The operator reports overheating.

**Tasks:**
- Draw the control loop and tag each instrument.
- How would you check for a faulty thermocouple vs transmitter?
- How might PID tuning cause overshoot?
- What safeguard (hardware or logic) can prevent overheating?

#temperature #PID #troubleshooting

---

## 📅 Day 2 – DP Transmitter Misreading Level
A [[DP transmitter]] is installed in a pressurized tank. Upper tap to vapor, lower tap to liquid base. The reading is unstable and inaccurate.

**Tasks:**
- Name 3 common installation errors (hint: impulse lines).
- Explain how condensate traps affect the reading.
- If tank height = 3 m, liquid ρ = 950 kg/m³, vapor space = 1 bar(g), calculate expected ΔP.

#level #DPtransmitter #processmeasurement

---

## 📅 Day 3 – Flow Control with Valve Sizing
A centrifugal pump delivers water through a control valve. Desired flow = 15 m³/h.

**Tasks:**
- Calculate valve authority using pump & system curves.
- Recommend valve type: globe vs butterfly vs ball.
- Explain the role of a [[positioner]] and [[I/P transducer]].

#valves #flowcontrol #actuators

---

## 📅 Day 4 – Sensor Selection for Harsh Environment
You need to monitor temperature inside a reactor with H₂S vapors, 250 °C, high vibration.

**Tasks:**
- Choose between [[RTD]] or [[thermocouple]]. Justify.
- Pick sheath material (e.g., Inconel?) and junction type (grounded, ungrounded, exposed).
- Specify a transmitter (signal type, diagnostics).

#sensors #thermocouple #RTD #hazardousarea

---

## 📅 Day 5 – PID Control Simulation
A first-order plant has:  
$$ G_p(s) = \frac{2}{5s + 1} $$

**Tasks:**
- Simulate step response with default PID gains in [[MATLAB]] or Python.
- Tune PID to reduce overshoot; settling time < 10 s.
- Plot and interpret result.

#PID #simulation #MATLAB

---

## 📅 Day 6 – Signal Loop Analysis
A 4–20 mA loop isn't transmitting signal to the controller.

**Tasks:**
- Sketch full loop: transmitter, power, resistor, controller.
- Identify 3 wiring mistakes (e.g., reverse polarity, open circuit).
- If R = 250 Ω, and I = 12 mA, what is the voltage drop?

#loopcheck #currentloop #instrumentation

---

## 📅 Day 7 – Multi-loop Coordination
A tank uses:
- Valve A for inflow control (flow loop)
- Valve B for outflow (level loop)

Operators report erratic level control.

**Tasks:**
- How do loops interact?
- Suggest a strategy: [[cascade control]] or [[decoupling]]?
- What happens if both loops run in auto with bad tuning?

#multiloop #levelcontrol #cascade
---
title: Week 2 – Control & Instrumentation Daily Practice
type: daily_problem_set
tags: [instrumentation, control, calibration, diagnostics, HAZOP, transmitters, safety]
duration: 40min
related_concepts: [[instrument calibration]], [[signal wiring]], [[fail-safe control]], [[alarms and interlocks]], [[instrumentation loops]], [[transmitter diagnostics]], [[loop tuning]], [[multivariable control]]
---

> 🎯 **Objective**: Reinforce applied instrumentation and control thinking through hands-on problem design and analysis.

---

## 📅 Day 8 – Calibration Drift Detection
A pressure transmitter used in a batching system starts showing erratic spikes during normal operation.

**Tasks:**
- List possible root causes (e.g., process noise, wiring, grounding).
- Design a 3-point calibration test and record values.
- If the drift is +1.6% FS over time, should you recalibrate or replace?

#calibration #pressuretransmitter #driftdetection

---

## 📅 Day 9 – Thermowell and RTD Selection
You're replacing a failed RTD in a line carrying thermal oil at 180 °C, under moderate flow. The last sensor failed due to vibration.

**Tasks:**
- Choose a suitable [[thermowell]] type (straight, tapered, stepped).
- Specify insertion length to avoid wake frequency failure.
- Recommend RTD element and mounting (e.g., spring-loaded).

#RTD #thermowell #sensorselection #vibration

---

## 📅 Day 10 – HAZOP and Fail-Safe Logic
In a fuel supply system, a valve should close on low pressure and high temperature alarms. Safety is critical.

**Tasks:**
- Design logic using [[relays]] or digital I/O to close valve on failure.
- Specify fail-safe position for valve actuator and reasoning.
- Recommend an [[interlock]] or HAZOP safeguard.

#fail-safe #safetyinstrumentedfunctions #interlocks #hazop

---

## 📅 Day 11 – Loop Performance Evaluation
You observe sluggish response in a flow control loop. Step tests confirm it takes ~40 s to reach 90% of setpoint.

**Tasks:**
- List what to check: valve stiction, sensor lag, etc.
- Suggest control strategies: increase gain, use [[feedforward]], etc.
- Design a performance metric (e.g., IAE, rise time).

#looptuning #controlperformance #flowcontrol

---

## 📅 Day 12 – Transmitter Configuration Logic
A DP transmitter measures open tank level with a remote seal and capillary tube. You’re asked to re-range it from 0–2 m to 0–5 m.

**Tasks:**
- What parameters need to be adjusted? (e.g., zero/span)
- How does capillary fill fluid type affect accuracy?
- Describe steps to validate output using a [[handheld calibrator]].

#levelmeasurement #DPtransmitter #configuration #remoteseals

---

## 📅 Day 13 – Ground Loop Problem
A 4–20 mA loop in a motor control center causes unstable readings. Technicians suspect a ground loop.

**Tasks:**
- Define a [[ground loop]] and how it affects analog signals.
- Show how to test and break the loop using isolators or differential inputs.
- Suggest wiring layout to prevent future problems.

#groundloop #wiring #signals #noise

---

## 📅 Day 14 – Split Range Control
In a mixing tank, two control valves regulate cold and hot water. The operator wants to control temperature using a single controller.

**Tasks:**
- Design [[split range]] control logic for the two valves.
- What issues can occur at the crossover point?
- Propose PID tuning strategy to prevent oscillation during overlap.

#splitrange #temperaturecontrol #dualvalve #loopdesign
___
---
title: Week 3 – Control & Instrumentation Daily Practice
type: daily_problem_set
tags: [instrumentation, control, signal conditioning, SCADA, diagnostics, dynamic response, process safety]
duration: 40min
related_concepts: [[instrumentation troubleshooting]], [[loop dynamics]], [[PLC vs DCS]], [[smart transmitters]], [[control modes]], [[signal filtering]], [[alarm management]], [[ISA standards]]
---

> 📌 **Objective**: Apply field-based judgment and signal-level insight to real-world instrumentation and control tasks.

---

## 📅 Day 15 – Smart Transmitter Diagnostics
A smart pressure transmitter connected to a DCS shows good PV but frequent “low sensor voltage” alarms.

**Tasks:**
- Decode what the diagnostic message implies.
- Suggest 3 tests to verify wiring and sensor connection.
- How would you use HART communication to access logs and force outputs?

#smarttransmitter #HART #diagnostics #alarms

---

## 📅 Day 16 – Control Loop Direction and Action
A control loop is unstable after a technician reversed a transmitter. The valve fails closed and is air-to-open.

**Tasks:**
- Determine if direct or reverse action is needed for:
  - Controller
  - Transmitter
  - Valve
- Redraw the loop with correct action paths.
- Describe how to test response direction without risking the process.

#controlaction #loopstability #signalpolarity

---

## 📅 Day 17 – Signal Filtering vs Responsiveness
Your temperature loop is noisy. A digital filter is applied, and now the process is sluggish.

**Tasks:**
- Model the trade-off between filtering and responsiveness.
- Simulate or sketch expected PV signal with and without filtering.
- Recommend a better method than filtering (e.g., signal conditioning or averaging).

#signalfiltering #responsiveness #noise #temperaturecontrol

---

## 📅 Day 18 – Alarm Management Strategy
An operator disables all alarms due to constant nuisance alerts during startup of a distillation column.

**Tasks:**
- Propose a strategy based on ISA-18.2 (alarm rationalization).
- Define alarm types: critical, warning, advisory.
- Design a logic delay or deadband for 2 key parameters.

#alarmmanagement #ISA18 #startup #nuisancealarms

---

## 📅 Day 19 – Cascade Loop Implementation
In a heat exchanger, the temperature is unstable due to lag in the main loop. Flow rate of heating fluid is measurable.

**Tasks:**
- Design a [[cascade control]] strategy with inner flow loop and outer temperature loop.
- Sketch both loops with PIDs.
- List benefits and tuning priorities.

#cascade #heatexchanger #loopdesign #tuning

---

## 📅 Day 20 – Field Fault Isolation
An instrumented level transmitter is not showing signal in SCADA. Multimeter shows 24 Vdc at terminals.

**Tasks:**
- Determine how to isolate whether the problem is:
  - Transmitter
  - Cable
  - Analog input card
- Explain how to simulate 12 mA signal to test wiring.
- List tools and test points.

#SCADA #fielddiagnostics #signaltest #cabling

---

## 📅 Day 21 – PLC vs DCS for Process Plant
You're designing a control system for a batch chemical reactor. Management is choosing between PLC and DCS.

**Tasks:**
- Compare PLC and DCS in terms of:
  - Scan time
  - Batch support
  - Cost
  - Integration with historian
- Recommend a system and justify based on operation type.
- Sketch architecture diagram.

#PLC #DCS #batchprocess #automationarchitecture
