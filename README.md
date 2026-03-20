# The definitive catalog of healthcare UI libraries and design systems

**Over 75 healthcare-specific UI libraries, design systems, and frontend frameworks exist today** — spanning open-source FHIR component libraries, proprietary EHR vendor systems, government health service design systems, medical imaging toolkits, and digital health company frameworks. The ecosystem is fragmented and overwhelmingly React-dominant, with most mature offerings concentrated in open-source projects and government initiatives. No single library has achieved the universal adoption that Bootstrap or Material UI enjoy in general web development, making this catalog essential for any team building healthcare software.

The healthcare UI landscape divides into clear tiers: a handful of actively maintained, production-grade systems (NHS Design System, CMS Design System, OpenMRS 3.0, Medplum, OHIF Viewer); several well-engineered but proprietary or archived systems (Terra UI, Edison, SHUI); and a long tail of specialized or niche tools for FHIR forms, medical imaging, clinical terminology, and openEHR data capture.

-----

## The 11 requested libraries: current status and details

### 1. PulseTile — Dormant since January 2023

PulseTile is an open-source UI framework for healthcare  created by the **Ripple Foundation**, a non-profit based in Leeds, UK, led by Dr. Tony Shannon. It follows a clinically-led List/Detail/Modal navigation pattern inspired by the NHS Common User Interface guidelines. 

- **Framework:** Multiple versions exist — AngularJS  (legacy, 19 stars), React Core (11 stars), **PulseTile-RA** (React Admin-based, 5 stars, most recent), Vue.js and Web Components (placeholders only)
- **License:** Apache 2.0 across all repos
- **GitHub:** github.com/PulseTile (12 repos) and github.com/RippleOSI (27 repos)
- **FHIR/openEHR:** Designed to work with EtherCIS openEHR backend via QEWDjs middleware; FHIR support was exploratory only
- **Components:** ~8–10 clinical tiles (Allergies, Medications, Problems/Diagnoses, Vitals, Contacts, Clinical Notes, Events, Vaccinations)
- **Status:** **Effectively dormant.** Last commits date to January 2023. The Ripple Foundation website remains live but offers no free support. The org has only 4 GitHub followers.
- **Notable users:** Leeds City Council / Yorkshire & Humber region (Helm PHR),  projects in Finland, Germany, India 
- **Docs:** docs.pulsetile.com

### 2. Terra UI (Cerner/Oracle Health) — Archived and abandoned

Terra UI was Cerner’s healthcare-focused React component library,   one of the most comprehensive open-source healthcare UI frameworks ever built. **Oracle archived the entire `cerner` GitHub organization on June 28, 2024.** All repos are read-only. 

- **Framework:** React (rewritten from internal “Blue Steel” library in 2017)
- **License:** Apache 2.0
- **GitHub repos:** terra-core (**183 stars**,  ~40+ packages),   terra-framework (~20+ packages), terra-clinical (~9 packages),  terra-toolkit, terra-application
- **Total components:** **~70+ packages** across three monorepos covering layout, forms, navigation, feedback, clinical data display
- **Clinical-specific packages:** terra-clinical-data-grid, terra-clinical-detail-view, terra-clinical-header, terra-clinical-item-collection, terra-clinical-item-display, terra-clinical-item-view, terra-clinical-label-value-view, terra-clinical-onset-picker, terra-clinical-result 
- **Accessibility:** Built for WCAG 2.0 AA and Section 508; axe-core integrated into testing pipeline;  clinical-lowlight-theme for clinical environments
- **i18n:** 17 locales supported via react-intl;  RTL support via postcss-rtl; terra-aggregate-translations pre-build tool 
- **Status:** **Dead.** All repos archived May–June 2024. Oracle is building an entirely new cloud-native EHR from scratch on Oracle Cloud Infrastructure, announced October 2024 and debuted August 2025.  No replacement open-source design system exists.
- **Docs:** engineering.cerner.com/terra-ui/ (may become unavailable)

### 3. Edison Design System (GE HealthCare) — Active, proprietary

Edison Design System (EDS) is GE HealthCare’s purpose-built healthcare design system,   winner of the **Red Dot Interface Award (2020)** and **DMI Design Value Award (2020, 2025)**.

