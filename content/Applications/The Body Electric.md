---
title: "The Body Electric"
---

# The Body Electric

**Weight Tracking & Trend Analysis Application**

**Status**: Live
**URL**: [body.quarterly.systems](https://body.quarterly.systems)

## Overview

The Body Electric is a health monitoring dashboard that uses EWMA (Exponentially Weighted Moving Average) methodology to track weight trends and provide calorie insights. Built with a cyberpunk aesthetic and local-first architecture, the application prioritizes data ownership and privacy while delivering sophisticated trend analysis.

The application transforms daily weight measurements into actionable insights by smoothing out daily fluctuations to reveal true trends, calculating meaningful 7-day slopes, and estimating caloric surplus or deficit based on weight changes.

## Current Features

### Weight Tracker Module (Active)

**EWMA Trend Analysis**:
- Exponentially weighted moving average smoothing
- Reduces noise from daily fluctuations (water retention, meal timing, etc.)
- Reveals true weight trends over time
- Configurable smoothing parameters

**7-Day Slope Calculations**:
- Calculates rate of weight change over rolling 7-day periods
- Displays trend direction (gaining, losing, maintaining)
- Visualizes momentum of weight changes

**Calorie Delta Insights**:
- Estimates daily caloric surplus or deficit
- Based on the principle that 3,500 calories ≈ 1 pound
- Provides feedback on energy balance
- Helps inform dietary adjustments

**Interactive Charts**:
- Built with Recharts for responsive visualizations
- Daily weight data points
- EWMA trend line overlay
- Slope indicator visualization
- Customizable date ranges

**Local-First Storage**:
- All data stored locally via Fireproof database
- IndexedDB persistence in browser
- No server required for data storage
- Complete data ownership and privacy
- Automatic CRDT (Conflict-free Replicated Data Type) synchronization

### Planned Modules (Offline)

The full "Bio Systems Monitor" vision includes additional tracking capabilities:

- **Activity Monitor**: Exercise and movement tracking
- **Nutrition Logger**: Food intake and macro tracking
- **Biometric Scan**: Comprehensive health metrics dashboard

## Technical Architecture

### Technology Stack

**Frontend**:
- React 18 with TypeScript
- Vite build system for fast development
- Tailwind CSS for styling
- Cyberpunk/futuristic UI design system

**Data Layer**:
- Fireproof CRDT database
- IndexedDB for browser persistence
- Local-first architecture
- No backend required for core functionality

**Visualization**:
- Recharts library for interactive charts
- Real-time data updates
- Responsive design for mobile and desktop

**Build & Deploy**:
- Cloudflare Pages hosting
- Automatic deployment on git push
- Requires `--legacy-peer-deps` for npm install

### EWMA Algorithm

The core of The Body Electric's trend analysis uses Exponentially Weighted Moving Average:

```
EWMA_today = α × Weight_today + (1 - α) × EWMA_yesterday
```

Where:
- `α` (alpha) is the smoothing factor (typically 0.1-0.3)
- Higher α = more responsive to recent changes
- Lower α = smoother trend line, less noise

This approach gives more weight to recent measurements while still considering historical data, providing a balanced view of true weight trends versus daily fluctuations.

### Calorie Calculations

Based on the physiological principle that approximately 3,500 calories equals one pound of body weight:

```
Daily_Calorie_Delta = (Weight_Change_lbs × 3,500) / Days_Elapsed
```

This provides an estimate of daily caloric surplus (gaining) or deficit (losing) to help users understand their energy balance.

## Design Philosophy

### Cyberpunk Aesthetic

The interface features a distinctive "Bio Systems Monitor" design:
- Full body scan visualization with targeting reticles
- Cyan text on black background
- Grid overlays and scanline effects
- Animated scanning lines
- Futuristic dashboard layout
- Modular app organization (Weight Tracker, Activity Monitor, etc.)

### Privacy-First Approach

- **Local-first architecture**: All data stays on your device
- **No account required**: Start tracking immediately
- **No server uploads**: Your health data never leaves your browser
- **Complete control**: Export, delete, or manage data as you wish
- **Fireproof sync**: Optional peer-to-peer sync without central servers

## Use Cases

**Personal Weight Management**:
- Track long-term weight trends
- Cut through daily noise (water weight, meal timing)
- Make data-driven dietary decisions
- Monitor progress toward health goals

**Fitness & Body Composition**:
- Track weight changes during bulk/cut cycles
- Monitor trend direction during training programs
- Correlate weight with performance metrics
- Maintain accountability

**Health Monitoring**:
- Long-term health trend visibility
- Early detection of concerning changes
- Supplement medical weight management programs
- Personal health record keeping

## Roadmap & Next Steps

### Phase 1: Enhanced Weight Tracking + Stack Basics (Q1 2025)

**Data Export & Import**:
- CSV export for analysis in other tools
- Import historical data from other apps
- Backup and restore functionality
- Data portability features

**Advanced Analytics**:
- Multiple EWMA timeframes (7-day, 14-day, 30-day)
- Customizable smoothing parameters
- Statistical analysis (variance, standard deviation)
- Trend prediction and forecasting

**Goal Setting**:
- Set target weight goals
- Calculate required daily deficit/surplus
- Progress tracking toward goals
- Milestone celebrations

**The Stack - Initial Release**:
- Simple supplement/medication tracker
- Daily logging interface (checkboxes for "took it today")
- Basic stack composition (name, dosage, timing)
- Notes field for each item
- Active stack view
- Simple adherence tracking (% of days taken)
- *Note: This is a minimal viable version; full Stack features in Phase 3*

**Performance Enhancement Database - Initial Release**:
- WADA Prohibited List index (2025 edition as baseline)
- Substance categorization browser
- Basic substance profiles (category, potential benefits, mechanism)
- Research notes field for each substance
- "Considering" vs "Researched" vs "Dismissed" status tracking
- Safety/legality disclaimer system
- *Note: For research and educational purposes; non-competitive context only*

**Healthcare Basics - Initial Release**:
- Simple visit log (date, doctor, reason, notes)
- Lab results quick-entry (date, test name, value, reference range)
- Document upload (store PDFs/images of lab reports)
- Basic timeline view of medical events
- Quick notes for tracking symptoms or concerns
- *Note: This is a minimal viable version; full Healthcare features in Phase 4*

### Phase 2: Activity Monitor Integration (Q2 2025)

**Exercise Tracking**:
- Log workouts and activities
- Track exercise calories burned
- Correlate activity with weight trends
- Weekly activity load scoring

**Movement Data**:
- Daily step tracking
- Active minutes monitoring
- Integration with fitness wearables (optional)
- Movement pattern analysis

**Performance Metrics**:
- VO2 max estimation
- Heart rate monitoring integration
- Recovery metrics
- Training load management

### Phase 3: Nutrition & Stack Tracker (Q3 2025)

**The Stack - Supplements & Medications**:
- Daily supplement logging (vitamins, minerals, nootropics, etc.)
- Prescription medication tracking
- Dosage and timing records
- Stack composition management
- Brand and form tracking (pills, powder, liquid)
- Cost tracking per supplement
- Adherence monitoring (did you take it?)
- Interaction warnings and contraindications
- Effectiveness notes and subjective feedback
- Schedule management (AM/PM, with meals, etc.)

**Stack Analytics**:
- Adherence percentage over time
- Cost analysis (monthly/yearly spend)
- Correlation with biometric data (does X supplement correlate with better sleep/weight/etc?)
- Stack history and changes over time
- "Active stack" vs "past experiments"
- Efficacy tracking (which supplements seem to help?)

**Food & Beverage Tracking**:
- Quick-add meal logging (simple "ate X" without full macros)
- General food intake tracking (breakfast, lunch, dinner, snacks)
- Beverage consumption (water, coffee, alcohol, etc.)
- Meal timing analysis
- Food mood/energy correlation
- Simple food diary (what/when, not necessarily calories)
- Photo logging (optional visual record)

**Detailed Nutrition (Optional)**:
- Macro tracking (protein, carbs, fats) for those who want it
- Calorie intake monitoring
- Micronutrient tracking
- Recipe and meal planning

**Nutritional Insights**:
- Compare intake vs. calorie delta calculations
- Identify eating patterns
- Macro ratio optimization (if tracking)
- Nutritional balance scoring
- Stack impact on nutrition (e.g., vitamins covering deficiencies)

**Integration**:
- Connect weight trends with nutrition data
- Correlate supplement stack with biometric changes
- Analyze relationship between diet and weight changes
- Track supplement effects on sleep, energy, mood
- Identify patterns (e.g., coffee intake vs sleep quality)
- Personalized recommendations based on stack + metrics

### Phase 3.5: Performance Enhancement Research Database (Q3 2025)

**IMPORTANT DISCLAIMER**: This feature is designed for educational research and informed decision-making in a non-competitive context. Users are not athletes subject to WADA regulations. All substances should be researched thoroughly for safety, legality in your jurisdiction, and potential health impacts before consideration.

**WADA Prohibited List Integration**:
- Complete 2025 WADA Prohibited List database (all categories)
- Annual updates as new lists are published
- Categorized browser by substance class:
  - S0: Non-approved substances (BPC-157, DNP, etc.)
  - S1: Anabolic agents (AAS, SARMs, etc.)
  - S2: Peptide hormones & growth factors (EPO, GH, IGF-1, etc.)
  - S3: Beta-2 agonists
  - S4: Hormone & metabolic modulators
  - S5: Diuretics & masking agents
  - S6: Stimulants
  - S7: Narcotics
  - S8: Cannabinoids
  - S9: Glucocorticoids
  - P1: Beta-blockers
  - M1-M3: Prohibited methods

**Substance Research Profiles**:
For each substance, track:
- **WADA category & classification**
- **Chemical name & common names/aliases**
- **Mechanism of action** (how it works)
- **Potential benefits** (why athletes use it; why it might be useful for non-competitive optimization)
- **Known risks & side effects**
- **Therapeutic uses** (legitimate medical applications)
- **Legal status** (by jurisdiction - prescription required, controlled substance, etc.)
- **Research links** (PubMed, studies, medical literature)
- **Personal research notes** (your findings and thoughts)
- **Consideration status**: Research Only / Considering / Consulting Doctor / Dismissed / Currently Using

**Use Case Analysis**:
Understand why substances are prohibited in competition and what benefits they might provide for non-competitive personal optimization:

- **Anabolic Agents** (S1): Muscle building, recovery, body composition
  - Testosterone & derivatives: Hormone optimization, muscle mass, recovery
  - SARMs: Targeted muscle/bone benefits with potentially fewer side effects
  - DHEA: Hormone precursor, aging, vitality

- **Peptide Hormones & Growth Factors** (S2): Recovery, healing, performance
  - Growth Hormone (GH): Anti-aging, recovery, body composition, sleep quality
  - IGF-1: Muscle growth, recovery, tissue repair
  - BPC-157: Tissue healing, gut health, injury recovery (non-approved)
  - TB-500 (Thymosin-β4): Healing, inflammation, tissue repair
  - EPO: Endurance, oxygen delivery (also medical: anemia treatment)

- **Metabolic Modulators** (S4): Energy, metabolism, body composition
  - GW1516 (Cardarine): Endurance, fat loss, metabolic health
  - AICAR: AMPK activation, endurance, metabolic benefits
  - Insulin: Nutrient partitioning, muscle building (with risks)
  - Meldonium: Cardioprotection, endurance

- **Beta-2 Agonists** (S3): Fat loss, muscle preservation
  - Clenbuterol: Fat loss, muscle preservation, metabolic rate
  - Salbutamol: Respiratory function (also therapeutic for asthma)

- **Stimulants** (S6): Energy, focus, performance
  - Modafinil/Adrafinil: Wakefulness, cognitive enhancement
  - Various amphetamines: Focus, energy, appetite suppression
  - Ephedrine: Energy, fat loss, performance

- **Glucocorticoids** (S9): Inflammation, recovery
  - Dexamethasone, Prednisone, etc.: Anti-inflammatory, recovery (also therapeutic)

- **Nootropics & Cognitive Enhancers**:
  - Fonturacetam (4-phenylpiracetam): Cognitive function, physical performance
  - Various racetams: Memory, learning, cognitive performance

**Safety & Legality Research Tools**:
- Jurisdiction-based legality checker (US, UK, EU, etc.)
- Prescription requirement flags
- Controlled substance schedules (DEA scheduling, etc.)
- Known drug interactions checker
- Contraindication warnings
- Clinical study repository links
- Dosing information from medical literature
- Half-life and detection time data

**Risk Assessment Framework**:
For each substance, evaluate:
- **Health risk level**: Low / Medium / High / Very High
- **Legal risk level**: Legal / Prescription Required / Controlled / Illegal
- **Evidence quality**: Well-studied / Some studies / Limited research / Anecdotal only
- **Reversibility**: Fully reversible / Mostly reversible / Partially irreversible / Permanent effects
- **Dependencies**: Risk of dependence (physical/psychological)
- **Cost-benefit ratio**: Personal assessment notes

**Medical Consultation Tracking**:
- Track which substances you've discussed with doctors
- Record doctor opinions and recommendations
- Link to lab tests that might be relevant (e.g., hormone panels before TRT consideration)
- Note any prescribed alternatives or legitimate therapeutic pathways

**Personal Experimentation Log** (if proceeding with medical supervision):
- Substance being used
- Dosing protocol
- Start/end dates
- Supervising physician information
- Baseline metrics (labs, vitals, performance)
- Ongoing tracking metrics
- Subjective effects (energy, mood, recovery, etc.)
- Side effects experienced
- Outcome assessment

**Research Library**:
- Link to scientific papers and studies
- Medical literature references
- Community experiences (forums, blogs - with healthy skepticism)
- Expert opinions (doctors, researchers)
- Risk assessment reports
- Regulatory agency statements (FDA, DEA, etc.)

**Correlation with Biometrics**:
- If using any performance-enhancing substances under medical supervision, correlate with:
  - Weight and body composition changes
  - Lab results (hormone panels, metabolic markers, etc.)
  - Activity and performance metrics
  - Sleep and recovery data
  - Mood and energy levels
  - Long-term health markers

**Ethical Framework**:
- Clear distinction: Not competing in sports where these substances are banned
- Medical supervision emphasis for anything beyond basic supplements
- Harm reduction approach
- Informed consent and personal autonomy
- Transparency about risks

**Example Substances of Interest for Non-Competitive Use**:

*Muscle Building & Body Composition*:
- Testosterone replacement therapy (TRT) - legitimate medical use for hypogonadism
- SARMs (e.g., Ostarine, LGD-4033) - research for muscle preservation
- DHEA - hormone precursor, OTC in US
- Growth Hormone - anti-aging, recovery (requires medical supervision)

*Recovery & Healing*:
- BPC-157 - peptide for tissue repair and gut health (research only, not approved)
- TB-500 - healing and recovery peptide
- Growth hormone secretagogues - natural GH enhancement

*Metabolic & Fat Loss*:
- GW1516 (Cardarine) - metabolic health and endurance
- Clenbuterol - fat loss (requires caution)
- Metformin - metabolic health, longevity (prescription for diabetes)

*Cognitive & Performance*:
- Modafinil - wakefulness and focus (prescription for narcolepsy)
- Phenylpiracetam - cognitive enhancement and physical performance

*Longevity & Health*:
- Metformin - anti-aging, metabolic health
- Rapamycin - mTOR inhibition, longevity research
- NAD+ precursors - cellular health

### Phase 4: Healthcare Integration & Biometric Dashboard (Q4 2025)

**Medical Visits & Appointments**:
- Doctor visit logging (date, provider, type)
- Visit notes and summaries
- Chief complaints and diagnoses
- Treatment plans and recommendations
- Follow-up scheduling and reminders
- Provider directory (doctors, specialists, clinics)
- Visit history timeline
- Appointment preparation checklists
- Questions to ask doctor (pre-visit planning)
- Post-visit action items

**Lab Results Tracking**:
- Upload and store lab reports (PDF, images, manual entry)
- Key biomarker tracking over time:
  - Blood panel (CBC, CMP, lipid panel)
  - Hormone levels (testosterone, thyroid, cortisol, etc.)
  - Vitamins and minerals (D, B12, iron, magnesium, etc.)
  - Metabolic markers (A1C, fasting glucose, insulin)
  - Inflammation markers (CRP, homocysteine)
  - Liver and kidney function
  - Custom markers
- Reference ranges and out-of-range alerts
- Trend visualization (how has X changed over time?)
- Lab comparison (this year vs last year)
- Lab result notifications
- Correlation with lifestyle changes

**Prescriptions & Medical Orders**:
- Prescription tracking (what was prescribed when)
- Medication history (separate from daily stack adherence)
- Dosage changes over time
- Prescription renewals and refills
- Medical device orders (CPAP, CGM, etc.)
- Referrals to specialists
- Medical imaging orders (X-rays, MRI, etc.)

**Healthcare Documents**:
- Store medical records securely
- Upload lab reports, imaging results, discharge summaries
- Vaccination records
- Allergy and adverse reaction history
- Family medical history
- Insurance information
- Medical release forms and consent documents
- OCR text extraction from documents for searchability

**Provider Notes & Recommendations**:
- Track what your doctor recommended
- Diet and lifestyle recommendations
- Exercise prescriptions
- Supplement recommendations from providers
- Correlation: did following recommendation X improve metric Y?

**Vital Signs Monitoring**:
- Blood pressure tracking (with timestamp and context)
- Resting heart rate
- Heart rate variability (HRV)
- Sleep quality metrics
- Temperature tracking
- Oxygen saturation (SpO2)
- Peak flow (for respiratory tracking)

**Body Composition**:
- Body fat percentage
- Muscle mass estimates
- BMI calculations
- Body measurements (waist, neck, chest, etc.)
- DEXA scan results
- Body composition trends

**Metabolic Health**:
- Glucose level tracking (finger stick or CGM)
- Resting metabolic rate estimation
- Hydration monitoring
- Stress level indicators
- Ketone tracking

**Healthcare Analytics**:
- Correlate lab results with weight, stack, activity
- Track biomarker improvement over time
- Identify patterns (e.g., vitamin D low in winter)
- Lab-based supplement recommendations (e.g., low B12 → add supplement)
- Medical timeline view (everything that happened medically)
- Before/after analysis (started medication X, biomarker Y improved)

**Full Dashboard**:
- Activate all "offline" modules
- Unified health dashboard view
- Cross-metric correlations (lab results + weight + stack + activity)
- Comprehensive health reporting
- Export health summary for doctor visits
- Timeline view of all health events

### Phase 5: Advanced Features (2026)

**AI & Predictions**:
- Machine learning trend predictions
- Anomaly detection (unusual weight changes)
- Pattern recognition in health data
- Personalized insights and recommendations

**Social & Community**:
- Optional peer-to-peer data sharing
- Accountability partnerships
- Progress sharing (privacy-controlled)
- Community challenges and support

**Integrations**:
- Fitness device APIs (Garmin, Fitbit, Apple Health, etc.)
- Smart scale integration
- Health app ecosystem connections
- Medical record integration (FHIR standard)

**Research & Insights**:
- Aggregated anonymous insights
- Contribution to health research
- Personal health reporting
- Longitudinal health analysis

## Development Notes

**Installation**:
```bash
npm install --legacy-peer-deps
```

**Local Development**:
```bash
npm run dev  # Starts on :5173
```

**Building**:
```bash
npm run build
```

**Deployment**:
- Auto-deploys to Cloudflare Pages on push to main branch
- Production URL: [body.quarterly.systems](https://body.quarterly.systems)

## Known Limitations

- Currently only weight tracking is active (other modules planned)
- Requires `--legacy-peer-deps` due to Fireproof dependency versions
- Browser-based only (no native mobile apps yet)
- No multi-device sync without manual data export/import (planned for Fireproof sync)

## Related Documentation

- [[Applications|Applications Overview]]
- Parent company: [[Company/KmikeyM|KmikeyM]]
- Platform: [[Applications#Primary Applications|Quarterly Systems]]

---

*Part of the [[index|Quarterly Knowledge Base]]*
