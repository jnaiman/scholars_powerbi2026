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
| 10 | WT3 numbering | Steps go Step 1 → Step 2 → **Step 4** → Step 5 (no Step 3). | **HTML copy fixed** (now Step 1 → 4). Still renumber in the Google Doc and re-export the PDF (see #31). |  |

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
| 17 | WT1 | "give it a useful name (Like "Dashboard1, SP25)" (also later: "Dashboard1, SP25") | Use a semester-neutral name such as "Dashboard1". (The missing closing quote is fixed in the HTML copy; see #31.) |  |
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

## Part 2: needs checking or a decision

| # | Where | Description | Suggested fix | Status |
|---|---|---|---|---|
| 29 | Repo: `_site/` | `_site/` (the old local build) is committed. GitHub Pages builds the site itself, and the committed copy goes stale. I added a `.gitignore` for `_site/`, `.DS_Store` and `*~`, but files that are already tracked stay tracked until you remove them. | Run `git rm -r --cached _site` and commit. This only removes them from git, not from disk. |  |
| 30 | Repo: leftover files | Template leftovers not used by this site: `_config.yml~`, `_data/class.yml~`, tracked `.DS_Store` files, `_layouts/index_old.html`, `_layouts/week_old.html`, `Makefile` (points to `/home/mturk/...`), `dodo.py`, `nbv.html`, the empty `helpful_setup.md`, and `module01/_lecture01p2.md` (an unpublished quiz lecture from IS445 whose 4 images are missing). | Delete the ones you don't want: `git rm` the backup/`.DS_Store` files, then decide on the rest. If you keep `helpful_setup.md`, either write it or exclude it. It's currently published as an empty page. |  |
| 31 | All three walkthroughs | I made these edits directly in the **HTML copies** only: alt text on 95 images (the other 2 already had alt text), WT1 typos ("corgis born", "down-caret", closing quote), and WT3 typos (step renumbering, "than", "latter", "choropleth", missing ")"). If you re-export HTML from the Google Docs, all of this is overwritten. | Make the same text edits in the Google Docs. For alt text, right-click each image → "Alt text" in Google Docs; it carries into the HTML export. Then re-export the PDFs. The alt text to copy over is in the review table below. |  |
| 32 | Modules 3 & 4 → Data | The corgi dataset's "scraped using Beautiful Soup" and "further processed in Python" links pointed to `UIUC-iSchool-DataViz/spring2020`, which no longer exists (404). I kept the wording and removed the dead links. IS445 (`week09/index.md`, `week13/index.md`) has the same dead links. | If you still have `grabCorgData_subpages.py` / `calc_corgData.ipynb`, put them somewhere public (e.g. the `is445_data` repo) and restore the links here and in IS445. |  |
| 33 | Lecture 2.1, chart-types slide | The image was hotlinked from `formations.imt-atlantique.fr`, a domain that no longer resolves (and has no Wayback copy). The slide now uses the local copy already in `module02/images/types_of_charts/charts_types.jpg`, with a "Source: online-behavior.com" line added, based on the README in that folder. | Confirm the source credit is right. |  |
| 34 | Lecture 2.1, other hotlinked images | The 12 perception images still load from `csc2.ncsu.edu`; the Tufte images load from geeksforgeeks.org and YouTube's thumbnail server. They work today, but any could disappear the way the chart-types image did. | Optional: download local copies into `module02/images/` and add source lines. |  |
| 35 | Lecture 1.0 `date:` | Lectures are now actually sorted by date (the layouts used a non-existent `sorted` filter, so order had been by filename). Lecture 1.0 was dated *after* 1.1, so I changed its date from 2025-09-25 to 2025-08-27 to keep it first. | Keep the order in mind if you change lecture dates (#3). |  |
| 36 | Optional activity screenshots | `module04/images/click_on_report.png` shows the "IS457 Prep Materials (SP25)" workspace; `include_data_from_report.png` shows your browser tabs and bookmarks bar (Canvas, PrairieLearn, IS445/IS457 links). | Optional: retake both in a neutral workspace or browser window. |  |
| 37 | Lecture 2.1 speaker notes | The notes after the data-to-viz `<embed>` slides depend on that site allowing itself to be embedded. It loads today, but if the slide ever shows a blank frame, link to the site instead. | Check during your run-through. |  |

## Alt text to review

I wrote all of the alt text below, using no tools beyond viewing each image and its surrounding text. The one exception is the OCR figure in Lecture 1.1, which comes from IS445. IS445 had no alt text for the other images these pages share. Please read each one and correct anything that's wrong or doesn't say what you want the image to convey. The walkthrough entries also need to go into the Google Docs (#31).

| # | File | Image | Alt text added | Status |
|---|---|---|---|---|
| A1 | module01/lecture01p1.md | `images/intro_naiman1.png` | Simulation rendering of the cosmic web from the Illustris project: glowing orange gas clusters connected by a network of blue filaments. |  |
| A2 | module01/lecture01p1.md | `images/intro_naiman2.png` | The same Illustris cosmic web rendering with the word 'SCIENCE!' overlaid. |  |
| A3 | module01/lecture01p1.md | `images/intro_naiman3.png` | The Illustris rendering annotated: blue 'Dark matter filaments (most of the matter in the Universe)' and bright 'Concentrations where gas collects and forms galaxies'; a scale bar reads about 3 x 10^18 meters. |  |
| A4 | module01/lecture01p1.md | `images/intro_naiman4.png` | The Illustris rendering with three zoomed-in insets showing individual simulated galaxies, two spirals and one elliptical, inside the cosmic web. |  |
| A5 | module01/lecture01p1.md | `images/intro_naiman5.png` | Diagram of volume rendering: a camera looks through an image plane into a 3D grid of blue simulation data, with an opacity map and color map that control how data values become pixels. |  |
| A6 | module01/lecture01p1.md | `images/intro_naiman6.png` | Comparison of a 'Simple' and a 'Complex' transfer function: a linear opacity map and grayscale color map give a gray rendering, while a multi-peaked opacity map and multi-color map give a detailed orange-and-purple rendering. |  |
| A7 | module01/lecture01p1.md | `images/intro_naiman7.png` | Cinematic rendering of a cosmological simulation with glowing gas bubbles and blue filaments, made by AVL/NCSA at the University of Illinois with data from Brian O'Shea, Michigan State. |  |
| A8 | module01/lecture01p1.md | `images/intro_naiman8.png` | Two scientific visualizations from the CADENS project (cadens.ncsa.illinois.edu): the Sun with looping blue magnetic field lines, and the solar wind streaming past a planet. |  |
| A9 | module01/lecture01p1.md | `www.astronaiman.com/assets/img/digitization_project/figure_axis_readin` | Image showing optical character recognition (OCR) applied to a technical image of the sky with declination (y) and right ascension (x) axis.  The raw OCR is processed into metadata to be added to the original image to give its location in the sky. (from IS445) |  |
| A10 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_closure.gif` | Field of open C-shaped rings with one closed circle among them. |  |
| A11 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_hue.gif` | Field of short blue dashes with one red dash among them. |  |
| A12 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_size.gif` | Field of short blue dashes with one larger dash among them. |  |
| A13 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_den.gif` | Field of short blue dashes with one region where the dashes are packed more densely. |  |
| A14 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_curve.gif` | Field of straight blue dashes with one curved dash among them. |  |
| A15 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_lum.gif` | Field of blue dashes with one lighter, brighter blue dash among them. |  |
| A16 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_orient.gif` | Field of horizontal blue dashes with one tilted dash among them. |  |
| A17 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_3d_depth.gif` | Field of shaded 3D spheres with one sphere that appears to sit at a different depth from the rest. |  |
| A18 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_isect.gif` | Field of L-shaped marks with one plus sign (two intersecting lines) among them. |  |
| A19 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/tg_term.gif` | Field of L-shaped marks with one T-shaped mark, whose line ends differ, among them. |  |
| A20 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/colour_A.gif` | Field of blue dots, all the same color, with no red dot. |  |
| A21 | module02/lecture2p1.md | `www.csc2.ncsu.edu/faculty/healey/PP/figs/colour_P.gif` | Field of blue dots with a single red dot that stands out immediately. |  |
| A22 | module02/lecture2p1.md | `images/perception_channels/stevensLaw.png` | Stevens' psychophysical power law plot of perceived sensation versus physical intensity: electric shock (exponent 3.5) and saturation (1.7) curve upward, length (1) is a straight line, and area (0.7), depth (0.67) and brightness (0.5) curve downward. From Tamara Munzner, data from Stevens. |  |
| A23 | module02/lecture2p1.md | `images/perception_channels/vad_slides_p51.png` | Munzner's channel rankings. Magnitude channels for ordered attributes, from most to least effective: position on common scale, position on unaligned scale, length, tilt/angle, area, depth, color luminance, color saturation, curvature, volume. Identity channels for categorical attributes: spatial region, color hue, motion, shape. |  |
| A24 | module02/lecture2p1.md | `images/types_of_charts/charts_types.jpg` | Hand-drawn infographic 'Nuts and Bolts of Chart Types' from online-behavior.com, with sketches and joke captions for 12 charts including histogram, bar, pie, line, area, bubble, radar, waterfall, tree map, scatterplot and box plot. |  |
| A25 | module02/lecture2p1.md | `images/types_of_charts/pie_chart.png` | Hand-drawn pie chart with the caption 'Extremely useful when creating a well designed document that is intended to people that will not read the data (e.g. management)'. |  |
| A26 | module02/lecture2p1.md | `images/types_of_charts/histogram.png` | Hand-drawn histogram with the caption 'Chart used by responsible analysts who understand the power of segmentation and the sadness that comes from aggregating data'. |  |
| A27 | module02/lecture2p1.md | `images/viz_resources.png` | The Module 2 row of the syllabus table with the links '2. The Data Viz Picker' and '3. Data Viz Caveats' outlined in red. |  |
| A28 | module02/lecture2p1.md | `images/clickonpage.png` | The data-to-viz.com histogram pop-up, with the 'See the dedicated page' link at the bottom outlined in red. |  |
| A29 | module02/lecture2p1.md | `media.geeksforgeeks.org/wp-content/uploads/20240513134644/Pic-1.jpeg` | Infographic of five Tufte principles: 1. Maximize data-ink ratio, 2. Minimize chartjunk, 3. Data over design variation, 4. Use small multiples, 5. Provide context. |  |
| A30 | module02/lecture2p1.md | `images/tufte/g4g_dataInkRatio.jpeg` | The same Tufte principles infographic with principle 1, 'Maximize Data-Ink Ratio', outlined in red. Original from geeksforgeeks.org. |  |
| A31 | module02/lecture2p1.md | `i.ytimg.com/vi/JIMUzJzqaA8/maxresdefault.jpg` | Two versions of the same monthly bar chart (Jan to Sep, 5% to 15%). Left, labeled 'low data-ink ratio', has a teal background and heavy grid lines. Right, labeled 'high data-ink ratio', has only the bars, with white lines cutting through them for the gridlines. |  |
| A32 | module04/lecture4p1.md | `images/datapivoted.png` | Excel table in the original 'wide' format: a Years column (1917, 1918, ...) followed by one column per country (United States, Brazil, Russia, Japan, Vietnam, Germany). |  |
| A33 | module04/lecture4p1.md | `images/dataunpivoted.png` | Excel table in the unpivoted 'long' format with three columns: Date (1/1/17), Country (United States, Brazil, Russia, ...) and corgis born. |  |
| A34 | module04/lecture4p1.md | `upload.wikimedia.org/wikipedia/commons/8/80/Power_Query_User_Interface` | The Power Query editor with its five numbered sections: the ribbon across the top, the queries panel on the left, the data view in the middle, the query settings on the right and the status bar along the bottom. |  |
| A35 | module04/lecture4p1.md | `images/changingLanguageExcel.png` | Excel for Mac with the Tools menu open and 'Language...' highlighted. |  |
| A36 | module04/optional_activity.md | `images/uploadpowerbi.png` | Power BI 'My workspace' with the Import menu open, showing 'From this computer', OneDrive and SharePoint options for importing .pbix files. |  |
| A37 | module04/optional_activity.md | `images/click_on_report.png` | A Power BI workspace listing with the Bad-to-Good Viz Level 1 Report item, the one with the bar chart icon, selected. |  |
| A38 | module04/optional_activity.md | `images/include_data_from_report.png` | An open Power BI report with the File menu outlined in red and the 'What do you want to download?' dialog, where 'A copy of your report and data (.pbix)' is selected. |  |
| A39 | syllabus.md | `module01/images/googledocsUse.png` | The Illinois Cloud Dashboard with the 'Google Apps @ Illinois' account status toggle set to On and outlined in red. |  |
| A40 | _layouts/week.html, _layouts/index.html | `module icons (undraw SVGs)` | alt="" (decorative, so screen readers skip them) |  |
| A41 | walkthrough1 (image 1) | `images/image11.png` | Power BI connection form with 'Connection settings' (Link to file selected, 'File path or URL' box) and 'Connection credentials' fields, including 'Connection name' set to 'Connection' and 'Authentication kind' set to 'Anonymous'. |  |
| A42 | walkthrough1 (image 2) | `images/image7.png` | Outlook on the web with the Apps icon selected in the left panel, opening a 'Find an app' panel of Microsoft apps; the cursor hovers over the Power BI icon, labeled 'Power BI'. |  |
| A43 | walkthrough1 (image 3) | `images/image25.png` | Pinning the PowerBI web app so it shows on your left sidebar in Outlook online. *(your original alt text from the export, left unchanged)* |  |
| A44 | walkthrough1 (image 4) | `images/image18.png` | Interface for initial opening of the PowerBI web version. *(your original alt text from the export, left unchanged)* |  |
| A45 | walkthrough1 (image 5) | `images/image19.png` | Green 'New report' button with a plus sign. |  |
| A46 | walkthrough1 (image 6) | `images/image24.png` | Power BI 'Create' page with a 'Build your first report' banner and, under 'Add data to start building a report', two options: 'Paste or manually enter data' and 'Pick a published semantic model'. |  |
| A47 | walkthrough1 (image 7) | `images/image20.png` | 'Add data to start building a report' screen with four options: 'Excel (Preview)', 'CSV (Preview)', 'Paste or manually enter data', and 'Pick a published semantic model'. |  |
| A48 | walkthrough1 (image 8) | `images/image3.png` | 'Connect to data source' page for a Text/CSV file, with 'Link to file' selected and the raw.githubusercontent.com UIUC-iSchool-DataViz URL pasted into the 'File path or URL' box. |  |
| A49 | walkthrough1 (image 9) | `images/image11.png` | Connection settings form where 'Connection name' (currently 'Connection') should be changed to something unique and 'Authentication kind' should be set to 'Anonymous'. |  |
| A50 | walkthrough1 (image 10) | `images/image6.png` | Bottom of the 'Preview file data' page showing part of a data table of zeros above 'Cancel' and a green 'Create' button. |  |
| A51 | walkthrough1 (image 11) | `images/image17.png` | Empty Power BI report editor reading 'Build visuals with your data', with the 'File' menu at top left, 'Filters' and 'Visualizations' panes, and the 'Data' pane listing the corgs_per_country_ov... table. |  |
| A52 | walkthrough1 (image 12) | `images/image13.png` | 'Save your report' dialog with 'My workspace' selected and 'Dashboard1, SP25' entered as the report name, plus 'Save' and 'Cancel' buttons. |  |
| A53 | walkthrough1 (image 13) | `images/image26.png` | Report toolbar with the pencil 'Edit' button. |  |
| A54 | walkthrough1 (image 14) | `images/image21.png` | Empty Power BI report editor now titled 'Dashboard1, SP25' at the top and in the left navigation bar, with the Filters, Visualizations, and Data panes. |  |
| A55 | walkthrough1 (image 15) | `images/image5.png` | Visualizations pane under 'Build visual' with the cursor on the 'Clustered column chart' icon, which shows its name in a tooltip. |  |
| A56 | walkthrough1 (image 16) | `images/image2.png` | Report editor after checking 'Years' and 'United States' in the Data pane: both appear under Y-axis as 'Sum of Years' and 'Sum of United States', and the chart shows only one tall bar for years and one short bar for the United States. |  |
| A57 | walkthrough1 (image 17) | `images/image10.png` | Visualizations pane with the clustered column chart selected, 'Years' now in the X-axis field and 'Sum of United States' in the Y-axis field. |  |
| A58 | walkthrough1 (image 18) | `images/image23.png` | Data pane with 'United Kingd...' checked and outlined in red, and a red arrow pointing to the new 'Sum of United Kingdo...' entry under Y-axis below 'Sum of United States'. |  |
| A59 | walkthrough1 (image 19) | `images/image12.png` | Unformatted clustered column chart titled 'Sum of United States and Sum of United Kingdom by Years', with small axis text, light blue US bars peaking above 600 around 2000, and similar dark blue UK bars that stay under 100. |  |
| A60 | walkthrough1 (image 20) | `images/image14.png` | Visualizations pane with the paintbrush 'Format visual' icon outlined in red, above the 'Visual' and 'General' tabs. |  |
| A61 | walkthrough1 (image 21) | `images/image22.png` | 'Format visual' pane on the 'Visual' tab with the 'X-axis' section expanded; under 'Title', the font size box (set to 12) is outlined in red. |  |
| A62 | walkthrough1 (image 22) | `images/image15.png` | X-axis 'Values' settings with the font size box (set to 9) outlined in red, next to the 'Segoe UI' font menu. |  |
| A63 | walkthrough1 (image 23) | `images/image4.png` | Y-axis 'Title' settings with the toggle 'On' and 'Title text' set to '# of Corgis'. |  |
| A64 | walkthrough1 (image 24) | `images/image8.png` | 'Columns' settings with 'Series' set to 'Sum of United Kingd...' and the 'Color' picker set to pink, with 'Transparency' at 0%. |  |
| A65 | walkthrough1 (image 25) | `images/image9.png` | 'Format visual' pane with the paintbrush icon, the 'General' tab, and the expanded 'Title' section outlined in red; the title 'Text' box begins 'Number of Corgis Bo...'. |  |
| A66 | walkthrough1 (image 26) | `images/image16.png` | 'Build visual' pane with the dropdown arrow on the 'Sum of United States' Y-axis field opened and 'Rename for this visual' outlined in red. |  |
| A67 | walkthrough1 (image 27) | `images/image1.png` | Finished chart in reading view titled 'Number of Corgis Born over Time', with a '# of Corgis' y-axis, a 'Years' x-axis from 1920 to 2020, blue United States bars peaking above 600 around 2000, and pink United Kingdom bars that stay under about 75. |  |
| A68 | walkthrough2 (image 1) | `images/image2.png` | Power BI report in view mode showing the bar chart 'Number of Corgis Born over Time', with United States (blue) and United Kingdom (pink) bars by year from about 1920 to 2020 and '# of Corgis' on the y-axis; US births peak near 600 around 2000. |  |
| A69 | walkthrough2 (image 2) | `images/image10.png` | Power BI report toolbar for 'Dashboard2, SP25, Starting Interactivity (unpivoted dataset)' with the 'Edit' button (pencil icon) outlined in red, next to File, Export, Share, Explore and Subscribe. |  |
| A70 | walkthrough2 (image 3) | `images/image13.png` | Power BI edit view with the 'Number of Corgis Born over Time' bar chart resized to fill only the top portion of the page, leaving empty space below; the Visualizations and Data panes are open on the right. |  |
| A71 | walkthrough2 (image 4) | `images/image7.png` | Visualizations pane under 'Build visual' with the Slicer icon (a small table with a funnel) outlined in red. |  |
| A72 | walkthrough2 (image 5) | `images/image9.png` | A blank slicer placed below the bar chart, showing a grey placeholder list of checkboxes and the message 'Select or drag fields to populate this visual'. |  |
| A73 | walkthrough2 (image 6) | `images/image6.png` | Visualizations pane with the slicer's 'Field' well now containing 'Years'. |  |
| A74 | walkthrough2 (image 7) | `images/image5.png` | Bar chart filtered to the years 1963 to 2009, with a 'Years' range slider below it showing those start and end values and two draggable handles. |  |
| A75 | walkthrough2 (image 8) | `images/image15.png` | Visualizations pane with the 'Format visual' (paintbrush) button outlined in red, showing the Visual tab sections 'Slicer settings' (with 'Options'), 'Slicer header' (On), 'Values', and 'Slider' (On). |  |
| A76 | walkthrough2 (image 9) | `images/image12.png` | Bar chart above a smaller, resized 'Years' slicer with larger text, moved to the lower right and set to 1963 and 2009, leaving empty space on the left for more elements. |  |
| A77 | walkthrough2 (image 10) | `images/image3.png` | A slicer with the fields 'Switzerland', 'Spain' and 'Serbia' in its Field well; the slicer lists numeric values (0, 1, 2, 3, 4, 6) as checkboxes instead of country names. |  |
| A78 | walkthrough2 (image 11) | `images/image14.png` | Visualizations pane under 'Build visual' with the Filled map icon outlined in red. |  |
| A79 | walkthrough2 (image 12) | `images/image4.png` | An empty Filled map visual showing a grey placeholder map graphic and the message 'Select or drag fields to populate this visual'. |  |
| A80 | walkthrough2 (image 13) | `images/image1.png` | Filled map field wells in the Visualizations pane: 'Location', 'Legend', 'Latitude' and 'Longitude', each reading 'Add data fields here'. |  |
| A81 | walkthrough2 (image 14) | `images/image11.png` | Filled map field wells with 'Russia' and 'Slovenia' added under 'Location' and 'Spain' under 'Legend'. |  |
| A82 | walkthrough2 (image 15) | `images/image8.png` | Filled map titled 'Russia and Spain' with legend 'Spain 0', showing a few small blue shaded regions in central and southern France rather than the countries named in the fields. |  |
| A83 | walkthrough3 (image 1) | `images/image1.png` | Microsoft 365 Copilot home page with the 'Install and more' button in the upper right highlighted and its dropdown option 'Install Microsoft 365 apps' (Install Word, Excel, PowerPoint, and more) highlighted. |  |
| A84 | walkthrough3 (image 2) | `images/image23.png` | Microsoft 365 'My account' page with the 'Install Office' button highlighted under the 'Office apps & devices' section. |  |
| A85 | walkthrough3 (image 3) | `images/image22.png` | The green Microsoft Excel app icon. |  |
| A86 | walkthrough3 (image 4) | `images/image18.png` | A new blank Excel workbook (Book2) open on a Mac, showing the Home ribbon and an empty grid of cells on Sheet1. |  |
| A87 | walkthrough3 (image 5) | `images/image12.png` | Excel General preferences window with the 'Font size' setting next to 'Default font: Body Font' highlighted and set to 18. |  |
| A88 | walkthrough3 (image 6) | `images/image40.png` | macOS Accessibility Zoom settings with 'Use scroll gesture with modifier keys to zoom' turned on and 'Modifier key for scroll gesture' set to 'Control', both highlighted. |  |
| A89 | walkthrough3 (image 7) | `images/image54.png` | Dashboard from last time: a 'Number of Corgis Born over Time' bar chart comparing United States and United Kingdom, a map of France titled 'Russia and Spain', a 'Years' slider set from 1963 to 2009, and a slicer titled 'Switzerland, Spain, Serbia' that lists numbers (0, 1, 2, 3...) instead of country names. |  |
| A90 | walkthrough3 (image 8) | `images/image52.png` | Original Excel table in wide format: a 'Years' column (1917, 1918, ...) followed by one column per country (United States, Brazil, Russia, Japan, Vietnam, Germany, ...) holding the number of corgis born. |  |
| A91 | walkthrough3 (image 9) | `images/image45.png` | Target Excel table in long format with three columns: Date (1/1/17), Country (United States, Brazil, Russia, ...), and corgis born. |  |
| A92 | walkthrough3 (image 10) | `images/image16.png` | Excel Data tab with the Get Data dropdown open and 'Get Data (Power Query)...' highlighted at the top of the menu. |  |
| A93 | walkthrough3 (image 11) | `images/image25.png` | Power Query 'Choose data source' dialog with the 'Text/CSV' option (Import data from a text or CSV file) highlighted among options such as Excel workbook, XML, JSON and Blank table. |  |
| A94 | walkthrough3 (image 12) | `images/image15.png` | 'Connect to data source' dialog for Text/CSV showing a 'Browse...' button and the selected local file 'corgs_per_country_over_time_columns_2020 (1).csv'. |  |
| A95 | walkthrough3 (image 13) | `images/image37.png` | 'Preview file data' dialog showing the CSV with a whole-number 'Years' column and one column per country, with Delimiter set to 'Comma' and Back, Cancel, 'Transform data' and green 'Load' buttons at the bottom. |  |
| A96 | walkthrough3 (image 14) | `images/image46.png` | Data loaded straight into Excel as a green-banded table with the Table ribbon tab active; it still has a 'Years' column plus one column per country (United States, Brazil, Russia, ...). |  |
| A97 | walkthrough3 (image 15) | `images/image39.png` | Excel Data tab with the Get Data dropdown open and 'Launch Power Query Editor...' highlighted. |  |
| A98 | walkthrough3 (image 16) | `images/image33.png` | Power Query Editor showing the corgi query: the wide table with 'Years' plus one column per country, the formula bar, and the 'Query settings' panel listing Applied steps 'Source', 'Promoted headers' and 'Changed column type'. |  |
| A99 | walkthrough3 (image 17) | `images/image35.png` | Query settings panel listing the Applied steps 'Source', 'Promoted headers' and 'Changed column type'. |  |
| A100 | walkthrough3 (image 18) | `images/image41.png` | Close-up of the 'Years' column header in Power Query showing the '123' whole-number type icon. |  |
| A101 | walkthrough3 (image 19) | `images/image11.png` | Data type dropdown opened from the '123' icon on the Years column, with the '123' icon and the 'Text' option highlighted. |  |
| A102 | walkthrough3 (image 20) | `images/image2.png` | Applied steps list now showing 'Source', 'Promoted headers', 'Changed column type' and the new 'Changed column type 1' step. |  |
| A103 | walkthrough3 (image 21) | `images/image48.png` | Power Query Transform tab with the Format dropdown open and 'Add prefix' highlighted, with a tooltip explaining it adds a specified text value to the front of each value in the selected column. |  |
| A104 | walkthrough3 (image 22) | `images/image4.png` | Alternate, compact Transform ribbon layout with the Format dropdown open and the cursor on 'Add prefix'; the Years column now has a text (ABC) icon. |  |
| A105 | walkthrough3 (image 23) | `images/image42.png` | 'Prefix' dialog with '01/01/' entered in the Prefix box and the OK button. |  |
| A106 | walkthrough3 (image 24) | `images/image36.png` | Power Query after the prefix step: the Years column now reads 01/01/1917, 01/01/1918, and so on, and 'Added prefix' appears at the bottom of the Applied steps list. |  |
| A107 | walkthrough3 (image 25) | `images/image30.png` | Data type dropdown opened from the text (ABC) icon on the Years column, with the 'Date' option highlighted. |  |
| A108 | walkthrough3 (image 26) | `images/image50.png` | Power Query with the Years column now showing a calendar (Date) icon and values like 1/1/1917, and the new 'Changed column type 2' step highlighted in Applied steps. |  |
| A109 | walkthrough3 (image 27) | `images/image17.png` | Transform tab with the 'Unpivot columns' dropdown open and 'Unpivot other columns' selected, with a tooltip explaining it turns all but the selected columns into attribute-value pairs. |  |
| A110 | walkthrough3 (image 28) | `images/image13.png` | Unpivoted table in Power Query with three columns, Years (1/1/1917), Attribute (country names) and Value (corgi counts), and 'Unpivoted other columns' added to Applied steps. |  |
| A111 | walkthrough3 (image 29) | `images/image43.png` | Power Query table with the columns renamed to 'Date', 'Country' and 'corgis born'. |  |
| A112 | walkthrough3 (image 30) | `images/image51.png` | Power Query Home tab with the 'Close & load' button highlighted. |  |
| A113 | walkthrough3 (image 31) | `images/image53.png` | Excel sheet with the loaded long-format table in three columns: Date, Country and corgis born. |  |
| A114 | walkthrough3 (image 32) | `images/image14.png` | Save As |  |
| A115 | walkthrough3 (image 33) | `images/image5.png` | Mac 'Save As' dialog with the file named 'example_corgs', saved to Downloads, File Format 'Excel Workbook (.xlsx)', and an 'Online Locations' button. |  |
| A116 | walkthrough3 (image 34) | `images/image38.png` | Power BI workspace with the '+ New item' button highlighted and, in the New item panel, the 'Report' option (Create an interactive presentation of your data) highlighted. |  |
| A117 | walkthrough3 (image 35) | `images/image55.png` | Power BI 'Build your first report' page with the 'Excel (Preview)' option highlighted under 'Add data to start building a report'. |  |
| A118 | walkthrough3 (image 36) | `images/image27.png` | 'Connect to data source' page for an Excel workbook with the 'Upload file' radio button and the 'Browse OneDrive...' button highlighted. |  |
| A119 | walkthrough3 (image 37) | `images/image31.png` | 'Connect to data source' page showing 'example_corgs.xlsx' with 'Upload successful (77.3 KB)' and a green 'Next' button at the bottom right. |  |
| A120 | walkthrough3 (image 38) | `images/image24.png` | Power BI Home page with the Profile panel open and the 'View account' link highlighted above the 'Sign out' button. |  |
| A121 | walkthrough3 (image 39) | `images/image10.png` | Power BI 'Choose data' page with three sheets listed under Excel workbook and a preview of the long-format table with Date, Country and corgis born columns, plus a 'Create' button. |  |
| A122 | walkthrough3 (image 40) | `images/image9.png` | Power BI Data pane listing the table's fields: 'corgis born', 'Country' and 'Date'. |  |
| A123 | walkthrough3 (image 41) | `images/image7.png` | Power BI bar chart titled 'Sum of corgis born by Year' showing total corgis rising from the 1920s to about 1500 near 2015, with Date (Year, Quarter, Month, Day) on the X-axis and 'Sum of corgis born' on the Y-axis in the Visualizations pane. |  |
| A124 | walkthrough3 (image 42) | `images/image20.png` | X-axis field well showing 'Date' reduced to only the 'Year' level. |  |
| A125 | walkthrough3 (image 43) | `images/image3.png` | Visualizations field wells with Date/Year on the X-axis, 'Sum of corgis born' on the Y-axis, and 'Country' highlighted in the Legend well. |  |
| A126 | walkthrough3 (image 44) | `images/image6.png` | Cluttered bar chart titled 'Sum of corgis born by Year and Country' with a long color legend of countries (Australia, Austria, Belarus, Belgium, ...) and many thin, faint, overlapping bars. |  |
| A127 | walkthrough3 (image 45) | `images/image21.png` | A Country slicer (Slicer icon and 'Country' Field highlighted in the Visualizations pane) with only Australia checked, so the bar chart shows just Australia's corgi births from the 1950s to 2020. |  |
| A128 | walkthrough3 (image 46) | `images/image28.png` | Format visual pane for the slicer showing Slicer settings: Style 'Vertical list', 'Single select' Off, 'Multi-select with CTRL' On, and 'Show Select all option' Off. |  |
| A129 | walkthrough3 (image 47) | `images/image29.png` | Bar chart 'Sum of corgis born by Year and Country' with Australia, Austria and Belarus selected in the Country slicer below, each shown in a different color. |  |
| A130 | walkthrough3 (image 48) | `images/image19.png` | Dashboard with a new Date slicer (12/30/1948 to 1/1/2020) whose calendar icon is highlighted, next to the Country slicer and the three-country bar chart. |  |
| A131 | walkthrough3 (image 49) | `images/image26.png` | Visualizations pane with the 'Filled map' icon hovered and its tooltip showing. |  |
| A132 | walkthrough3 (image 50) | `images/image49.png` | Filled map titled 'Sum of corgis born by Country' with Australia and parts of Europe shaded, alongside the bar chart and slicers; 'Country' in the Location well and 'Sum of corgis born' in the Tooltips well are highlighted. |  |
| A133 | walkthrough3 (image 51) | `images/image47.png` | Map tooltip over Australia reading 'Country Australia' and 'Sum of corgis born 891'. |  |
| A134 | walkthrough3 (image 52) | `images/image8.png` | Format visual pane for the map with 'Fill colors' > 'Colors' expanded and the 'fx' button next to the Default color highlighted. |  |
| A135 | walkthrough3 (image 53) | `images/image44.png` | 'Default color - Fill colors - Colors' dialog with Format style 'Gradient' and field 'Sum of corgis born' highlighted, running from a light blue lowest value to a dark blue highest value. |  |
| A136 | walkthrough3 (image 54) | `images/image32.png` | Filled map after applying the gradient, where the shaded countries are pale and hard to see against the light default basemap. |  |
| A137 | walkthrough3 (image 55) | `images/image34.png` | Dashboard with the filled map switched to the 'Aerial' style under Map settings > Style, so Australia and the European countries stand out in blue on a dark satellite map. |  |

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

### Part 2 fixes (already done)

- Module 3 and 4 pages: the HTML walkthrough links were broken (`/module03/w1html`) because `_layouts/week.html` had no `webpage` link type. Added it.
- Syllabus: the Lecture 1.0 link pointed to `lecture1p0.html`; it's now `lecture01p0.html`.
- Lecture 1.0: the `go.illinois.edu/office365` links had no `https://`, so they resolved as relative links. Fixed. The speaker notes on the last slide were indented and could show on the slide. Fixed.
- `_layouts/lecture.html`: replaced the dead Font Awesome CSS link (maxcdn, 404) with cdnjs 5.14.0. Removed two commented-out copies of `{{page.content}}` that duplicated every slide deck into the page source, and removed a stray `</style>` tag.
- `_layouts/index.html` + `_layouts/week.html`: `sorted` → `sort`, so lectures are really ordered by date (see #35).
- Alt text: 46 lecture `<img>` tags (37 distinct images), 95 walkthrough images (2 in WT1 already had your alt text and were kept), `alt=""` on decorative module icons. Every `<img>` on the built site now has an `alt` attribute.
- Lecture 2.1: invalid `</br>` → `<br>`; chart-types image is now local (#33).
- Typos: syllabus "it's", "book's" (syllabus + Module 1), Module 2 "your data", "advice", "a list of things", "spaghetti", Lecture 5.1 "fewer features", "trickier", MediaSpace sentence, stray `**` in Lecture 1.1 notes, plus the walkthrough typos in #31.
- README: real title, "Set up" typo, and the empty setup section now explains the per-semester config.
- Added `.gitignore` (#29).
