Y-Lab website — editing the site without touching the code
============================================================

Everything on the site that changes over time lives in plain text files in this
folder, next to index.html. Edit a file on GitHub (or locally), commit, and the
published page shows the new content after a refresh. index.html itself never
needs to be touched.

  publications.bib   Publications page (BibTeX)
  news.json          Home "Recent news" (newest 3) + Notice > News (all)
  members.json       People page
  gallery.json       Notice > Gallery
  positions.json     Join Us openings

RULES THAT APPLY TO EVERY .json FILE
------------------------------------
* The file is a list, written between [ and ]. Each entry is a { ... } block,
  separated by commas. The last entry has NO comma after it.
* JSON has no comments. Instead, the first entry of every file is a worked
  EXAMPLE. Any entry containing   "example": true   is skipped by the website,
  so the example never appears online. To add a real entry: copy the example
  block, paste it where you want it, delete the "example": true line, edit the
  values.
* Order in the file is the order on the page. Newest first is the convention
  for news and gallery.
* Text values go in double quotes. A double quote inside text must be written
  as \" and a backslash as \\.
* If a file has a typo and cannot be read, only that section of the site shows
  "could not be loaded" — the rest of the page keeps working. Paste the file
  into jsonlint.com if you are unsure.

news.json
---------
  date   Short label shown in the left column, e.g. "Sep 2026".
  text   One sentence. Shown on Home (3 newest) and on Notice > News (all).

members.json
------------
  id        Internal key, lowercase, no spaces. Must be unique.
  name      Display name, e.g. "Jaekak Yoo".
  role      Blue line above the name, e.g. "Principal Investigator",
            "PhD Student", "Undergraduate Researcher".
  title     Grey line under the name, e.g. "Assistant Professor".
  photoId   Photo file name without extension: images/<photoId>.jpg
            (.png also works). Leave the file out and a grey placeholder shows.
  office    Room and building.
  email     Shown as a mailto link.
  phone     Optional. Leave as "" to hide the phone line.
  scholar   Optional Google Scholar URL. "" hides the button.
  linkedin  Optional LinkedIn URL. "" hides the button.
  history   List of { "period", "text", "place" } rows, newest first:
              period  "2026 – present"
              text    Position or degree
              place   Institution, advisor in parentheses if relevant

gallery.json
------------
  id           Photo file name without extension: images/<id>.jpg
  caption      One line under the photo.
  date         Small grey line under the caption, e.g. "Sep 2026".
  placeholder  Text shown in the grey box until the photo file exists.

positions.json
--------------
  title   Card heading, e.g. "Graduate Students (MS / PhD)".
  desc    One or two sentences. Delete an entry to close a position.

publications.bib
----------------
Standard BibTeX. Paste the entry from the publisher and save. Notes:
  * Papers are numbered oldest to newest automatically.
  * doi = {10.xxxx/yyyy} makes the title a link.
  * An entry with no year (@unpublished) is grouped under "In Preparation";
    note = {Submitted} or note = {Accepted} is shown next to it.
  * Author marks: put the symbol right after the name inside the braces —
    "J. Yoo†" for equal contribution, "M. S. Jeong*" for corresponding author.
  * Graphical abstract: images/<year>_<journal abbreviation>.jpg, e.g.
    images/2024_NT.jpg for the Nano Today 2024 paper. Add  abbrev = {NT},  to
    the entry to set the abbreviation by hand. images/README.txt lists the exact
    file name for every paper currently in the list.

images/
-------
Drop .jpg or .png files in the images folder; the site picks them up by name.
  images/home-hero.jpg          Home key visual
  images/proj-1.jpg proj-2.jpg proj-3.jpg   Research topic figures, in page order
  images/prof-photo.jpg         Portrait (photoId in members.json)
  images/gal-1.jpg              Gallery photo (id in gallery.json)
  images/<year>_<abbr>.jpg      Graphical abstract, e.g. images/2024_NT.jpg
