# Smart City Flood Defense Command Center (SCADA Simulation)

## Project Overview
This is a highly accurate, zero-dependency cyber-physical system simulation. It models the telemetry and IoT rule engine for a Tier-1 Global Mega-Infrastructure flood defense system. The architecture is heavily inspired by existing hydrostatic barrier systems (like the MOSE project in Venice) and deep-shaft discharge silos (like the MAOUDC "G-Cans" in Tokyo).

This dashboard is designed to act as the primary Command Center (War Room) during a catastrophic flash flood or cyclone. It enforces strict physical laws, power grid failovers, and real-time kinetic visual feedback.

**Live Demo:** [Insert Your GitHub Pages Link Here]

## Core Infrastructure Simulated

### 1. The Hydrostatic Deflection Ramp (Primary Gate)
Unlike pneumatic buoyancy gates, this system uses a bottom-up hydrostatic basin. 
*   **Hinge Placement:** The gate is hinged on the *upstream* side.
*   **Physics:** When deployed, it acts as an angled ramp. 40mph floodwaters and heavy debris (cars, trees) surf up and over the barrier, deflecting kinetic energy away from the vulnerable hinge mechanism and guiding trash cleanly into the surface-level debris pen.

### 2. Deep-Shaft Discharge Silo (The Muscle)
Clean water drops through the surface trash rack into a 50-foot subterranean silo.
*   **Jet Turbines:** Massive discharge turbines at the base pump 200 tons of water per second out to the ocean outfall.
*   **Thermodynamics Rule:** These turbines require **Megawatts** of power. They are hard-wired exclusively to the main city power grid.

### 3. Micro-Gen & Hydro-Battery Failover (The Brain)
If the city grid collapses during a cyclone, the main turbines die. However, the War Room must remain online to broadcast evacuation sirens.
*   **Kinetic Harvesting:** A micro-generator in the drop shaft harvests the kinetic energy of the falling water, producing **Kilowatts** of power.
*   **Failover Logic:** This trickle-charge feeds a buried, reinforced battery bank. If the grid dies, the LoRaWAN network and IoT dashboard automatically fail over to this battery, guaranteeing telemetry survives the blackout.

## Dashboard Architecture & UI/UX
This interface rejects consumer-grade design in favor of a brutalist, high-density layout standard in critical industrial control rooms.
*   **Tech Stack:** 100% Vanilla HTML, CSS, and JavaScript. Zero external libraries.
*   **Visual Engine:** Raw inline SVG manipulaton using `requestAnimationFrame` for the physics loop.
*   **Dual-Camera CCTV:** Operators can toggle between "Cam 1: Main Facility" and "Cam 2: Ocean Outfall" without losing sight of critical right-panel telemetry. 
*   **Terminal Logging:** Flush-left, timestamped system logs provide a chronological audit of state changes and structural warnings.

## Usage / Simulation Controls
1. **Upstream Velocity Slider:** Controls the severity of the flash flood. Push past 50mph to force the gate to overtop and trigger the turbines.
2. **Main Grid Toggle:** Simulates a catastrophic city-wide blackout. Watch the physical wiring change states and the hydro-battery engage.
3. **Inject Heavy Debris:** Drops heavy payload into the high-velocity stream to verify the deflection angle of the gate and the capacity of the debris pen.
4. **CCTV Outfall Toggle:** Click "TO OCEAN DISCHARGE" on the main schematic to view the real-time high-pressure dispersal at the seawall.
