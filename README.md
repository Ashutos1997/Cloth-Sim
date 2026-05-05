[English](README.md) | [한국어](README.ko.md)

# Cloth Simulation
A high-performance, interactive, physics-based cloth simulation running directly in the browser. The project simulates a grid of interconnected points using springs, constraints, and aerodynamic drag models to replicate realistic fabric behavior.

## Features

- **Realistic Physics:** Built from scratch using verlet integration and constraint relaxation. Simulates properties like mass, stiffness, and structural integrity.
- **Interactive Tearing:** Click and drag to interact with the cloth. Pulling too hard will cause the fabric to tear naturally.
- **Material Presets:** Toggle between different fabric types with distinct physical properties:
  - **Silk:** Lightweight, highly responsive to wind.
  - **Denim:** Stiff and heavy, resistant to tearing.
  - **Linen:** Balanced behavior between silk and denim.
- **Environmental Controls:** Adjust wind strength, gravity, and even use your microphone to blow wind onto the cloth!
- **Responsive UI:** A tailored experience for both desktop (using a heads-up display side-panel) and mobile devices (using bottom sheets).
- **Internationalization:** Bilingual support for English and Korean directly in the UI.

## Tech Stack

- **Core:** HTML5 Canvas, Vanilla JavaScript (ES6+), Vanilla CSS.
- **Icons:** Phosphor Icons.
- **Fonts:** Pretendard, Noto Sans KR.
- **Package Manager:** `pnpm`.

## Getting Started

### Prerequisites

Ensure you have [Node.js](https://nodejs.org/) and [pnpm](https://pnpm.io/) installed.

### Installation

1. Clone the repository and navigate to the project directory:
   ```bash
   cd Cloth-Sim-2026
   ```

2. Install dependencies:
   ```bash
   pnpm install
   ```

### Running Locally

You can serve the project using any standard static file server. For example:
```bash
npx serve .
```
Then, open the provided localhost URL in your browser to view the simulation.

### Building & Typechecking

To run the TypeScript type checks (if you add TypeScript features or libraries):
```bash
pnpm run typecheck
```

## Structure

- `index.html`: The main entry point. Contains the complete application layout, HUD (Heads-Up Display), CSS styling, and the entire simulation engine written in JavaScript.
- `package.json` & `pnpm-workspace.yaml`: Project metadata, script commands, and workspace configurations.
- `vercel.json`: Deployment configuration for Vercel.

## Deployment

This project is configured for deployment on Vercel. With `vercel.json` and `@vercel/analytics` script tags included in the HTML, you can easily deploy it by running the `vercel` CLI command or connecting the repository to your Vercel account.

## License

MIT License