- **Framework:** Proprietary code snippets for web, tablet, mobile, and embedded medical device screens; Sketch toolkit for designers
- **License:** Proprietary — publicly viewable at edisondesignsystem.com but not open-source
- **GitHub:** github.com/GEHealthcare has **zero public repositories** 
- **Components:** **33 reusable components** with **12 foundational directories**  and **3,000+ icons** (each in 3 sizes)
- **Healthcare features:** Patient banner, medical specialty icons, AI imaging guidelines, custom color palettes optimized for clinical lighting conditions  (radiology reading rooms, ORs, ICUs), three themes, step-by-step clinical wizards, extensible data grids
- **Status:** **Active internally.** Supported by 2,000+ designers and developers at GE HealthCare (GEHC, NYSE). The company spun off from GE in January 2023  as a ~$20B revenue independent company.
- **Docs:** edisondesignsystem.com (some content requires authentication)

### 4. SHUI (Siemens Healthineers) — Active, proprietary

SHUI® (Siemens Healthineers User Interface) is a registered trademark and Siemens Healthineers’ dedicated design system, **entirely separate from Siemens iX** (the open-source industrial design system from Siemens AG).

- **Framework:** Angular, React, Vue.js (confirmed from job postings); supports desktop, tablet, mobile, and embedded hardware UIs 
- **License:** Fully proprietary and internal — no public GitHub repos, no npm packages
- **Healthcare features:** Light/dark mode for clinical lighting, Hygienic Design Concept for medical devices, Touch User Interface patterns for imaging equipment tube heads, context-specific content display for clinical workflows
- **Status:** **Active and growing.** Job postings from 2025 seek SHUI designers and developers in Bratislava. Described as “the go-to design system for developing new products at Siemens Healthineers.” Won Red Dot and UX Design Awards.
- **Related:** Siemens iX (github.com/siemens/ix, **331 stars**, MIT license, React/Angular/Vue/Web Components/Blazor) is the open-source industrial Siemens system — actively maintained at v4.3.0 but not healthcare-specific
- **Docs:** shui.siemens-healthineers.com (login required), ux.siemens-healthineers.com (public overview)

### 5. SAP OpenUI5-FHIR — Open-source FHIR data binding for SAP UI5

SAP’s contribution to healthcare UI is not a standalone design system but a **FHIR data-binding library** connecting SAP’s UI5/Fiori ecosystem to HL7 FHIR servers. 

- **Framework:** OpenUI5/SAPUI5 (SAP’s enterprise web framework)
- **License:** Apache 2.0
- **GitHub:** github.com/SAP/openui5-fhir — **34 stars**, 315 commits, 40 releases
- **npm:** `openui5-fhir`  (latest v2.4.0, May 2024)
- **Features:** FHIRModel (analogous to ODataModel but for FHIR), FHIRContextBinding, FHIRPropertyBinding,  FHIRListBinding, FHIRTreeBinding; FHIR R4 support; automatic request batching; manifest.json configuration
- **Status:** **Low-to-moderate activity.** Last release May 2024. SAP’s broader healthcare play is SAP Health Data Services for FHIR (GA late 2023) on SAP BTP.
- **Docs:** sap.github.io/openui5-fhir/

### 6. Medblocks UI — Active open-source openEHR form generator

Medblocks UI is an open-source Web Components library  focused on **auto-generating forms from openEHR web templates**,  maintained by Medblocks, an Indian healthcare company founded by Sidharth Ramesh.

- **Framework:** Web Components built with Lit-Element + Shoelace;  works with React, Vue, Angular, Svelte, or any framework 
- **License:** Apache 2.0
- **GitHub:** github.com/medblocks/medblocks-ui — **69 stars**,  688 commits
- **npm:** `medblocks-ui` (v0.0.217,  updated ~January 2026, ~44 weekly downloads) 
- **Components:** **21 documented components** including mb-auto-form, mb-fhir-form, mb-form, mb-input, mb-select, mb-date, mb-quantity, mb-search, mb-duration, mb-proportion, mb-context, mb-submit
- **Key differentiator:** `mb-auto-form` generates complete forms from openEHR web templates — the primary open-source alternative to Better’s EHR Studio 
- **Status:** **Actively maintained.** VSCode extension available.  Used with EHRbase-based setups.
- **Docs:** medblocks.com/docs/medblocks-ui

