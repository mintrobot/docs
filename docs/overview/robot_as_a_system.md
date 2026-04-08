# Robot as a System

MINTROBOT treats a robot as a system-level building block rather than a sealed standalone machine.

## Core Principle

MINTROBOT starts from the idea that `robot = system`.

A robot arm, a gripper, a mobile base, or a vision module should not be treated as an isolated endpoint. Each one should be designed to participate in a larger software-defined robotics environment.

## Why This Matters

- users should be able to start from one robot and expand without replacing the control concept
- hardware modules should remain reusable as the system grows
- robot behavior should be shaped by software orchestration, not fixed hardware boundaries
- integration should get easier as the deployment becomes larger

## Product Direction

This philosophy supports a product direction that grows from standalone robots toward more complex systems such as:

- mobile manipulators
- humanoids
- multi-robot cells
- networked robotic workstations

## System Architecture

MINTROBOT organizes robot products into a composable system architecture so one control foundation can scale from a single product to a larger robotic system without changing the core operating model.

### Robot Module

Each individual robot product, such as an arm, gripper, or mobile base, exposes controllable behavior through the shared software stack.

At this layer, the main concern is product-level capability.

### Composite Robot

Multiple robot modules can be combined into one coordinated system, such as:

- mobile manipulator
- dual-arm platform
- humanoid system

At this layer, the main concern is coordination between modules.

### Robotics System

Composite robots can then be integrated with external software, sensors, production infrastructure, and network services.

At this layer, the main concern is deployment in a real operating environment.

## Shared Software Boundaries

Within this architecture:

- product-specific mechanics and setup stay inside each product family
- shared control software, APIs, and common tools are provided through the Stellar stack
- system integration happens through networked software interfaces rather than isolated control silos
