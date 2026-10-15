# Parametric Aero-Thermal Heat Sink Optimizer

A thermo-fluid design and optimization tool linking analytical aerodynamic drag formulations with convective heat dissipation.

## Engineering Trade-Off
In forced-convection heat sink design:
- Increasing fin height and reducing fin gap maximizes total wetted surface area, boosting thermal dissipation ($\dot{Q}$).
- Conversely, tighter channels constrict airflow, exponentially increasing pressure loss ($\Delta P$) and fan pumping power ($P_{pump}$).

This tool uses a 1D thermo-fluid model in MATLAB to scan the geometric design space and determine optimal dimensions prior to 3D CAD modeling.

## Parametric Design Space
![Trade-off Contours](tradeoff_contours.png)

## Current Results
- **Constraint:** Fan Power $\le$ 5.0 W
- **Target Heat Sink Footprint:** $120 \times 100$ mm
- **Optimized Parameters:**
  - Fin Height ($H$): 45 mm
  - Fin Pitch ($P$): 4 mm
  - Cooling Output: ~280 W
  - Pumping Power: 3.8 W

## Project Roadmap
- [x] 1D aerodynamic pressure drop & thermal dissipation solver
- [x] Design space exploration and contour visualization
- [ ] Parametric 3D CAD model generation in Siemens NX
- [ ] Automated dimension update pipeline
