Y-Lab website — images folder
=============================

Photos are sorted into five subfolders. Both .jpg and .png work everywhere (the
page tries .png first, then .jpg). A slot with no file keeps showing its grey
placeholder, so images can be added one at a time.

  images/webpages/   site figures (home key visual, research topic figures)
  images/people/     member portraits
  images/papers/     graphical abstracts of publications
  images/gallery/    gallery photos
  images/news/       optional photo for a news item


images/webpages/
----------------
  home-hero.jpg      Home key visual (wide, ~16:9)

  Research topics have two slots each — small for the list card, large for the
  detail page that opens when the card is clicked:

  proj-1-small.jpg   Research 01 list card  |  proj-1-large.jpg   Research 01 detail
  proj-2-small.jpg   Research 02 list card  |  proj-2-large.jpg   Research 02 detail
  proj-3-small.jpg   Research 03 list card  |  proj-3-large.jpg   Research 03 detail

  Research 01 = Multimodal AI for Semiconductor Materials Physics
  Research 02 = Scientific Foundation Models for Semiconductor Materials
  Research 03 = Metasurface-Based Excitonic Devices

  The small image is cropped to fill the card, so keep it simple; the large one
  is shown whole, so a full graphical abstract fits. If either file is missing
  the site falls back to proj-1.jpg / proj-2.jpg / proj-3.jpg in this folder,
  so a single file per topic also works.


images/people/
--------------
  prof-photo.jpg     Portrait of the PI (3:4 portrait crop)

  For every other member the file name is the "photoId" in members.json
  (photoId "kim-minji" → images/people/kim-minji.jpg).


images/gallery/
---------------
  gal-1.jpg          The file name is the "id" in gallery.json.


images/news/
------------
  Optional. Add  "image": "opening-day"  to an entry in news.json and put
  images/news/opening-day.jpg in this folder; the photo then shows next to that
  news item on the Notice page. Entries without an "image" stay text-only.


images/papers/
--------------
Named  <year>_<journal abbreviation>.jpg  — e.g. 2024_NT.jpg for the Nano Today
2024 paper. Two papers in the same journal and year get _2 on the second one,
counted in publications.bib order. To choose the abbreviation yourself, add
  abbrev = {NT},   to that paper's .bib entry.

  2026_M.jpg          Macromolecules (2026)
                      Quantum Dot-Induced Kinetic Bottleneck in Singlet Exciton Relaxation of Conjugated Polymer Aggregates
  2026_S.jpg          Small (2026)
                      Ultrawide Charge-Trap Memory Window and Photoinduced Synaptic Behavior in P-Channel Amorphous Oxide Semiconductors
  2026_LAM.jpg        Light: Advanced Manufacturing (2026)
                      Thickness-dependent vibrational properties of high-quality violet phosphorus revealed by tip-enhanced Raman spectroscopy
  2026_CM.jpg         Chemistry of Materials (2026)
                      Site-Selective Doping and Oxidation State Control of Copper in Gold Nanorods
  2026_CAP.jpg        Current Applied Physics (2026)
                      Unveiling physical insight through XAI-based correlative spectroscopy
  2026_ICML.jpg       ICML 2026 (2026)
                      Position: Significant impact of numerical precision in scientific machine learning
  2026_MD.jpg         Materials & Design (2026)
                      Predicting the tip-enhanced Raman spectroscopy performance of nanoprobe using explainable artificial intelligence
  2026_S_2.jpg        Small (2026)
                      Straightening energy puddles in wrinkled monolayer WSe2 via selective passivation
  2026_NL.jpg         Nano Letters (2026)
                      Solvated electron generation from coupled plasmon modes of gold nanoparticles using visible light
  2026_ACSAMI.jpg     ACS Applied Materials & Interfaces (2026)
                      Interpretation of Photogenerated Charge Carrier Transfer Dynamics Using Interactive Surface-Molecular System
  2025_NMA.jpg        npj 2D Materials and Applications (2025)
                      Identification of phonon vibrational modes for layered Ta2Se metal-rich chalcogenide
  2025_AM.jpg         Advanced Materials (2025)
                      Anomalous phonon softening with inherent strain in wrinkled monolayer WSe2
  2025_APR.jpg        Applied Physics Reviews (2025)
                      Probing Nanoscale Structural Perturbation in WS2 monolayer via eXplainable Artificial Intelligence
  2025_ASCT.jpg       Applied Science and Convergence Technology (2025)
                      A robust approach for analyzing vibrational motions via polarizability and dipole moment
  2024_MLST.jpg       Machine Learning: Science and Technology (2024)
                      Evaluating cell growth and hypoxic regions of 3D spheroids via a machine learning approach
  2024_ASS.jpg        Applied Surface Science (2024)
                      Strain-sensitive optical properties of monolayer tungsten diselenide
  2024_ACSN.jpg       ACS Nano (2024)
                      Role of chalcogenides in sensitive therapeutic drug monitoring using laser desorption and ionization
  2024_N.jpg          Nanoscale (2024)
                      Mitigating substrate effects of van der waals semiconductors using 2-perfluoropolyether self-assembled monolayers
  2024_JPCL.jpg       J. Phys. Chem. Letters (2024)
                      Divergent vibrational property induced by anomalous layer sequence in two-dimensional GaPS4
  2024_NT.jpg         Nano Today (2024)
                      Unraveling the role of Raman modes in evaluating the degree of reduction in graphene oxide via explainable artificial intelligence
  2023_AO.jpg         Applied Optics (2023)
                      Uncertainty evaluation of photoluminescence quantum yield measurement in an integrating hemisphere-based instrument
  2023_ASS.jpg        Applied Surface Science (2023)
                      Functional group inhomogeneity in graphene oxide using correlative absorption spectroscopy
  2023_AIS.jpg        Advanced Intelligent Systems (2023)
                      Explainable artificial intelligence approach to identify the origin of phonon-assisted emission in WSe2 monolayer
  2022_JPCC.jpg       J. Phys. Chem. C (2022)
                      Identifying the origin of defect-induced Raman mode in WS2 monolayers via density functional perturbation theory

  In-preparation and submitted papers have no graphical abstract slot.