### 7. NHS Design System — Production-grade, the gold standard for health service design

The NHS Design System is the most mature, well-documented government healthcare design system,   maintained by **NHS England** and based on the GOV.UK Design System adapted for health contexts.

- **Framework:** Nunjucks/HTML/CSS/JS (nhsuk-frontend); React wrappers (nhsuk-react-components)
- **License:** Code: MIT; Documentation: Open Government Licence v3.0 
- **GitHub:** nhsuk-frontend — **664 stars**,  6,818 commits, 79 releases, **925 dependents**; nhsuk-react-components — **70 stars**,  v6.0.0 (March 10, 2026)
- **Current version:** **v10.3.1** (January 19, 2026)
- **Components:** **38 components** including 4 health-specific: Care Cards (3 severity levels), Do and Don’t Lists (clinical guidance), Review Date (medical content freshness), Warning Callout (important health warnings) 
- **WCAG:** **2.2 Level AA** mandatory, AAA aspirational 
- **Content guidelines:** Extensive health literacy guidance targeting reading age 9–11; inclusive language for health contexts; guidance on writing about medicines, treatments, and conditions
- **Status:** **Very active.** NHS App has its own extension (nhsapp-frontend).   Prototype kit available. React components actively seeking new maintainers. 
- **Docs:** service-manual.nhs.uk

### 8. CMS Design System — US government healthcare standard

The CMS Design System serves the **Centers for Medicare & Medicaid Services**, powering HealthCare.gov and Medicare.gov with React components built on the US Web Design System.

- **Framework:** React (primary), Preact, Web Components (growing subset), HTML/CSS
- **License:** Public domain (US Government work)
- **GitHub:** github.com/CMSgov/design-system — **354 stars**,  2,619 commits, 228 releases
- **Current version:** **13.2.0** (January 28, 2026)
- **npm:** `@cmsgov/design-system`, `@cmsgov/ds-healthcare-gov`, `@cmsgov/ds-medicare-gov`
- **Components:** **~40+ components** with 4 themes (Core, CMS.gov, Healthcare.gov, Medicare.gov)
- **Healthcare patterns:** Enrollment flows, plan comparison with star ratings, Idle Timeout for security-sensitive health sessions, masked fields for SSN/phone, Third Party External Link disclaimers, Step List for multi-step enrollment
- **Accessibility:** Section 508 compliant,   WCAG 2.0 AA, Playwright visual regression testing
- **Status:** **Very active** with Figma multi-mode variable system for theme tokens. 
- **Docs:** design.cms.gov

### 9. Queensland Health Design System — Beta, extending to whole-of-government

Originally developed by Queensland Health  as part of its Digital Transformation Program, this system is now expanding to serve the entire Queensland Government.  

- **Framework:** Bootstrap 5.3 with custom CSS properties, Handlebars/Mustache templates, Storybook 
- **License:** MIT
- **GitHub:** github.com/qld-gov-au/qgds-bootstrap5 (~4 stars); also qgds-vanilla and qgds-web-components repos
- **npm:** `@qld-gov-au/qgds-bootstrap5` 
- **Components:** **~23+ components** including accordions, banners (4 variants), breadcrumbs, cards, forms, navigation, pagination, search, tables, alerts
- **Accessibility:** WCAG 2.1 Level AA 
- **Multi-brand support:** Master brand, sub-brand (department-specific), stand-alone (statutory bodies), campaign themes  via CSS custom properties
- **Status:** **Beta.** Dedicated team funded since January 2024.  Consulted with 3,700+ patients and professionals.  Designed by Folk (strategic design consultancy).
- **Docs:** designsystem.qld.gov.au and design-system.health.qld.gov.au

### 10. Better Design System — Commercial powerhouse for openEHR

Better (formerly Marand, headquartered in Ljubljana, Slovenia) has built a comprehensive design system for its openEHR-based clinical platform, transitioning from Angular to **Lit-based Web Components** for framework-agnostic deployment.

