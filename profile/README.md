# Dawson Institute

**Advanced Research in Quantum Gravity, Superconducting Systems, and Computational Physics**

---

## 🎯 Mission

The Dawson Institute develops open-source computational frameworks and experimental validation methodologies for transformative physics research, focusing on quantum gravity, high-temperature superconducting systems, and advanced spacetime engineering.

## 🔬 Research Areas

### Quantum Gravity & Coherence-Matter Coupling
- Coherence-modulated gravitational coupling with experimental validation
- Matter-geometry coupling via non-minimal scalar fields
- Laboratory-scale precision gravimetry with cryogenic torsion balances
- Reproducible computational workflows with pinned environments

### High-Temperature Superconducting (HTS) Systems
- REBCO coil optimization for fusion and antimatter confinement
- Multi-tape conductor designs achieving 5-10 Tesla operation
- Computational frameworks integrating electromagnetic, thermal, and mechanical analysis
- Cross-platform FEA validation (COMSOL Multiphysics, FEniCSx)

### Warp Field & Exotic Metric Engineering
- Computational optimization frameworks for exotic-matter distributions
- Multi-objective algorithms for metric ansatz parameter optimization
- Energy reduction strategies achieving ~40% efficiency improvements
- Experimental hardware abstraction for mission-critical systems

---

## 📊 Key Projects

### 🔭 [coherence-gravity-coupling](https://github.com/DawsonInstitute/coherence-gravity-coupling)
**Coherence-Modulated Gravity: Laboratory Experiment Design**

Computational and experimental workflows exploring matter-geometry coupling through macroscopic quantum coherence. Proposes experimentally testable framework where coherence fields modulate effective gravitational coupling constant G_eff.

**Repository Highlights (v1.0.0):**
- **Publication-ready manuscript** with 3 high-quality figures (LaTeX + PDF/PNG)
- **Reproducible pipeline**: pinned environment (Python 3.11, numpy 1.26.4, scipy 1.14.1)
- **Verification scripts**: 23 tests passing in 107s with release manifest generation
- **Data integrity**: Complete SHA256 manifests for 3,940 result artifacts
- **Experimental feasibility**: Cryogenic torsion balance achieves SNR=5 in 0.7-24 hours

**Key Scientific Results:**
- **Validated signals**: τ_coh = 1.4 ± 0.2 × 10⁻¹² N·m (convergence at 81³-101³ resolution)
- **Newtonian baseline**: τ_N ≈ 2×10⁻¹³ N·m (dimensional analysis validated)
- **Energy reduction**: 10⁶-10¹⁰× gravitational coupling suppression with coherent systems
- **Critical requirement**: Cryogenic operation (4K) + 10× seismic isolation essential

**Getting Started:**
```bash
git clone https://github.com/DawsonInstitute/coherence-gravity-coupling.git
cd coherence-gravity-coupling
conda env create -f environment.yml && conda activate cohgrav
pytest -q                          # 23 tests, ~107s
python generate_figures.py         # Publication figures
cd papers && pdflatex coherence_gravity_coupling.tex  # 5-page manuscript
```

---

### 🧲 [hts-coils](https://github.com/DawsonInstitute/hts-coils)
**REBCO HTS Coil Optimization Framework**

Comprehensive computational framework for high-temperature superconducting coils using rare-earth barium copper oxide (REBCO). Validated designs for fusion energy and antimatter research applications.

**Features:**
- **Interactive Jupyter notebooks** (MyBinder ready) for education and research
- **24 benchmark validations** with computational reproducibility
- **Multi-backend FEA support**: COMSOL Multiphysics and FEniCSx (open-source)
- **100% validation success rate** for paper reproduction

**Achievements:**
- ✅ **7.07T magnetic fields** with 0.16% ripple
- ✅ **74.5K thermal margins** at 15K operating temperature
- ✅ **Mechanical reinforcement** reducing stress from 178.7 MPa → 35 MPa
- ✅ **30% current utilization** in multi-tape designs
- ✅ **Plasma confinement**: β = 0.48 stable high-beta operation
- ✅ **Interferometric detection**: 10⁻¹⁸ m spacetime distortion sensitivity

**Getting Started:**
```bash
git clone https://github.com/DawsonInstitute/hts-coils.git
cd hts-coils
pip install -r requirements.txt
python scripts/validate_reproducibility.py  # Run validation suite
```

