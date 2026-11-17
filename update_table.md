# Fall 2026 update checklist

Items from the semester review that can't be fixed in the site text alone.
Each one needs a decision, a login, or a re-run of the materials in the live
software. Text-only fixes are already made (see "Already done" at the bottom).

## Needs your input

| # | Where | Description | Suggested fix | Status |
|---|---|---|---|---|
| 1 | `_data/class.yml` → `course.time`, `course.location` | Workshop date/time and room are set to `TBD` (2025 was "Dec 3, 3:30-5pm", "Room TBD"). They appear on the syllabus. | Fill in this year's date/time and room. |  |
| 2 | `_data/class.yml` → `urls` → `mediaspace` | The MediaSpace channel is still the "...Workshop 2025" channel. It's used in the Module 5 slides (`COURSE_MEDIASPACE`) and is now listed on the syllabus. | Keep it, or make a 2026 channel and paste the new URL here. Nothing else needs to change. |  |
| 3 | `date:` front matter in every `module*/lecture*.md` | Lecture dates are still 2025 (Aug-Oct 2025). They aren't shown anywhere. | Optional: set them to the workshop date, or leave as is. |  |

## Walkthroughs: re-run in the current software

The walkthroughs exist in three copies: the Google Doc (source), the PDF
(`assets/pdfs/`) and the HTML (`assets/webpages/`). Suggested workflow: edit
the Google Doc, then re-export both the PDF and the HTML ("Download → Web page")
so the three stay in sync. Then check that the MediaSpace videos linked from
Modules 3 and 4 still match.

| # | Walkthrough | Description | Suggested fix | Status |
|---|---|---|---|---|
| 4 | WT2 & WT3 (Filled map sections) | **Microsoft is retiring the Bing-based Map / Filled map visuals in favor of the Azure Maps visual.** No firm removal date has been published, but third-party reports say it was deprecated around mid/late 2025. WT2's "Attempt #2: Adding in a Map Visualization" and all of WT3's "PowerBI Plot #2: Filled World Map" (Location field, tooltips, `fx` gradient conditional formatting, "Dark"/"Aerial" map style) depend on it. | Open Power BI online and check whether "Filled map" is still in the Visualizations pane. If it's gone or shows a deprecation warning, redo both sections with the **Azure Maps** visual (Location → Country; bubble/filled-layer color by "corgis born") and replace the screenshots. Microsoft's conversion guide: https://learn.microsoft.com/en-us/azure/azure-maps/power-bi-visual-conversion |  |
| 5 | WT1, "Making a New Report" | Steps depend on exact UI labels: green "New Report" button, "Paste or manually enter data", the 2-vs-4 option screen, "CSV (Preview)", connection name + "Anonymous" authentication, the "Loading Data" screen. | Step through with the corgis URL and update labels and screenshots where they changed. |  |
| 6 | WT1, rest of walkthrough | File → save to "My workspace", "Edit" button, "Clustered column chart", "Format visual" (paint icon), "Rename for this visual", "Read View". | Same as above. Also check the formatting-panel layout, which Microsoft reshuffles often. |  |
| 7 | WT2 | "Slicer" visual, slicer format options ("between"/"less than"/"greater than"). | Re-run and update screenshots. Microsoft has been adding new slicer types (e.g. "Button slicer"), so the slicer pane and defaults may look different. |  |
| 8 | WT3, Excel / Power Query (Mac) | "Data → Get Data (Power Query) → Get Data (Power Query)...", "Text/CSV", "Launch Power Query Editor...", "add type conversion as separate step", Add Prefix, Unpivot other columns, "Close & load", Save As → "Online Locations". | Re-run in current Excel for Mac (and Windows if possible). Update menu names and screenshots. |  |
| 9 | WT3, uploading to Power BI | "Excel (Preview)" option, "Upload" vs "Browse OneDrive", the "OneDrive cannot link" workaround, sheet-picker preview. | Re-run and update. |  |
| 10 | WT3 numbering | Steps go Step 1 → Step 2 → **Step 4** → Step 5 (no Step 3). | Renumber while editing the Google Doc. (This is also in the general/typo list.) |  |

## Walkthroughs: leftovers from the semester course

These sentences refer to IS445/IS457 course infrastructure (Canvas, SP25
files, Google Data Studio activities) that workshop participants don't have.
Fix them in the Google Doc, then re-export.

