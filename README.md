# Case Review Notepad

An offline, single-file notepad for seller account reviews. It checks your note while you write it, so nothing gets missed before you give a verdict.

## How to use
1. Download `index.html` and double-click it. It opens in Chrome or Edge with no install and no internet.
2. Enter the Case ID and pick the review type: Restriction, Onboarding/KYC or ATO.
3. Fill each section. Click the phrase chips to insert standard text, then fill the `___` blanks.
4. Mark each section **Checked**, **Issue found** or **N/A**. N/A needs a reason.
5. Pick the final verdict, add final verdict notes and click **Complete note**. It lists anything missed and any conflict, such as "Lift" chosen while an issue was found, then gives the full note to copy.
6. Click **Copy final note** and paste it into your case tool.

## What it checks
- Required sections for the chosen review type that aren't done yet
- Unfilled `___` blanks and very short notes
- Section order: Account profile → Linked account review → ATO indicators → Transaction log → Counterparty / money movement → Service log → Previous teammate notes → Documents → Final verdict
- Counterparty review becomes required once the notes mention counterparties or chargebacks
- Verdict conflicts: Lift/Approve with issues found, Keep/Decline with no issue found, Request info without listing what's needed, an unhandled ATO issue, or a verdict that doesn't fit the review type
- An AHT timer that turns amber at 80% of the target time and red once over it

## Customise
Edit the `CONFIG` block at the top of the `<script>` in `index.html`. You can change the sections, the required sections per review type, the phrase chips and the verdicts.

Notes are saved in the browser's local storage on your own PC. Nothing is sent anywhere. Don't put real customer data in this repository.

Shortcuts: `Ctrl+Enter` next section · `Alt+1/2/3` Checked/Issue/N/A · `Ctrl+Shift+F` complete note