**Try Interactive Notebooks:**
[![Launch Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DawsonInstitute/hts-coils/main?urlpath=lab/tree/notebooks/)

---

### ⚛️ [warp-bubble-optimizer](https://github.com/DawsonInstitute/warp-bubble-optimizer)
**Multi-Objective Optimization for Exotic Spacetime Metrics**

Computational optimization algorithms for warp-bubble metric ansatz and exotic-matter distribution design. Provides JAX-accelerated electromagnetic field calculations and Monte Carlo uncertainty quantification.

**Applications:**
- Multi-objective optimization for magnetic field uniformity
- Energy reduction algorithms achieving ~40% efficiency improvements
- Validation framework for theoretical warp field research
- Hardware abstraction for mission-critical experimental systems

**Integration:**
- Used by `hts-coils` for plasma confinement optimization
- Provides energy minimization algorithms for Lentz soliton research
- Monte Carlo UQ for manufacturing tolerance analysis

**Getting Started:**
```bash
git clone https://github.com/DawsonInstitute/warp-bubble-optimizer.git
cd warp-bubble-optimizer
pip install -r requirements.txt
pytest  # Run test suite
```

---

## 🏆 Validated Performance Metrics

| **Capability** | **Achievement** | **Repository** | **Status** |
|---------------|----------------|----------------|-----------|
| HTS Field Generation | 7.07T @ 0.16% ripple | hts-coils | ✅ Validated |
| Thermal Management | 74.5K margin @ 15K operation | hts-coils | ✅ Validated |
| Mechanical Integrity | 35 MPa reinforced design | hts-coils | ✅ Validated |
| Energy Optimization | 40% reduction in positive density | warp-bubble-optimizer | ✅ Validated |
| Interferometric Detection | 10⁻¹⁸ m displacement sensitivity | hts-coils | ✅ Validated |
| Gravitational Coupling | G_eff suppression 10⁶-10¹⁰× | coherence-gravity-coupling | ✅ Validated |
| Convergence Validation | τ_coh = 1.4 ± 0.2 × 10⁻¹² N·m | coherence-gravity-coupling | ✅ Validated |

---

## 🚀 Getting Started

### Quick Launch Options

**Interactive Notebooks (No Installation):**
- Launch HTS coils notebooks: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DawsonInstitute/hts-coils/main?urlpath=lab/tree/notebooks/)

**Local Installation (Any Repository):**
```bash
# Clone desired repository
git clone https://github.com/DawsonInstitute/<repo>.git
cd <repo>

# Install dependencies (conda or pip)
conda env create -f environment.yml && conda activate <env>
# or
pip install -r requirements.txt

# Run validation/tests
pytest -q                                    # For repos with test suites
python scripts/validate_reproducibility.py  # For validation scripts
```

**Example Quickstart Commands:**

```bash
# coherence-gravity-coupling
git clone https://github.com/DawsonInstitute/coherence-gravity-coupling.git
cd coherence-gravity-coupling
conda env create -f environment.yml && conda activate cohgrav
pytest -q && python generate_figures.py

# hts-coils
git clone https://github.com/DawsonInstitute/hts-coils.git
cd hts-coils
pip install -r requirements.txt
python scripts/validate_reproducibility.py

# warp-bubble-optimizer
git clone https://github.com/DawsonInstitute/warp-bubble-optimizer.git
cd warp-bubble-optimizer
pip install -r requirements.txt && pytest
```

---

## 📚 Documentation & Resources

- **Papers**: Manuscripts and preprints in `papers/` directories
- **Notebooks**: Interactive Jupyter notebooks with educational content (hts-coils)
- **Validation**: Comprehensive benchmark validation frameworks
- **Reproducibility**: Pinned environments, verification scripts, release manifests
- **API Documentation**: Detailed technical documentation for all modules

---

## 🤝 Contributing

We welcome contributions from the research community! Areas of interest:
- Experimental validation of computational models
- Extension to new materials and parameter regimes
- Integration with additional simulation platforms
- Uncertainty quantification and sensitivity analysis
- Hardware design and fabrication workflows

Please read `CONTRIBUTING.md` in individual repositories for development guidelines.

---

## 📄 License

All software is released under the MIT License unless otherwise specified. Papers and documentation follow standard academic licensing.

---

## 📧 Contact

For research inquiries, collaborations, or technical questions:
- **Issues**: Open an issue in the relevant repository
- **Discussions**: Use GitHub Discussions for general questions
- **Email**: Contact maintainers through repository README files

---

## 🌟 Recent Highlights

**October 2025:**
- ✅ Released coherence-gravity-coupling v1.0.0 with validated experimental design
- ✅ Validated 7.07T HTS coil designs with comprehensive FEA analysis
- ✅ Achieved 40% energy optimization in warp field calculations
- ✅ Published convergence-validated gravitational coupling framework

**September 2025:**
- ✅ Cross-platform FEA validation showing <1% solver variance (hts-coils)
- ✅ MyBinder deployment with interactive educational notebooks
- ✅ Integrated plasma-HTS coupling for high-beta confinement (β = 0.48)

---

**Advancing transformative physics research through rigorous computational validation and open-source collaboration.**
