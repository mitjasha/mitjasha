# Dzmitry Shakhrai

**Computational Engineering · Multiphysics Simulation · Thermal Management · Scientific Computing**

I develop physics-based computational models and open-source engineering tools to understand complex systems and support engineering decisions. My work connects thermal and fluid engineering, structural mechanics, numerical optimization, and scientific software, from detailed simulation to fast, interpretable models.

I care about more than producing a plausible field plot: a useful computational result needs clear assumptions, numerical checks, reproducible experiments, and an honest account of its limitations.

## Engineering and research interests

- **Thermal management and cooling:** electronics and semiconductor cooling, heat transfer, liquid-cooling systems, thermal transients, and thermal networks.
- **Computational mechanics:** finite-element analysis, structural response, vibration and frequency analysis, and topology optimization.
- **Fluid dynamics and multiphysics:** flow and heat-transfer modeling, coupled physical systems, and reduced-order representations.
- **Optimization and scientific ML:** physics-checked surrogate models, data-driven warm starts, parameter studies, and ML-assisted engineering workflows.
- **Scientific software:** Python-based solvers, simulation automation, visualization, and reproducible computational research.

## Selected open-source work

### [Topology Optimization](https://github.com/mitjasha/Topology-optimization)
**FEM, SIMP and machine-learning-assisted optimization · In progress**

An evolving structural optimization workflow combining finite-element analysis, density-based topology optimization, and ML warm starts with physics-based acceptance checks and fallback solves.

In the documented 2D benchmark, the Ridge-based approach required approximately **44% fewer online FEM solves** than the uniform-start baseline while passing the defined final-quality checks. This is a benchmark-specific result, not a claim of industrial or end-to-end speedup.

[![Continuous-density cantilever optimized with SIMP on a 48 by 24 mesh](https://raw.githubusercontent.com/mitjasha/Topology-optimization/master/mesh_study/mesh_48x24_continuous.svg)](https://github.com/mitjasha/Topology-optimization)

*Continuous-density SIMP example with 50% material. This illustrates the workflow, not a manufactured part.*

### [Air-Induction Sprinkler Investigation](https://github.com/mitjasha/Air-Induction-Sprinkler-investigation)
**Physics-based droplet and spray modeling**

A Python reduced-order model covering air entrainment, radial film flow, droplet breakup, and rainfall distribution. The project connects engineering equations to my co-authored research publications and develops workflows for calibration, parameter exploration, and comparison with future experiments or CFD results.

The included examples use synthetic inputs; calibration against raw experimental measurements is still pending.

[![Film flow, droplet sizes and rainfall distribution for a synthetic example](https://raw.githubusercontent.com/mitjasha/Air-Induction-Sprinkler-investigation/main/docs/demo/overview.png)](https://github.com/mitjasha/Air-Induction-Sprinkler-investigation)

*Model outputs for a synthetic example: film flow, droplet sizes and rainfall distribution.*

### [OpenChipCool](https://github.com/mitjasha/OpenChipCool)
**Multiscale thermal modeling for liquid-cooled chiplets**

A computational framework linking 3D thermal FEM, transient thermal RC networks, a simplified liquid-cooling loop, and parameterized OpenFOAM case generation. It includes a dashboard for exploring workload and cooling scenarios, as well as numerical checks and comparisons between high- and reduced-order models.

OpenFOAM mesh checks, converged conjugate heat-transfer fields, and experimental validation are pending; solver compatibility remains unverified. Numerical verification and FEM/RC agreement do not establish experimental validation.

[![Steady 3D FEM temperature distribution in the chiplet package](https://raw.githubusercontent.com/mitjasha/OpenChipCool/main/results/temperature_field.png)](https://github.com/mitjasha/OpenChipCool)

*Steady 3D FEM temperature distribution for the synthetic chiplet package.*

## How I approach computational engineering

1. **Start from the physics.** Define governing equations, modeling assumptions, scales, and boundary conditions.
2. **Verify the numerics.** Check balances, convergence, sensitivity, and agreement with independent calculations or solvers where possible.
3. **Compare methods fairly.** Keep baselines, costs, and acceptance criteria explicit, especially when evaluating machine learning.
4. **Make results reproducible.** Provide runnable examples, documented parameters, tests, and inspectable outputs.
5. **Build incrementally.** Treat limitations and open questions as part of the development roadmap.

## Tools and methods used across my projects

**Methods:** FEM · CFD · heat transfer · structural dynamics · reduced-order modeling · topology optimization · numerical verification · scientific machine learning

**Software ecosystem:** Python · NumPy · SciPy · PyTorch · OpenFOAM · CalculiX · Modelica · Streamlit · Git / GitHub Actions

## Current directions

I am extending work on 2D/3D computational optimization, multiphysics coupling and co-simulation, fast models informed by higher-fidelity simulation, and practical ML integration into CAE workflows.

Explore the code, models, assumptions, and results in the repositories above.