| # | Walkthrough | Current text | Suggested fix | Status |
|---|---|---|---|---|
| 11 | WT1 summary | "...similar barchart with the corgis dataset to the one we made in Google Data Studio in prior weeks." | "...a simple barchart with the corgis dataset." |  |
| 12 | WT1, WT2, WT3 "Notes for instructors" | "Example file is the "Dashboard1/2/3, SP25..." file in the "IS457 Prep Materials (SP25)" Workspace" | Point to the 2026 example files/workspace, or remove the note from the student-facing copies. |  |
| 13 | WT1 | "...we will be using the online version only for this class." / "For the purposes of this course..." / "For the purposes of this class..." | "class"/"course" → "workshop". |  |
| 14 | WT1 | "This link is also under "PowerBI resources" at the top of our Canvas page." | "This link is also on the syllabus and the Module 1 and Module 3 pages of the workshop website." |  |
| 15 | WT1 | "...you all will have access to our class workspace (view only) to get the example PowerBI files." | Remove, or describe how workshop participants get the example files. |  |
| 16 | WT1 | CSV options: "upload the CSV file that you downloaded from the prior Google Data Studio activity" / "Upload the CSV file linked on Canvas" | Replace both with "download the CSV linked under 'Data' on the Module 3 page and upload it." |  |
| 17 | WT1 | "give it a useful name (Like "Dashboard1, SP25)" (also later: "Dashboard1, SP25") | Use a semester-neutral name such as "Dashboard1", and close the quote. |  |
| 18 | WT2 | "A few things we didn't do (that we did in Google Data Studio) were add some interactive filtering..." | Drop the Google Data Studio clause. |  |
| 19 | WT3 | "...proper date formatting (just like we did with GDS through Google Sheets)." | Drop the parenthetical. |  |
| 20 | WT3, Step 1 | "...or downloading from the course Canvas site." | "...or from the 'Data' link on the Module 3/4 page of the workshop website." |  |

## Links and setup steps to verify by hand

The automated link check couldn't confirm these: the servers blocked
non-browser requests, the pages need an Illinois login, or the flow may have
changed.

| # | Where | Description | Suggested fix | Status |
|---|---|---|---|---|
| 21 | Syllabus, Module 1, Lecture 1.0 | Illinois WebStore Excel page (`zpid=2816`) and the `go.illinois.edu/office365` → "Install and more" → "Install Microsoft 365 apps" flow, plus screenshots in `module01/images/excel/`. | Click through and refresh the screenshots if the Office portal changed. |  |
| 22 | Syllabus step 4, Module 1 | Google Apps @ Illinois toggle at `cloud-dashboard.illinois.edu/cbdash/` and the help page (`ServiceDet?ID=135`); screenshot `module01/images/googledocsUse.png`. | Confirm it still works. This step is only needed to open the Google Doc walkthroughs, so it could be dropped if you point people to the PDF/HTML versions. |  |
| 23 | Syllabus, Modules 3 & 4 | The three Google Doc walkthrough links (returned 401 = Illinois-only sharing, as expected). | Confirm they open with an @illinois.edu account, and that the sharing setting is what you want. |  |
| 24 | Lecture 5.1 | Power BI Desktop download link (`download/details.aspx?id=58494`) returned 403 to the checker. Microsoft also distributes Desktop through the Microsoft Store. | Open in a browser. If it redirects or is retired, use the Power BI Desktop product page (https://www.microsoft.com/en-us/microsoft-fabric/features/power-bi/desktop, checked working). |  |
| 25 | Syllabus, Module 3 | "Microsoft's Getting Started with PowerBI" (`microsoft.com/en-us/power-platform/products/power-bi/getting-started-with-power-bi`) returned 403. | Open in a browser and replace if it's dead. |  |
| 26 | Lecture 3.1 | Screenshots of Power BI online (`powerbi_first_view.png`, `selectlanguage1/2.png`, `find_powerbi_app.png`, `pin_powerbi_app.png`) and the Outlook "Apps" panel. | Compare with the current UI and retake if needed. |  |
| 27 | Lecture 4.1 | `changingLanguageExcel.png` (Excel for Mac language setting). | Compare with current Excel and retake if needed. |  |
| 28 | Lecture 5.1 | New wording for the Power BI Desktop and Tableau pros/cons (see "Already done"). | Read once to confirm you're happy with it. |  |

## Already done (for reference)

- `_config.yml`: `baseurl` → `/scholars_powerbi2026`. Added `githuburlbase` and a "change these every semester" header. `url` no longer has a trailing slash. Fixed the description typo ("website **for** the").
- `_data/class.yml`: semester → Fall 2026, number → PowerBI 2026. Added a header explaining how to use the values. Added `urls` entries for `mediaspace` and `is445` (these now also show on the syllabus info box).
- `_layouts/lecture.html`: slides now substitute `COURSE_WEBPAGE`, `COURSE_GITHUB`, `COURSE_MEDIASPACE`, `COURSE_IS445`, `COURSE_SEMESTER`, `COURSE_NUMBER`, `COURSE_NAME`.
- `_layouts/week.html` + `_layouts/index.html`: new resource-link `type: github`. Its `link:` is a path in the repo, and the layout builds the full GitHub URL from `_config.yml`. The walkthrough PDF links in `module03/index.md` and `module04/index.md` use it.
- `syllabus.md`, `module03/index.md`, `module04/index.md`: PDF links in the page body are built from `site.githuburlbase` / `site.baseurl` / `site.branch`.
- `_includes/header.html`: GitHub nav link built from `site.githuburlbase`.
- Lecture 1.1: workshop/syllabus URLs → `COURSE_WEBPAGE`.
- Lecture 5.1: MediaSpace → `COURSE_MEDIASPACE`; IS445 link → `COURSE_IS445` (now the Fall 2026 site). Power BI Desktop is no longer listed as "$$" (it's free, but sharing needs a Pro license). Replaced Tableau's "active development is less" with a note about Tableau Public.
- Lecture 3.1: replaced the outdated Microsoft quote with the current "Power BI overview" wording; "class" → "workshop"; removed the Canvas reference.
- Lectures 1.0 and 2.1: removed Canvas, reading-quiz and "next week" references from slides and speaker notes.
