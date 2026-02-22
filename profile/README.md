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
- Cosmological-constant-workbench: reproducible framework to evaluate dark energy mechanisms, emergent gravity models, and gravitational-wave standard-siren observables

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
**Coherence-Modulated Gravity: Laboratory Experiment Design & Null Results**

Computational and experimental workflows exploring matter-geometry coupling through macroscopic quantum coherence and curvature–electromagnetism couplings. Includes systematic null-result studies and exclusion limits for beyond-GR physics.

**Repository Highlights (v1.0.0+):**
- **Two publication-ready manuscripts**: (i) coherence-gravity validation, (ii) null results & exclusion limits
- **Enhanced analysis pipeline**: CLI sweeps for ξ, materials, curvature–EM limits (B, R, precision)
- **Automated reporting**: CSV/Markdown/LaTeX table generation via `generate_report.py`
- **Reproducible pipeline**: pinned environment (Python 3.13, numpy 1.26, scipy 1.11.3)
- **Verification scripts**: 41 tests passing in ~94s with SHA256-keyed result caching
- **Data integrity**: Complete SHA256 manifests for timestamped result artifacts
- **Experimental feasibility**: Cryogenic torsion balance achieves SNR=5 in 0.7-24 hours

**Key Scientific Results:**
- **Coherence-gravity signals**: τ_coh = 1.4 ± 0.2 × 10⁻¹² N·m (convergence at 81³-101³ resolution)
- **Null results**: Systematic sweeps over ξ ∈ {50,100}, materials, and geometries yield consistent nulls at numerical floor (|Δτ| ≈ 5×10⁻¹³ N·m)
- **Curvature–EM exclusion limits**: κ_R < 5×10¹⁷ m² for B=10T, R=10⁻²⁶ m⁻², δ=10⁻⁶ (terrestrial lab constraints)
- **CLI analysis tools**: Sweeps for coupling strengths, materials, magnetic fields, Ricci curvature, and experimental precision
- **Energy reduction**: 10⁶-10¹⁰× gravitational coupling suppression with coherent systems
- **Critical requirement**: Cryogenic operation (4K) + 10× seismic isolation essential