- **Framework:** Web Components (Lit) — next generation; formerly Angular Material. Works with React, Angular, Vue, or no framework.
- **License:** Mostly proprietary (commercial Better Platform/Studio ecosystem); some open-source components (Apache 2.0): better-ui-components,  web-template, ehr-common
- **GitHub:** github.com/better-care (17 repos) 
- **Components:** **50+ new web components** delivered in 2025 alone;  BDS 2.0.0 released  with WCAG 2.2 compliance
- **Key features:** Low-code form builder from openEHR templates, clinical data visualizations  (vital signs, lab results, medications, sparklines), design tokens, dark mode/high-contrast,  AI-assisted design-to-code workflows, Figma integration 
- **Notable users:** National EHR systems in Slovenia, Greece, Malta; NHS (One London, Plymouth); **60+ hospitals in Finland**; Karolinska University Hospital (Sweden);  100,000 Genomes Project 
- **Status:** **Very actively developed.** Named Leader in IDC MarketScape: EMEA Healthcare Data Platforms 2025. 
- **Docs:** better.care/design-system

### 11. BonFHIR — The most comprehensive FHIR-native React UI toolkit

BonFHIR is a collection of TypeScript libraries for building FHIR-based products, offering **renderless React components** that can be paired with any UI toolkit via custom renderers.

- **Framework:** React (web), React Native (via Gluestack UI renderer), Next.js (dedicated package with NextAuth)
- **License:** Apache 2.0
- **GitHub:** github.com/bonfhir/bonfhir — **65 stars**, 868 commits, **171 releases**
- **npm packages:** @bonfhir/core, @bonfhir/query, @bonfhir/react, @bonfhir/mantine, @bonfhir/gluestack-ui, @bonfhir/next, @bonfhir/subscriptions, @bonfhir/aws-lambda, @bonfhir/us-core, @bonfhir/cli, @bonfhir/codegen,  @bonfhir/n8n-nodes-bonfhir
- **FHIR versions:** **R4B and R5**  with complete TypeScript type definitions and search parameter builders
- **Key components:** FhirValue (localized FHIR data type display), FhirTable, FhirInput (form inputs), FhirQueryLoader, FhirPagination; hooks: useFhirSearch, useFhirRead, useFhirClientMutation
- **FHIR server compatibility:** Any FHIR-compliant server; default devbox uses Medplum
- **Status:** **Actively developed** (latest release September 2025). Team offers commercial FHIR consulting.
- **Docs:** bonfhir.dev, bonfhir.dev/storybook

-----

## FHIR UI libraries and form builders

The FHIR UI ecosystem is fragmented across multiple competing libraries. **Medplum** has the largest community, while **BonFHIR** offers the most comprehensive FHIR-native developer experience. For Questionnaire/form rendering, **Smart Forms (CSIRO)** is the SDC reference implementation.

### Medplum React Components — Full-platform FHIR UI

The most popular FHIR React component library, part of the Medplum open-source healthcare platform.  Built on **Mantine v7+**, it provides ResourceForm, QuestionnaireBuilder, PatientTimeline, and SmartText (SNOMED/ICD concept detection).  GitHub stars for the monorepo exceed **9,400**, with npm packages `@medplum/react` and `@medplum/react-hooks` at v5.1.x. Apache 2.0 licensed, very actively maintained. Storybook at storybook.medplum.com.

### fhir-react (1upHealth) — Simple drop-in resource renderer

A single `<FhirResource>` React component that auto-renders any FHIR resource across **DSTU2, STU3, and R4**.  Bootstrap-based accordion UI  with CARIN Blue Button profile support. MIT licensed, npm package `fhir-react` at v1.0.2.   The simplest option for read-only FHIR data display.

### Smart Forms (CSIRO) — SDC reference implementation

The **reference implementation for FHIR SDC Form Filler** from Australia’s CSIRO. React-based (Material UI theming), supporting $populate, $assemble, $extract operations, complex enableWhen logic, terminology bindings, and calculations. npm: `@aehrc/smart-forms-renderer` (v1.0.0 released).  Apache 2.0. Very actively maintained. Docs at smartforms.csiro.au.

### LHC-Forms (NLM/LHNCBC) — The longest-standing FHIR form widget

Developed by the National Library of Medicine’s Lister Hill Center, this Web Component renders forms from FHIR Questionnaire definitions with skip logic, calculated values via FHIRPath, pre-population, coded answer autocomplete, and multi-language support. Supports **STU3, R4, and R5**. Companion NLM Form Builder provides GUI-based Questionnaire editing. npm: `lforms` (v36.3.x+). Actively maintained.

