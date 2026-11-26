# NilePhytoDock Studio v1.0.3 validation

26–27 November 2026. This maintenance release changes live reads, functional/shared-group analysis scheduling, progress reporting, layout, incremental saving and installation cleanup. It retains historical scientific validation and documents the limited template-restoration correction separately.

## Automated suite

96 tests passed in 99.40 seconds, including the original scientific/geometry tests, independent live reads, shared/functional analysis and charts during an active scientific task, all workspace command rows at 900×600 and 1280×720 logical sizes, wrapping at 360/520/900 pixels, background selected-pose reanalysis, in-place cache reuse without overwriting, strict template restoration, native-output lock retry, owned-process cancellation and installer cleanup preservation. One existing MDAnalysis deprecation warning remains. Qt offscreen GPU diagnostics did not fail the tests; native rendering is checked separately. Evidence: data/validation/v1_0_3_release_full_tests.xml.

## Live result regression

A controlled GUI regression holds the scientific worker open while a separate writer commits two explicitly synthetic result records. Both the detailed table and oil summary must reflect each commit before the scientific worker is released. The fixture also confirms that a read failure does not cancel screening. Synthetic fixture scores are test inputs, not docking evidence.

## Native visual regression

The current source passed real PDB retrieval from a pasted structure URL, direct 2D save, native 3D atom mapping, three distinct camera exports, high-resolution label scaling and a computed pocket surface. All four chart types exported PNG/SVG/PDF/CSV/XLSX/JSON. All five molecular-analysis views were exercised, including shared Ketone structures from three distinct curcuminoids and molecular-analysis dataset exports. Evidence: data/validation/v1_0_3_final_visual/visual-verification.json. The final installed package also passed the combined native checks below.

## Read performance

On a private copy of the stopped 393-pose study, the pose/contact-count query took 15.929 seconds without indexes and 0.00425 seconds with indexes. The pose IDs and contact counts were identical after sorting; query order without ORDER BY is unspecified. This is one query on one host, not an overall application speed factor. Original research records were not used as release inputs or published.

## Functional/shared-group analysis and restoration

A separate private-copy check analyzed 160 distinct structures from completed runs in 26.235 seconds. It returned nine shared conventional functional-group categories, 31 group/residue association rows, four groups in the top-ten summary and zero contact-validation errors. Interactive analysis now validates only selected completed best poses, publishes progress, saves durable result JSON and queues SQLite history without blocking the display behind screening. These counts test software behavior; they are not a biological efficacy claim and the private research dataset is excluded from release artifacts.

All five previously invalid native caffeine poses were reconstructed against the validated achiral template in a local check. Sanitization and chemical identity passed, and every heavy-atom coordinate was retained without alignment. Unit negative fixtures reject changed connectivity and charge; a valid stereospecified fixture preserves its configuration. The fallback does not repair invalid outputs with specified stereochemistry.

## In-place cache recovery

A separate actual 3PTB/curcuminoid integration marked one saved run failed while retaining its hash-verified cache in its original destination folder. Resume processed three jobs with zero failures: one verified cache reuse, two retained completed runs and zero new docking calculations. All original pose-file hashes were unchanged. This catches the Windows same-file copy failure observed during real study recovery. Evidence: data/validation/v1_0_3_inplace_cache/verification.json.

## Installer cleanup

The real C# cleanup methods were exercised against owned installation fixtures, an unlisted research file, an unowned folder and a malicious parent-directory path. Owned executable/runtime files were removed; the unlisted research file and unowned folder survived; the outside path was rejected and its file preserved. The same regression is included in the test suite. Old application files are removed only after successful installation.

## Frozen source

All 59 included application modules match the final source code, including the independent read queue, progress strip, index migration, pose-stage progress and current-scene load gating. The scientific seed catalog and original source observations are retained. The installed-executable verification and final package hashes are recorded below after the actual installer test.

## Scope

The executable is unsigned. Tests use this Windows host, not a newly provisioned Windows VM. Existing upstream MDAnalysis deprecation and optional packaging warnings remain distinct from functional failures. Historical failed QA attempts remain local and are not represented as passed checks.

## Installed executable

The final Setup installed v1.0.3 with PATH restricted to Windows system directories and developer Python/Java/Qt settings removed. Three actual P2Rank/Smina jobs completed, and saved results appeared while the scientific worker was still active. The packaged checks passed PDB retrieval, direct 2D/300-DPI saving, atom/feature mapping, three camera exports, high-resolution labels, computed pocket surfaces, four chart types with six exports each, all five molecular-analysis views, shared-group structures, analysis exports and all project-report formats.

The one-close probe left zero owned engines and zero tasks; close latency was 0.031 seconds. Installation took 45.219 seconds on this host as an update, and native/visual/lifecycle verification took 121.297 seconds. This is not a fresh-install benchmark.

- Setup: `NilePhytoDock-v1.0.3-Setup.exe`, 428,914,176 bytes.
- Setup SHA-256: `3b4972f2ab20cc7361e722abf9d64009e9596bb4410bc89d0255f0948d99aa69`.
- Installed executable SHA-256: `96ff9eb16bbd994aff76ddb851b5be38f8f60d91630f956a087f8f0f7944989b`.
- Original scientific seed SHA-256: `da0b0f27f59c4790d06b54ab8de56bed056a524f5514277b340620aec11da90e`.
- Payload: 4,341 files, no researcher projects/databases, logs or SQLite sidecar caches.

Evidence: data/validation/v1_0_3_packaged_verification.json, v1_0_3_shipping_source_match.json and v1_0_3_payload_audit.json. Failed earlier release-QA attempts remain local; they are not represented as passed checks. These are software checks, without a new claim of experimental or broad docking accuracy.
