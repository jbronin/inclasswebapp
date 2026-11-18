# Project prompts

## 2026-11-18 14:03:20 -0700

Build stage 1 from the Build stages section of spec.md: a mockup of the app as a single file named index.html. Use plain HTML, CSS, and JavaScript with no build tools. You may load libraries from a CDN. Show every input, output, and plot from the spec, filled with realistic placeholder values. Don't write any calculations yet.

Summary: Created the stage 1 Beam Designer mockup in `index.html` with the complete input panel, beam and load drawing, three placeholder diagrams, design check cards, and lightest-section suggestion. Added UI-only interactions for synchronized inputs, adding/removing loads, material switching, and aligned diagram crosshair movement. No structural calculations were implemented.

## 2026-11-18 14:09:38 -0700

Build stage 2 from the Build stages section of spec.md. Only build this stage. Put the calculations in their own clearly named functions, separate from the drawing code.

Summary: Implemented the stage 2 calculation engine in `index.html` with named functions for reactions, shear, moment, deflection, beam results, and lightest passing sections. Added the section tables, load/model collection, bending and deflection calculations, and automatic calculation display updates for inputs. Kept drawing/diagram code separate from the calculation functions and exposed the calculation API as `window.BeamCalculations`.

## 2026-11-18 14:17:36 -0700

build stage 3 Only build this stage. Put the calculations in their own clearly named functions, separate from the drawing code.

Summary: Implemented stage 3 live drawing integration in `index.html`. Added calculated SVG beam supports and loading, dynamic point/uniform load arrows and reactions, filled shear/moment/deflection diagrams with maximum labels, aligned mouse crosshairs with V/M/y hover values, and immediate updates for input changes. Added the "Use section" action and kept drawing functions separate from the existing named calculation functions.

## 2026-11-18 14:19:35 -0700

run stage 4 Only build this stage. Put the calculations in their own clearly named functions, separate from the drawing code.

Summary: Added stage 4 benchmark validation for the four cases in `spec.md`, exposed as `window.BeamValidation.validateFourCases()`, and ran it automatically during page startup.

## 2026-11-18 14:24:00 -0700

Fix the point-load position control so its maximum matches the current beam span.

Summary: Updated point-load position sliders and number inputs to use the current beam span as their maximum. Existing point positions are clamped when the span decreases, and newly added point loads default to the span midpoint or cantilever free end within the span.