### Formbox Renderer (Health Samurai) — Headless questionnaire renderer

Formerly Aidbox Forms, this headless React renderer uses pluggable themes (@formbox/mantine-theme or custom). Covers **80% of FHIR SDC IG**, with pre-population, extraction, calculations, multilingual forms, and FHIRPath editor with autocomplete. Works with Aidbox and other FHIR servers. Actively developed.

### Google Open Health Stack — Android FHIR SDK with Material Design

Google’s Structured Data Capture Library renders **FHIR Questionnaires as native Android Material Design UI**, with skip logic, pagination, validation, FHIRPath expressions,  offline capability,   and WHO SMART Guidelines support.   Package: `com.google.android.fhir:data-capture`. Apache 2.0. **Digital Public Good certified**,  used across Sub-Saharan Africa, India, and Southeast Asia.  Very actively developed with comprehensive design guidelines. 

### Additional FHIR UI tools

|Library                           |Framework          |FHIR Versions   |Status                        |
|----------------------------------|-------------------|----------------|------------------------------|
|@beda.software/fhir-react         |React (data layer) |R4B             |Active                        |
|fhir-ui (HealthIntellect)         |React + Material UI|R4              |Inactive (3yr old)            |
|material-fhir-ui (Clinical Meteor)|React + Material UI|STU3/R4         |Deprecated (5yr old)          |
|@artezio/surveybuilder            |React + Bootstrap  |R4              |Limited activity              |
|@i4mi/fhir-questionnaire-renderer |Vue (Quasar)       |R4              |Active but partial            |
|fhirclient (SMART Health IT)      |Framework-agnostic |DSTU2/STU3/R4   |Active (~15K weekly downloads)|
|fhir-kit-client (Vermonster)      |Node.js            |Version-agnostic|Maintained                    |
|SAP OpenUI5-FHIR                  |OpenUI5/SAPUI5     |R4              |Low-moderate                  |

-----

## Open-source EHR design systems and frameworks

### OpenMRS 3.0 (O3) — The most mature open-source EHR frontend

OpenMRS 3.0 is the global open-source EHR project’s modern frontend, built on **React + TypeScript + IBM Carbon Design System**   with a **micro-frontend architecture** (single-spa). It represents the most complete, actively developed open-source healthcare design system available.

npm packages include `@openmrs/esm-framework`, `@openmrs/esm-styleguide`,  and many `@openmrs/esm-*` domain packages.  The system provides Carbon Design tokens,  an extension/slot system for pluggable UIs, **13 calendar system** support,  offline-first capabilities, and Playwright E2E testing. Latest stable v3.4.0 with Rspack migration delivering 5–10x faster builds.  MPL 2.0 licensed. Deployed globally across hundreds of health facilities.

### Bahmni (ThoughtWorks) — Carbon-based EHR UI for global health

Bahmni’s `bahmni-carbon-ui` extends IBM Carbon Design System components for healthcare workflows,  including India’s ABDM (Ayushman Bharat Digital Mission) UI extensions.  AGPL-3.0 licensed,  used in **50+ countries**.  Active UX redesign underway with split-screen consultation dashboards. 

### HospitalRun — Stalled but notable React component library

The `@hospitalrun/components` npm package  (v3.4.0) provides React + TypeScript + Bootstrap components built for developing-world hospitals  with offline-first design (PouchDB/CouchDB).  **132 GitHub stars**, MIT licensed,   but development has been **stalled/dormant since ~2022**.

### Other open-source EHR UIs

**OpenEMR** (GPL-2.0, github.com/openemr) is the most popular open-source EHR globally but lacks a formal component library — a UI/UX separation project is underway. **GNU Health** (GPL-3.0,  hosted on Codeberg) uses the Tryton ERP framework  providing GTK desktop forms, with a FHIR server since v2.8.  **LibreHealth** (MPL-2.0) is an OpenEMR fork   with a slow-moving Laravel rewrite. **VistA/CPRS** (public domain, US VA) remains in use at VA hospitals  with its 1990s-era Delphi UI,  while the eHMP project provided a Backbone.js-based web alternative. 

-----

## Medical imaging UI libraries

