# Tekla Automation Toolkit

Tekla Structures macros, plugins and setup tools that remove repetitive measuring, marking, modelling, reporting and model maintenance work. The `.tsep` installers package each tool for supported Tekla versions, where noted, and the catalog separates measured results from estimates and lists known limits.

**Live site:** https://mosakr970.github.io/tekla-automation-toolkit/

## The tools

| Tool | Runs in | What it does | Verified or measured result | Details |
|---|---|---|---|---|
| HC Check | Model | Flags hollow-core panels the factory cannot saw | 897 panels in 38–52 s; 0 disagreements on 851 panels against a second check | [hc check](https://mosakr970.github.io/tekla-automation-toolkit/hc_check.html) |
| Insert Tendons | Model | Models post-tensioning tendons and ducts from the designer's Excel profile | 118 beams and 848 parts in 13–17 s | [insert tendons](https://mosakr970.github.io/tekla-automation-toolkit/insert_tendons.html) |
| EK Mark | Model | Gives identical pieces the same `EK_MARK` and every different piece the next number | 3,421 pieces compared in 3.6–5 min; 1,356 / 1,357 identical pairs matched | [ek mark](https://mosakr970.github.io/tekla-automation-toolkit/ek_mark.html) |
| Drawing Creator | Model | Creates a GA drawing per selected model view | 6.5–17 s per drawing across 36 views | [drawing creator](https://mosakr970.github.io/tekla-automation-toolkit/drawing_creator.html) |
| Report Creator | Model | Writes EK-8xx summaries to Excel templates | 3,421 assemblies scanned in 7–9 s; assembly reports in 0.1–2 s | [report creator](https://mosakr970.github.io/tekla-automation-toolkit/report_creator.html) |
| Opening Marks | Drawing | Finds every opening in a floor plan and crosses it out | 1 plan in 24 s; 37 openings and 1,572 parts previously checked | [opening marks](https://mosakr970.github.io/tekla-automation-toolkit/opening_marks.html) |
| Auto Dimension | Drawing | Dimensions a plan to the grid and chains elements in a row | 1st floor plan: 20 s versus 15 min by hand | [auto dimension](https://mosakr970.github.io/tekla-automation-toolkit/auto_dimension.html) |
| Drawing Check | Drawing | Checks an open drawing against the Esplan checklist | 281 / 287 dimension texts placed as printed in the test | [macro guide](https://mosakr970.github.io/tekla-automation-toolkit/macro_catalog.html#drawing-check) |
| Coordinate Mark | Drawing plugin | Writes point coordinates from the view's location base point | No live check or timed run recorded yet | [coordinate mark](https://mosakr970.github.io/tekla-automation-toolkit/coordinate_mark.html) |
| Auto Maintenance | Model plugin | Saves, syncs, diagnoses, repairs, backs up and archives a model | No timed run recorded yet | [auto maintenance](https://mosakr970.github.io/tekla-automation-toolkit/auto_maintenance.html) |
| Tekla Setup | Windows app | Sets up a newly installed Tekla version from the office server | Date-format and paper-size steps verified on Tekla Structures 2026.0 | [tekla setup](https://mosakr970.github.io/tekla-automation-toolkit/tekla_setup.html) |

For all tools side by side, with setup requirements and known limits, see the [Macro Catalog](https://mosakr970.github.io/tekla-automation-toolkit/macro_catalog.html).

## Status and limits

- **Auto Dimension:** reviewed and measured on live plans; no result is implied beyond the published 20-second macro run and 15-minute hand comparison.
- **Coordinate Mark:** the plugin is packaged and compiled, but no live coordinate check or timed run is recorded yet.
- **Drawing Check:** the catalogue documents it, but it has no `.tsep` installer or standalone case-study page yet.
- **Auto Maintenance:** no timed run is recorded yet.
- **Tekla Setup:** a full copy/install run has not been completed through the tool yet.
- Each standalone case study lists its own limits.

## Install, in short

1. Double-click `Install-All.bat` or install the relevant `.tsep` into the supported Tekla versions. The catalog lists the exact package for each tool.
2. Restart Tekla. Tekla registers macros and extensions only at startup.
3. Open **Applications & components** and run model tools with a model open or drawing tools with a drawing open.

Tested with Tekla Structures 2023.0 and 2025.0.

## Author

Mohamed Sakr, Structural Engineer, BIM & Digital Delivery, Tallinn, Estonia.
[LinkedIn](https://www.linkedin.com/in/mosakr970) · [GitHub](https://github.com/mosakr970) · mo.sakr970@gmail.com
