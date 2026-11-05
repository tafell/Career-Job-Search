# Tools and Troubleshooting

Every workflow supports pasted text and uploaded files. Connect only the tools you want the assistant to use.

| Number | Category | Placeholder | No-connector fallback |
| --- | --- | --- | --- |
| 1 | Email | `~~email` | Paste the relevant alert or correspondence. |
| 2 | File storage | `~~file storage` | Upload the source document and download the separate result. |
| 3 | Application tracker | `~~tracker` | Upload an export and receive proposed rows or a spreadsheet. |

## Access and scope

1. Put alert sources, document locations, and tracker columns in your private profile. Tool categories are not commands or credentials.
2. Connect through your assistant's supported settings. Never paste passwords or access tokens into the profile.
3. Tell the assistant the requested scope: read, draft, create a separate file, or update specified records. A connection alone does not authorize sending correspondence.
4. Web access stays read-only. Use an accessible employer page or pasted text when login or page rendering blocks access.

## Troubleshooting

1. Missing resume: upload the source before full tailoring. A prior generated resume is not independent evidence.
2. Posting blocked or truncated: paste the complete employer description. Source-dependent conclusions remain provisional.
3. Expired posting: retain it with an expired label. An access failure alone does not prove expiration.
4. Unknown pay: treat 0 and 1 as undisclosed. Follow the [shared compensation rule](guides/SHARED-RULES.md); unknown currency or pay period prevents a final comparison.
5. Missing tracker connection: return proposed records; do not claim the tracker was updated.
6. Duplicate opening: compare employer and requisition and preserve distinct requisitions.
7. Scheduled run unavailable: run once and state that no ongoing monitoring was established.
8. Custom assistant creation unavailable: use a private project or paste the instructions into a conversation.
9. Skill not automatically selected: name the workflow and provide its instructions. Uploading a file does not necessarily install an automatic trigger.

## Move the alert run log from Notion to Google Sheets or Excel

The alert run log records which emails were processed. The application tracker records individual roles. You can move either one separately.

1. Choose the destination. For Google Sheets, record the spreadsheet link and tab name. For Excel, record the workbook location and worksheet name. If moving both records, identify each destination separately.
2. Before the next scheduled run, export the Notion log as a comma-separated values file. Import it into the destination worksheet. For Excel, save the result as an Excel workbook. Import identifiers as text so leading zeros and long values survive. Keep the original log available for comparison.
3. Compare row counts and spot-check alert dates, message or posting identifiers, and links. Preserve the fields your workflow uses to recognize processed alerts. Copy any records added since the export before switching.
4. In your private profile under **Documents and tools**, enter `Alert run log: [spreadsheet link or workbook location], worksheet: Alert Runs` and list the actual column names. If only the run log moved, keep the existing application tracker setting. Update any scheduled instructions that name the old log to say “use the alert run log in my private profile.”
5. Test with an alert already in the log. Ask “Which worksheet and row show that this alert was processed? Check without adding a row.” Verify the match before the next scheduled run. Automatic logging requires read and write access to the destination. Without a connection, upload the workbook or paste the relevant rows and request a row to copy manually.

## Choose which alert emails to process

1. In your private profile under **Documents and tools**, enter the full sender address from an alert you want to process. If the sender also sends unrelated messages, add a subject phrase to the scheduled instructions.
2. Specify the time window and what to do when nothing matches. For example, “At each scheduled check, read alerts from my configured sender from the past day. Include only subjects containing [chosen phrase]. Skip alerts already processed. If nothing matches, stop.” Omit the subject condition if every alert from that sender qualifies.
3. Preview the filter once by asking for matching senders, subjects, and dates only. Adjust it before using it in a scheduled run. A manual request or an authorized schedule starts the workflow.
