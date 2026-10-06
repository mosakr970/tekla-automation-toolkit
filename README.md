# Tekla Automation Toolkit

Five single-file Tekla Structures macros that take the repetitive measuring, marking and modelling out of precast work. Each is one `.cs` file: no installer, no Python, no server. Each has a case study that separates measured results from estimates and lists what the tool does not do.

**Live site:** https://mosakr970.github.io/tekla-automation-toolkit/

## The macros

| Macro | Runs in | What it does | Verified result | Case study |
|---|---|---|---|---|
| HC Check | Model | Flags hollow-core panels the factory cannot saw | 851 panels measured, 0 disagreements against an independent second implementation | [hc_check](https://mosakr970.github.io/tekla-automation-toolkit/hc_check.html) |
| Insert Tendons | Model | Models post-tensioning tendons and ducts from the designer's Excel profile | 424 parts and 11,282 points across 59 beams, 0 skipped or failed | [insert_tendons.html](insert_tendons.html) |
| EK Mark | Model | Gives identical pieces the same `EK_MARK`, comparing assemblies part by part | 1,356 of 1,357 identical pairs matched Tekla's numbering | [ek_mark.html](ek_mark.html) |
| Auto Dimension | Drawing | Dimensions a drawing view to the grid, chained like a detailer would | 52 of 52 dimension points bound to the model | [auto_dimension.html](auto_dimension.html) |
| Opening Marks | Drawing | Finds every opening in a floor plan and crosses it out | 37 openings on a 1,572-part plan, every line end within 1 mm | [opening_marks.html](opening_marks.html) |

For all five side by side, with what each needs from you and how to install it, see the [Precast Macro Catalog](macro_catalog.html).

## Status and limits

- **Time saved is not measured** for Auto Dimension. Insert Tendons compares a measured ~5 minute session against the team's *estimate* of ~40 hours by hand. HC Check's runtime has not been timed.
- **EK Mark:** the comparison and numbering are verified on a live model. The newest window features (Clear, remembered options, rebar warning) have not been run inside Tekla yet.
- **Opening Marks:** the marks are verified on a live drawing. The placement of dimensions has not been checked yet.
- Each case study lists the tool's other known limits in its own "what it does not do" section.

## Install, in short

1. Copy the `.cs` file into the first folder listed in the `XS_MACRO_DIRECTORY` advanced option (`modeling\` for model macros, `drawings\` for drawing macros).
2. Restart Tekla. It registers macros only at startup.
3. Open **Applications & components → Macros** and run it. Run drawing macros with the drawing open.

Tested with Tekla Structures 2023.0 and 2025.0. Details are in the [catalog](macro_catalog.html).

## Author

Mohamed Sakr, Structural Engineer, BIM & Digital Delivery, Tallinn, Estonia.
[LinkedIn](https://www.linkedin.com/in/mosakr970) · [GitHub](https://github.com/mosakr970) · mo.sakr970@gmail.com