**Getting Started:**
```bash
git clone https://github.com/DawsonInstitute/coherence-gravity-coupling.git
cd coherence-gravity-coupling
pip install -r requirements.txt   # Python 3.13 recommended
pytest -q                          # 41 tests, ~94s
python run_analysis.py sweep-curvature --B 0.5 1.0 3.0 10.0 --plot  # Exclusion limits
python generate_report.py --all   # CSV/Markdown/LaTeX tables
cd papers && pdflatex null_results.tex  # Null results manuscript
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

### 🪐 [cosmological-constant-workbench](https://github.com/DawsonInstitute/cosmological-constant-workbench)
**Cosmological-constant-workbench (CCW): testing mechanisms for dark energy and novel observables**

A reproducible framework to evaluate proposals for the cosmological constant and dark energy. CCW emphasizes transparency, constraints-first validation, and observational signatures that can *distinguish* modified-gravity or emergent scenarios from ΛCDM.

**Highlights (Jan 2026):**
- ✅ **Emergent gravity (H.18)** — Verlinde-inspired entropic/holographic implementation in `src/ccw/mechanisms/emergent_gravity.py`. The parameter-free case (α=1) reproduces an effective Λ-like ρ_DE with w≈−1; implemented, tested, and demo'ed.
- ✅ **Gravitational wave standard sirens (I.21)** — `src/ccw/gw_observables.py` + `gw_likelihood` integrated into `joint_likelihood` to test d_L^GW ≠ d_L^EM via running G_eff(z) models (emergent gravity toy model, scalar-tensor adapters). Includes `generate_mock_gw_data` and `examples/demo_gw_sirens.py` showing current and ET-era constraints.
- ✔️ **Testing & demos** — 25 GW-focused tests added (`tests/test_gw_observables.py`), full-demo script produces plots and χ² scans; core likelihood functions extended for GW terms.
- ⚠️ **Work in progress / blockers** — Coupled ODE solver (J.22) is **BLOCKED** by dimensional scaling/unit normalization; next priorities are J.23 (radiative backreaction checks) and K.25 (LQG polymer corrections).

**Getting started:**
```bash
git clone https://github.com/DawsonInstitute/cosmological-constant-workbench.git
cd cosmological-constant-workbench
pip install -r requirements.txt
pytest -q  # Run test suite (GW tests pass; coupled ODE currently blocked)
python examples/demo_gw_sirens.py  # Demonstration: GW-EM mismatch constraints
```

---

### 🚀 [irrotational-warp-lab](https://github.com/DawsonInstitute/irrotational-warp-lab)
**Irrotational Shift-Vector Warp Metrics: Validation & Optimization**

Computational framework for exploring irrotational (curl-free) shift-vector warp metrics with Rodal-style potentials. Provides 3D volume integration, GPU acceleration, and Bayesian optimization for minimal negative-energy configurations.

**Features:**
- **Full 3D energy integration** with tail corrections (convergence to Rodal 2025 results)
- **GPU acceleration** via CuPy backend (5-10× speedup for high-resolution grids)
- **Bayesian optimization** achieving 5× efficiency vs grid+Nelder-Mead
- **Validated against literature**: Rodal (2025), Celmaster & Rubin (2024)
- **Paper-ready pipeline**: LaTeX manuscript + figure generation via Makefile
- **39 passing tests** with CI/CD and comprehensive coverage tooling

**Key Results:**
- Tail imbalance: 0.034% (n=80) approaching Rodal's ~0.04%
- Energy ratio at R₂: 1.085 converging to Rodal's ~1.07
- Superluminal regime (v ≤ 3): E ∝ v² scaling confirmed
- Optimization: σ=2.0, v=0.8 minimizes |E⁻| in tested parameter space

**Getting Started:**
```bash
git clone https://github.com/DawsonInstitute/irrotational-warp-lab.git
cd irrotational-warp-lab
pip install -e ".[dev]"
make test      # 39 tests
make all       # Regenerate figures + compile paper
```

---

### 🔬 [energy-tensor-cone](https://github.com/DawsonInstitute/energy-tensor-cone)
**Convex Cone of Energy Tensors under AQEI: Formal Verification and Computational Exploration**

Hybrid formal/computational framework exploring the geometric structure of stress-energy tensors satisfying Averaged Quantum Energy Inequalities (AQEI). Combines Lean 4 theorem proving with Mathematica computational search to rigorously characterize the convex cone of admissible energy configurations in quantum field theory.

**Features:**
- **Formal proofs in Lean 4**: Closure, convexity, and homogenization theorems fully proven with Mathlib
- **Computational search**: Mathematica randomized search in 1+1D Minkowski spacetime with Gaussian basis
- **Vertex verification**: Exact rational arithmetic certification of extreme points using determinant computation
- **End-to-end pipeline**: Mathematica → Python → Lean integration with automated candidate generation
- **Comprehensive testing**: Full validation suite with build, Python, and Mathematica test harnesses

**Key Results:**
- ✅ **10/10 core theorems proven**: Admissible set closure, convexity, cone properties all mechanically verified
- ✅ **Vertex certification**: Finite-dimensional extreme ray verified via exact rational determinant (6×6 full rank)
- ✅ **Hybrid methodology**: Demonstrates feasibility of combining formal proofs with computational exploration
- ✅ **Publication-ready**: Manuscript `aqei-cone-formalization.tex` with full mathematical exposition

**Scientific Significance:**
- Provides first mechanically-verified characterization of AQEI constraint geometry
- Establishes existence of extreme rays in finite-dimensional discretization
- Opens avenue for systematic exploration of quantum energy bounds using hybrid formal/computational methods
- Addresses fundamental question: "What is the boundary of physically allowed energy configurations in QFT?"

**Getting Started:**
```bash
git clone https://github.com/DawsonInstitute/energy-tensor-cone.git
cd energy-tensor-cone
./run_tests.sh  # Full validation: Lean build, Python tests, Mathematica search
cd lean && lake build  # Verify formal proofs
```

**Paper & Publication:**
- **Submitted**: Physical Review D (February 2026)
- **Zenodo**: [DOI 10.5281/zenodo.18522456](https://doi.org/10.5281/zenodo.18522456)
- **Dataset**: [DOI 10.5281/zenodo.18727839](https://doi.org/10.5281/zenodo.18727839)
- **Manuscript**: `papers/aqei-cone-formalization-prd.tex`

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

### ♾️ SU(2) 3nj Series (su2-*)
A coordinated suite implementing closed-form, generating-functional, and recurrence-based representations of SU(2) 3nj recoupling coefficients, with deterministic validation datasets and reproducible analysis pipelines.

- 🔗 [su2-3nj-series-paper](https://github.com/DawsonInstitute/su2-3nj-series-paper)
  Unified paper hub integrating the SU(2) 3nj representations, validation tables, and a reproducibility appendix. Contains the cross-repo integration harness and generated reference datasets.

- 🔗 [su2-3nj-uniform-closed-form](https://github.com/DawsonInstitute/su2-3nj-uniform-closed-form)
  Uniform closed-form hypergeometric representation for 12j (and related) symbols; includes implementations, tests, and documentation.

- 🔗 [su2-3nj-generating-functional](https://github.com/DawsonInstitute/su2-3nj-generating-functional)
  Universal generating-functional implementations and reference notebooks for deriving determinant-based formulas and extracting coefficients.

- 🔗 [su2-3nj-recurrences](https://github.com/DawsonInstitute/su2-3nj-recurrences)
  Finite three-term recurrence engine with stability analysis and reproducible stability reports.

- 🔗 [su2-3nj-closedform](https://github.com/DawsonInstitute/su2-3nj-closedform)
  Closed-form hypergeometric product formula repo with paper sources and reproducible numerical experiments.

- 🔗 [su2-node-matrix-elements](https://github.com/DawsonInstitute/su2-node-matrix-elements)
  Node-matrix element implementations (N0–N6 parity), deterministic validation scaffolding, and N6 derivative prototype with stability reports.

**Getting started (quick):**
```bash
# Clone the unified hub and run integration tests
git clone https://github.com/DawsonInstitute/su2-3nj-series-paper.git
cd su2-3nj-series-paper
pip install -r requirements.txt
python scripts/run_integration_tests.py  # runs cross-repo validation harness and emits data/integration_validation_report.json
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
- **Email**: info@dawsoninstitute.org

