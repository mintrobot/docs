# SDR Ecosystem

MINTROBOT builds its robots on a consistent SDR ecosystem instead of assigning a different control stack to each product.

## Why This Matters

MINTROBOT does not want each robot family to depend on a separate control philosophy, interface model, or software workflow.

An SDR ecosystem matters because it keeps robotics open, composable, and scalable.

- open interfaces reduce dependence on isolated vendor-specific silos
- modular components can be combined more naturally into larger robot systems
- network-based robotics becomes easier to expand across products and deployments
- one control philosophy can remain consistent as the lineup grows

For that reason, MINTROBOT is deliberate about its control foundation. The controller must do more than drive motion. It must fit an open, network-oriented, software-defined robotics model.

## Open Architecture

At the foundation of this ecosystem is SDRM, an open-source middleware distributed by LibreRobotics.

SDRM is not a controller. It is an interface layer that allows each element of a robot system to operate efficiently in a networked environment.

Because SDR is fundamentally network-oriented, SDRM is well suited to robots that rely on software-based communication, distributed composition, and frontend-driven operation.

This matters because the architecture stays extensible. The middleware defines how components connect and interoperate, while leaving room for higher-level control products to provide actual control, user workflows, and deployment experience.

## Adoption of a Best-in-Class SDR Controller

Sodero builds SDR-based controllers on top of the SDRM middleware foundation.

Its controller combines:

- control functionality
- GUI and user workflows
- SDR-oriented software integration
- frontend-based, app-less operating experience

This is what turns an open middleware interface into a practical SDR controller product.

MINTROBOT adopts Sodero because it provides what MINTROBOT values most in an SDR control system: a mature controller built for network-based robotics, strong software integration, and a usable operator experience.

That decision creates consistency across the lineup:

- the control system remains coherent across robot families
- software workflows remain aligned across products
- composite robots can be assembled without changing the control philosophy
- system expansion remains compatible with the SDR approach

## Ecosystem Context

Within this ecosystem:

- LibreRobotics provides the open-source SDRM middleware foundation
- Sodero builds the SDR controller on top of that foundation
- MINTROBOT builds robot products around that controller environment