Medical imaging has the richest ecosystem of specialized healthcare UI libraries, anchored by the OHIF/Cornerstone stack.

### Cornerstone3D — GPU-accelerated DICOM rendering engine

The foundation of modern web-based medical imaging, maintained by the **Open Health Imaging Foundation** with NCI grant funding.  The cornerstone3D monorepo (~**1,000 stars**) provides  GPU-accelerated rendering, all DICOM transfer syntaxes, DICOMweb support,  MPR, volume rendering, segmentation, and annotation tools via web workers. npm packages: `@cornerstonejs/core`, `@cornerstonejs/tools`, `@cornerstonejs/dicom-image-loader`. MIT licensed, framework-agnostic with React/Vue/Angular/Next.js integration repos.  **Very actively maintained.**

### OHIF Viewer — The standard open-source DICOM viewer

Built on Cornerstone3D, the OHIF Viewer  (~**3,100 stars**) is a React-based zero-footprint DICOM viewer supporting 2D/3D/MPR, PET/CT, microscopy, segmentation, DICOM SR, RT structs, and lesion tracking. Its extension/mode architecture enables customization, and **FDA-Cleared derivative viewers** exist. MIT licensed with NCI sustainment grant through 2028.  Docs at docs.ohif.org.

### The broader imaging ecosystem

|Library                     |Stars |Framework    |Key Feature                             |License   |Status     |
|----------------------------|------|-------------|----------------------------------------|----------|-----------|
|DWV                         |~1,400|Pure JS/HTML5|Zero-footprint, filters, ROI tools      |GPL-3.0   |Active     |
|VTK.js (Kitware)            |~1,200|ES6 JS       |Full VTK rewrite; WebGL + WebGPU + WebXR|BSD-3     |Very Active|
|dicom-parser                |~744  |Pure JS      |Lightweight DICOM Part 10 parsing       |MIT       |Stable     |
|AMI.js (Harvard/FNNDSC)     |~800  |JS + Three.js|WebGL 3D medical visualization          |Apache-2.0|Mature     |
|Papaya (UT Health SA)       |~572  |Pure JS      |Zero-dependency neuroimaging viewer     |MIT       |Mature     |
|NiiVue (Oxford/USC)         |~250  |WebGL2 JS    |30+ volume/mesh formats, neuro focus    |BSD-2     |Very Active|
|ITK-Wasm (Kitware)          |~219  |C++→Wasm+TS  |N-dimensional image processing          |Apache-2.0|Very Active|
|BioImage Suite Web (Yale)   |~200  |JS+Wasm      |fMRI connectivity, segmentation         |Apache-2.0|Active     |
|Stone of Orthanc (UCLouvain)|N/A   |C++→Wasm     |MPR, PET-CT fusion, teleradiology       |AGPL      |Active     |

-----

## Digital health company design systems

Most digital health companies maintain **proprietary, internal design systems** that are not publicly available. The notable exceptions and documented systems include:

**Nordhealth Nord** is the only fully documented healthcare company design system with public documentation.  Built with **Lit-based Web Components** (40+ components), it serves Nordhealth products  like Provet Cloud. However, its **proprietary license restricts use to Nordhealth products only**.  npm packages: @nordhealth/components, @nordhealth/css, @nordhealth/themes, @nordhealth/tokens, @nordhealth/icons (v4.9.0).  Docs at nordhealth.design.

**Doctolib’s Oxygen** Design System  has a publicly accessible Storybook (doctolib.github.io/storybook/) and processes **70,000+ component insertions per week** by 50+ designers.  React-based, primarily internal.

**Babylon Health’s DNA** was an extensively documented design system  with Web Components, iOS (MedKit), and Android libraries, led by Amy Hupe (formerly of GDS). **Now defunct** after Babylon’s August 2023 bankruptcy. Some GitHub repos remain archived at github.com/babylonhealth. 

**Oscar Health’s Anatomy** is a comprehensive React/React Native design system  with WCAG AA compliance, important for their Medicare Advantage market. Fully internal. 

**Boston Scientific’s Anatomy** (confusingly same name as Oscar’s) is the standout medical device company design system  — available on GitHub at github.com/bos-sci with `@boston-scientific/anatomy-react` (v2.4.2), design tokens, icons, and Figma kit. Active, with multiple themes including clinical variants.

