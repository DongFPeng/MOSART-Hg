# MOSART-Hg

MOSART-Hg is a mercury-enabled extension of the Model for Scale Adaptive River Transport (MOSART) developed for simulating mercury transport, retention, and redistribution through global river networks.

This repository is maintained as a component of the **MOSART-Hg-WM** modeling framework based on CESM2.1.3. It contains the riverine mercury processes used to connect terrestrial mercury inputs with downstream transport, reservoir retention, and river-to-ocean export.

## Important Notice

**This repository is provided solely for peer review and scientific evaluation.**

The source code, model modifications, parameterizations, configuration information, documentation, unpublished implementation details, figures, and other materials contained in this repository are not released for unrestricted public reuse.

Any reuse, redistribution, adaptation, incorporation into other models or software, derivative development, or use of unpublished materials from this repository requires **prior written permission** from **Dong Peng or the corresponding author(s)** of the associated work.

If you wish to reuse or reference repository-specific materials, model implementation details, parameterizations, or unpublished methods, please contact the authors before use.

These restrictions apply to the authors' original modifications and materials and do not supersede the licenses or terms governing CESM, MOSART, or other third-party software.

## Model base

```text
CESM version: 2.1.3
River model:  MOSART
Component:    MOSART-Hg
```

MOSART-Hg extends the standard MOSART river-routing framework with mercury-specific source, transport, and retention processes.

## Main developments

The model framework includes processes related to:

- mercury delivery from terrestrial systems
- dissolved mercury transport
- particulate mercury transport
- sediment-associated mercury routing
- riverine mercury retention
- mercury release and remobilization
- anthropogenic mercury inputs to river systems
- reservoir and dam regulation
- mercury trapping by reservoirs
- downstream transport through river networks
- river-to-ocean mercury export
- source attribution of riverine mercury fluxes
- historical and future changes in mercury transport

These processes allow MOSART-Hg to represent how both natural processes and human perturbations modify mercury transport through continental river systems.

## Water-management representation

MOSART-Hg can be coupled with water-management and reservoir-related processes to quantify the influence of dams and reservoirs on riverine mercury transport.

Relevant processes include:

- reservoir interception of particulate mercury
- modification of downstream mercury fluxes
- changes in sediment-associated mercury transport
- spatial redistribution of mercury retention
- cumulative regulation along river networks

The integrated configuration is referred to as **MOSART-Hg-WM**.

## Role in MOSART-Hg-WM

Within the coupled framework:

```text
           CLM-Hg
              ↓
     Land-to-river Hg fluxes
              ↓
          MOSART-Hg
              ↓
   River transport / retention
              ↓
 Reservoir regulation / trapping
              ↓
      River-to-ocean export
```

MOSART-Hg receives terrestrial mercury inputs from CLM-Hg and routes mercury through the river network while accounting for transport, retention, and human perturbations.

The coupled model configuration is maintained in:

**MOSART-Hg-WM**  
`https://github.com/DongFPeng/MOSART-Hg-WM`

## Repository use

This repository preserves the MOSART-Hg development history and the riverine mercury model versions used in MOSART-Hg-WM.

For coupled simulations, users should refer to the parent MOSART-Hg-WM repository, which records the exact CLM-Hg and MOSART-Hg commits used for each model configuration.

## Publications

The development and application of MOSART-Hg and the coupled terrestrial-river mercury framework are described in the following studies:

1. **Peng, D. et al. (2025). Human perturbations to mercury in global rivers. _Science Advances_, 11, eadw0471.**  
   DOI: `10.1126/sciadv.adw0471`

2. **Peng, D. et al. (2026). Tracing Mercury from Land to River: Global Sources, Retention, and Implications for Sustainability. _Environmental Science & Technology_, 60, 21885–21900.**  
   DOI: `10.1021/acs.est.6c03367`

Additional publications and research outputs are available through the author's ResearchGate profile.

## Data and model input

Large CESM input datasets, hydrological forcing, NetCDF input files, restart files, model outputs, and temporary processing files are not maintained in this repository.

Required CESM and MOSART input datasets should be obtained separately and configured according to the local computing environment.

## License and use restrictions

The underlying CESM and MOSART source code remains subject to its original license and terms of use.

The authors' original mercury-related modifications, parameterizations, configurations, documentation, and unpublished implementation details are provided for **peer-review and scientific-evaluation purposes only**, unless explicit written permission for further use has been granted.

Permission requests should be directed to Dong Peng or the corresponding author(s) of the associated publication.

## Contact

**Dong Peng**  
Email: dongpeng506@gmail.com  
ResearchGate: `https://www.researchgate.net/profile/Dong-Peng-4`

For questions regarding MOSART-Hg, requests for reuse, or permission to use repository-specific materials, please contact the authors before use.


～～～～～～～～～～～～～～～～～～～～～～～～～～～～～～～～
# Model for Scale Adaptive River Transport



The Model for Scale Adaptive River Transport, Mosart,
is part of the Community Earth System Model.

See the CESM web site for documentation and information:

http://www.cesm.ucar.edu
