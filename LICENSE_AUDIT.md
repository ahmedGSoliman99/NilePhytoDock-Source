# Redistribution audit — NilePhytoDock Studio v1.0.0

Developers: Ahmed G Soliman and Malak Taha. This audit records packaging and source-access decisions for the first official release; it does not relabel earlier development builds or validation evidence.

## Application and repository history

The existing application's LICENSE grants GPL-3.0-or-later rights. Publishing binaries therefore requires access to the corresponding application source, including the build and installation scripts and essential build inputs. Making a working repository private cannot withdraw rights granted by previously published copies. Deleting files from a branch cannot remove their historical publication.

The public product repository is a new repository with a clean initial history: logo, English product description, actual screenshots, requirements, download link and required legal notices. It does not inherit development history. Corresponding source for v1.0.0 and the earlier distributed 0.6.0/0.6.1 builds is separately accessible without authentication through the public NilePhytoDock-Source release archives. Full development history is preserved in the original working repository; its visibility changes only after source access is in place.

No promise of closed-source ownership or revocation of GPL rights is made. Application GPL rights, upstream copyright notices and cited-publication rights remain in force. Personal working databases, research project outputs, debugging logs and credentials are not release build inputs and are excluded from the new source archives and product repository.

## Component review

| Component | Relevant obligation and delivery |
| --- | --- |
| NilePhytoDock | GPL-3.0-or-later; application source, package configuration, installer source, packaging scripts, original essential library data/resources and rebuild instructions are available separately. |
| Smina / OpenBabel | Smina's Apache/GPL components and GPL OpenBabel require retained notices and source. The inherited Smina executable reports 2020.12.10 conda-forge:b08c07c. Source tag 2020.12.10 and the dated conda recipe/patches are supplied, together with OpenBabel 3.1.1 and the Python wheel build source. Original native hashes and provenance are retained. No native code was modified. |
| P2Rank | The application is MIT, but this does not relicense its Java libraries. Weka/FasterForest GPL source, BioJava/CDK/XOM LGPL source, modified BioJava source and dependency source JARs are retained/listed. The bundled FastRandomForest source JAR is preserved. Original JAR license/notice entries are copied into the installed notices. |
| Java | Temurin 17.0.19+10 GPL-2.0 plus Classpath Exception. The jlink runtime retains legal notices. The complete matching OpenJDK source archive is available with its published SHA-256. |
| Qt / PySide6 | LGPL/GPL options and mandatory third-party notices are retained. The runtime uses separate DLLs; researchers can replace interface-compatible libraries. Reverse engineering to debug modified LGPL components is permitted. Sources and packaging instructions permit rebuilding with modified libraries. No installer restriction or signature lock prevents this. |
| Qt WebEngine / PDF | Bindings 6.12.0.140 contain native engine 6.140.0 / Chromium 140.0.7339.225. The matching upstream 6.140.0 release-candidate source and pinned Chromium source tree/download are identified separately from Qt 6.12.0. Chromium's full source is provided through the explicitly linked public upstream server; the VERSION file was checked against the installed engine. The wheel does not embed a native Git commit; byte-identical reconstruction of that upstream wheel is not asserted. |
| MDAnalysis / GridDataFormats / Meeko | LGPL license texts and matching source distributions are supplied. Application source and instructions allow replacement and repackaging. |
| RDKit and other Python libraries | Each distribution retains its license. The RDKit library BSD notice is retained alongside its wheel-wrapper MIT notice. Python/NumPy/SciPy/pandas numerical-runtime notices and the other collected Python distribution licenses remain included. |
| Plotly / 3Dmol | Local visualization assets retain their MIT/BSD license notices. They do not require online assets at runtime. |
| Windows runtime | Microsoft system/runtime components retain Microsoft terms and are not relicensed as application GPL code. Windows supplies .NET Framework used by Setup; no Python or Java install is delegated to the user. |

THIRD_PARTY_SOURCES.json contains archive checksums, exact package versions and upstream source links. Source JARs are kept separate from the researcher download. Native binaries are version/provenance identified and tested; a byte-for-byte native rebuild or a fresh scientific validation of upstream algorithms is not claimed.

## Packaging decisions

Python/Qt/scientific dependencies, Java, Smina, the default P2Rank prediction model, visualization assets and essential library data remain bundled. Unused P2Rank alternate models, Qt QML assets, non-English translations, source/test/development files and non-Windows native JARs are omitted. P2Rank headless prediction does not use OpenChart's legacy GUI plotting JAR; that JAR and the duplicate vecmath 1.3.1 JAR are omitted while vecmath 1.5.2 remains. Smina retains its actual PE dependency closure and non-Cairo molecular plugins; unrelated Cairo drawing dependencies are omitted. Native prediction/docking outputs must pass integration checks after these packaging changes.

A one-file PyInstaller build was actually launched and tested. It repeatedly extracts dependencies before startup. A one-file Windows Setup was selected because it installs the same native runtime once and launches the installed application faster. Dependencies are hidden for a clean installed folder, not encrypted or concealed from license recipients. Full notices are installed under Documentation and _internal/external_tools/licenses.

Nuitka 4.3.1 was investigated and a one-file compiler probe attempted. It required additional Windows dependency-analysis/compiler tooling absent from this host; no successful Nuitka binary or timing is claimed. The final release uses the existing verified PyInstaller dependency graph and a source-provided .NET installer.

## References

[GNU GPL FAQ: source and binary on different servers](https://www.gnu.org/licenses/gpl-faq.en.html#SourceAndBinaryOnDifferentSites), [Qt for Python licenses](https://doc.qt.io/qtforpython-6/licenses.html), [PyInstaller one-file behavior](https://pyinstaller.org/en/stable/operating-mode.html), [Nuitka compiler requirements](https://nuitka.net/user-documentation/user-manual.html).

## v1.0.1 maintenance update

The maintenance update changes coordinate retrieval and scientific presentation. Dependency versions, native binaries, redistribution terms and the source-replacement policy are unchanged. Its corresponding application source and build inputs are provided in a separate v1.0.1 source release; the v1.0.0 dependency archives and earlier sources remain available. No user projects or working database are included.

The supplied Python ssl module has a distribution-specific public CA distrust hook. v1.0.1 includes the missing 906-byte public policy file at the frozen runtime root, without changing its contents or disabling certificate verification. The precise module and policy are provided in build/runtime in the corresponding source; Python's full PSF license is retained. Frozen OpenSSL reports 3.6.4, unchanged from the existing collected native libraries. Source/runtime versions and the runtime-specific TLS source are distinguished in THIRD_PARTY_SOURCES.json.