Other documented but proprietary systems include **Sanofi Elements** (built with Rangle.io),  **J&J’s UXPin-based system**,  **Optum/UHG’s Netra**,  and **Elevance Health’s AEM-based system**.  No pharmaceutical company publishes an open-source UI component library.

-----

## Government and national health IT design systems

Beyond the three requested government systems (NHS, CMS, Queensland), several additional government healthcare design systems exist:

**Australian Health Design System** (github.com/healthgovau/health-design-system) extends the Gold/DTA Design System with SASS-based components. MIT licensed, npm: `@health.gov.au/health-design-system`. 

**Our Future Health Design System** (UK health research program) is based on the NHS.UK Service Manual, using Nunjucks templates with an Eleventy-powered docs site. MIT licensed, at designsystem.ourfuturehealth.org.uk (alpha stage). 

**Sweden’s Inera 1177 UX Framework** provides internal UX guidelines for the national 1177 Vårdguiden healthcare portal, including a form management system and design tool (“Designverktyget”). Not publicly available as a downloadable component library.

**Germany’s gematik** publishes specifications for the Telematikinfrastruktur including FHIR-based MIOs (Medical Information Objects)  and TI-Messenger  (Matrix protocol), but these are infrastructure standards rather than UI component libraries.

Most national health portals — including Denmark’s Sundhed.dk, Norway’s Helsenorge, Finland’s Kanta, Estonia’s Digilugu, Singapore’s HealthHub, India’s ABDM, and Saudi Arabia’s NPHIES — operate as **infrastructure and data exchange platforms** without publicly documented reusable design systems. India’s ABDM is notable for scale (**690M+ health accounts**) and a revamped ABHA app with new UI in 2024, but no public component library exists.

-----

## openEHR UI tools and form renderers

Beyond Medblocks UI and Better’s commercial offerings, several openEHR UI tools exist for form generation:

**CaboLabs openEHR-CLI** (github.com/CaboLabs/openEHR-CLI) provides a `uigen` command that generates Bootstrap-based HTML/JavaScript forms from Operational Templates.   Apache 2.0.

**openEHR Archetype Designer** (tools.openehr.org/designer) is a web-based visual archetype/template editor  originally built by Marand (now Better) in Angular. Free to use, primary tool for openEHR clinical modeling.

**EHRbase** (github.com/ehrbase, ~**500 stars**, Apache 2.0) provides an openEHR Clinical Data Repository with a web sandbox UI for template management and composition editing, plus an AQL Builder adapted from Better’s open-source tool.

**Ocean Template/Archetype Designers** are legacy Windows desktop applications for openEHR template creation, being superseded by web-based tools. 

-----

## Clinical informatics specialized UI tools

### CDS Hooks Sandbox

The HL7 **CDS Hooks Sandbox** (github.com/cds-hooks/sandbox) is a React + Redux mock-EHR simulator that renders CDS cards (info/warning/critical indicators, suggestion cards, app link cards).  Apache 2.0. Live at sandbox.cds-hooks.org.

### HL7v2 message viewers

Web-based HL7v2 parsing tools include the **Backbeach Software HL7v2 Viewer** (github.com/brynlewis/HL7-v2-Parser-and-Viewer), **Redox HL7v2 Parser** (github.com/RedoxEngine/redox-hl7-v2), and **Antvaset Online Tools** (antvaset.com) with parser, editor, validator, and FHIR converter.

### C-CDA document renderers

The **Backbeach C-CDA Viewer** (github.com/brynlewis/C-CDA_Viewer, Apache 2.0) won the HL7/ONC C-CDA Rendering Tool Challenge with responsive rendering, section reordering, drag-and-drop, and duplicate detection — extending the standard HL7 CDA XSL stylesheet.

### Clinical terminology UIs

**SNOMED CT Browser** (github.com/IHTSDO/sct-browser-frontend, Apache 2.0) powers browser.ihtsdotools.org and the NHS Digital term browser with multi-lingual search and hierarchy navigation. **SNOMED UI Examples** (github.com/IHTSDO/snomed-ui-examples) provides Angular-based search demo components.

**Health Icons** (github.com/resolvetosavelives/healthicons) offers **1,000+ free CC0 public domain** health icons for clinical concepts, conditions, and devices — designed for low-resource settings.

