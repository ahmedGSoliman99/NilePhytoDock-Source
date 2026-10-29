# Third-party notices

NilePhytoDock is developed by Ahmed G Soliman and Malak Taha. The application source is supplied under GPL-3.0-or-later; see LICENSE and external_tools/licenses/GPL-3.0.txt. The Word documents and their cited scientific data remain subject to their respective authors' rights; no ownership of those source publications is claimed.

Third-party components retain their own licenses. This notice is not a replacement for the included full texts or license obligations. Redistributors must provide corresponding source and notices where required and preserve the ability to replace LGPL Qt libraries. No proprietary PyMOL component is distributed.

| Component | License / provenance |
| --- | --- |
| Smina 2020.12.10 | Apache-2.0/GPL-2.0 components; dynamically uses GPL OpenBabel. Native binary/runtime from fhh2626/BFEE-Docking commit 6bb8d06df67e8ca3077622bbb208fac51be0bb30, with file hashes in external_tools/smina/provenance.json. Corresponding upstream source tag 2020.12.10 from jaimergp/smina is archived in external_tools/source_archives. A fresh rebuild was not performed. |
| OpenBabel 3.1.1 | GPL-2.0-or-later; source https://github.com/openbabel/openbabel/tree/openbabel-3-1-1 |
| P2Rank 2.5.1 | MIT; included LICENSE.txt; source https://github.com/rdk/p2rank/releases/tag/2.5.1. Its Java libraries retain their separate upstream licenses. |
| Temurin Java 17.0.19 | GPL-2.0 with Classpath Exception; jlink image retains legal notices. Source https://github.com/adoptium/temurin17-binaries/releases/tag/jdk-17.0.19%2B10 |
| Qt / PySide6 | LGPL-3.0/GPL/commercial alternatives; LGPL option used with dynamically bundled libraries; source https://code.qt.io/ and installed package metadata/notices. |
| RDKit | BSD-3-Clause; source https://github.com/rdkit/rdkit |
| ProLIF | MIT; source https://github.com/chemosim-lab/ProLIF |
| MDAnalysis | LGPL-3.0-or-later; source https://github.com/MDAnalysis/mdanalysis |
| Meeko | LGPL-2.1-or-later; source https://github.com/forlilab/Meeko |
| 3Dmol.js | BSD-3-Clause; bundled local build SHA-256 4ab374e1830bcceC950b280fd285a430e05e91bd13c9ef0097c611c66de6cb36; source https://github.com/3dmol/3Dmol.js |
| Plotly.js 3.3.0 | MIT; offline bundle SHA-256 6ceddd4bac82a64f5a2b8814a4d10bb4288379262f1989caee3148e7c3509c72; full license external_tools/licenses/plotly-js-LICENSE.txt; source https://github.com/plotly/plotly.js/tree/v3.3.0 |
| BioPython | Biopython License / BSD-3-Clause |
| NumPy / SciPy / pandas | BSD-style licenses and bundled numerical runtime notices |
| matplotlib | PSF-based license with included third-party notices |
| python-docx / openpyxl | MIT |
| ReportLab | BSD-style license |
| Python | PSF License |
| PyInstaller | GPL-2.0-or-later with bootloader exception |

Exact Python packages are listed in requirements.txt. Installed distribution license files are collected into external_tools/licenses/python_packages. The native Smina directory contains Windows/Boost/OpenBabel support DLLs; their original projects' terms apply. The RDKit library uses BSD-3-Clause; its Python wheel wrapper's separate MIT license is also retained. See the included RDKit-BSD-3-Clause.txt.

P2Rank's MIT license does not cover all its Java dependencies. These include Weka and FasterForest (GPL), BioJava/CDK/XOM (LGPL), and other separately licensed libraries. Their embedded notices are retained under external_tools/licenses/p2rank_dependencies, supplemented by upstream source notices. Exact dependency source JARs and the modified BioJava/FasterForest sources are listed in THIRD_PARTY_SOURCES.json.

The PySide6 WebEngine/PDF bindings are version 6.12.0.140; the actual embedded Qt WebEngine/PDF engine reports 6.140.0 with Chromium 140.0.7339.225. These version numbers are intentionally distinguished. Qt sources, LGPL license texts, GPL license texts and Chromium source access are preserved. The installer exposes replaceable libraries and does not restrict LGPL debugging or modification rights.

Public corresponding source and packaging instructions: https://github.com/ahmedGSoliman99/NilePhytoDock-Source . See SOURCE_ACCESS.md and LICENSE_AUDIT.md. Native binaries are inherited from their identified upstream distributions; a byte-for-byte native rebuild is not claimed. The full working development history is preserved separately, and previously granted GPL rights remain in force.

GridDataFormats 1.2.0 is LGPL-3.0-or-later; its complete COPYING and COPYING.LESSER texts and matching source distribution are retained.