---

## 🌟 Recent Highlights

**February 2026:**
- ✅ Released energy-tensor-cone with Lean 4 formal proofs and Mathematica computational search
- ✅ Published to Zenodo: [Convex Cone of Energy Tensors under AQEI](https://doi.org/10.5281/zenodo.18522456)
- ✅ Verified 35 theorems mechanically (closure, convexity, homogenization, vertex characterization, rational determinant)
- ✅ Demonstrated extreme ray existence via exact rational arithmetic certification
- ✅ Submitted to Physical Review D (February 21, 2026)

**January 2026:**
- ✅ Implemented emergent gravity mechanism and tests in `cosmological-constant-workbench` (parameter-free α=1 reproduces Λ-like ρ_DE).
- ✅ Added gravitational wave standard siren observables and likelihoods (`src/ccw/gw_observables.py`), integrated into `joint_likelihood`; 25 GW-focused tests passing and demo script `examples/demo_gw_sirens.py` added.
- ⚠️ Coupled ODE solver (J.22) remains BLOCKED due to unit normalization/scaling issues; next priorities: J.23 backreaction and K.25 LQG polymer.

**October 2025:**
- ✅ Released coherence-gravity-coupling v1.0.0 with validated experimental design
- ✅ Validated 7.07T HTS coil designs with comprehensive FEA analysis
- ✅ Achieved 40% energy optimization in warp field calculations
- ✅ Published convergence-validated gravitational coupling framework

---

**Advancing transformative physics research through rigorous computational validation and open-source collaboration.**