-----

## Telehealth and video consultation UI

The telehealth video component market is in flux following **Twilio’s December 2024 announcement** that its Video WebRTC service will shut down by end of 2025.

**Daily.co** has emerged as the industry leader for telehealth video, offering HIPAA-compliant (BAA available) peer-to-peer encrypted video with **AI-powered clinical notes generation**, mobile-native SDKs, and low-bandwidth optimization. Founded by engineers who wrote the WebRTC specification. Actively acquiring Twilio Video customers with $30K migration credits.

**Vonage/TokBox** (Ericsson) remains active with comprehensive WebRTC SDKs (github.com/opentok) for web, iOS, Android, Windows, macOS, and React Native. HIPAA-compliant with v2.32.1 SDKs, SIP integration, and AI agent framework support.

-----

## Clinical research and trial UI platforms

**REDCap** (Vanderbilt University) is the dominant clinical research data capture platform — used by **5,900+ institutions in 145 countries** with 2.1M+ end users and 19,000+ journal citations. Free for consortium partners but **not open-source**. Features a web-based form builder, FHIR integration via CDIS, and mobile app with offline collection. HIPAA/GDPR/21 CFR Part 11 compliant.

**OHDSI ATLAS** (github.com/OHDSI/Atlas, Apache 2.0) provides self-service cohort identification, population characterization, and prediction across the **800M+ patient** OHDSI network using the OMOP Common Data Model. Built with Knockout.js.

**OpenClinica** (github.com/OpenClinica/OpenClinica) offers open-source clinical data management with eCRF design, CDISC ODM support, and 21 CFR Part 11 compliance. Community and Enterprise editions available.

**i2b2** (i2b2.org) provides a Java-based clinical data research warehouse with drag-and-drop cohort discovery, deployed across academic medical centers including Mayo Clinic.

-----

## Additional notable healthcare UI projects

**Opal** (github.com/openhealthcare/opal, MIT/BSD) is a Python/Django + Angular clinical application framework with patient lists, clinical pathways, and modular plugins. Used in NHS settings.

**Fasten Health** (github.com/fastenhealth) is an Angular/Go self-hosted personal health record aggregator with its own UI.

**Infermedica Component Library** (github.com/infermedica/component-library) provides mobile-first, accessibility-friendly **Vue 3** components for AI-powered symptom checker interfaces.

**Elsa Health Design System** (github.com/Elsa-Health/design-system) offers React Native components for mobile health apps in African contexts, with English/Swahili support. Apache 2.0.

**Open mHealth Web Visualizations** (github.com/openmhealth/web-visualizations, Apache 2.0) provides D3-based charts for mobile health data including blood pressure, heart rate, body weight, and step count.

**Flux Notes** (MITRE/Standard Health Record) is a React-based prototype for innovative clinical note-taking with structured data capture within narratives. Apache 2.0.

-----

## What the landscape reveals

Three structural patterns define the healthcare UI ecosystem. First, **the open-source tier is surprisingly robust** — projects like OpenMRS 3.0, OHIF Viewer, Medplum, Smart Forms, and BonFHIR rival commercial alternatives in quality and are actively maintained with institutional backing (IBM, NCI, CSIRO, NLM). Second, **no major proprietary EHR vendor** (Epic, Oracle Health, athenahealth, eClinicalWorks, Meditech, NextGen) provides a public UI component library — they offer APIs and sandboxes but expect developers to build their own interfaces. Third, **the FHIR form/questionnaire space is maturing rapidly**, with Smart Forms reaching v1.0 as the SDC reference implementation and Formbox offering a headless alternative.

The most significant gap remains the absence of a comprehensive, open-source, general-purpose healthcare design system equivalent to Material UI or Ant Design. Terra UI came closest but died with Oracle’s acquisition. The NHS Design System is excellent but UK-health-specific. **OpenMRS 3.0’s Carbon-based system** is currently the most complete open-source option, though its EHR-specific architecture limits reusability for other healthcare applications. Teams building healthcare software today typically compose solutions from general-purpose design systems (Carbon, Mantine, Material UI) combined with specialized healthcare libraries (BonFHIR for FHIR, Cornerstone for imaging, Medblocks for openEHR) rather than finding a single integrated healthcare UI framework.
