# UUT Transfer mobile web demo

## Package
index.html is a self-contained HTML/CSS/JavaScript app. No build step, dependencies, Python runtime, secrets, or external assets. .nojekyll disables Jekyll processing. All paths, workbook fields, file sizes and copy actions are illustrative. No real workbook is loaded and no real files are copied. Do not add private operational data to this public repository.

## GitHub Pages setup
1. Open https://github.com/azalmusa-coder/uut-transfer-demo/settings/pages while signed in.
2. Under Build and deployment, choose Deploy from a branch.
3. Choose main and / (root), then Save.
4. Wait for the Pages deployment to succeed. Use the published URL shown in Settings > Pages. The expected default URL is https://azalmusa-coder.github.io/uut-transfer-demo/ .
5. Open that URL in Safari or Chrome on your phone. Once configured, later pushes to main trigger publication.

## Mobile configuration
The viewport uses width=device-width, initial-scale=1, viewport-fit=cover; zoom is not disabled. The grid becomes one column at 560px. Buttons have a 48px minimum height, inputs use 16px text, paths wrap, and dialogs scroll within the viewport. Safe-area padding accommodates display cutouts.

Touch, pen and mouse input use pointerdown/up/cancel/leave handlers for pressed-state feedback. Activation uses click only so a tap does not execute twice and keyboard activation remains available. touch-action: manipulation is scoped to buttons; page scrolling and pinch zoom are not globally prevented.

## Verification checklist
- Test at 320px, 390px, and desktop widths; rotate the phone.
- Edit sample values and check the target path.
- Tap Start Copy Demo; verify the conflict dialog opens.
- Run three times and test Skip, Keep Both, and Overwrite.
- Verify completion reaches 3/3; Reset clears progress and activity.
- Try scrolling off a button mid-touch: it must not remain visually pressed.
- Test keyboard Tab/Enter and Escape (Escape skips the conflict).
- Confirm no horizontal overflow, pinch zoom works, and no console errors occur.

## Scope
This is a browser interface simulation, not a deployed version of the Windows Python file-transfer application. A real transfer service needs a separately secured Windows backend; do not expose arbitrary file-copy operations publicly.
