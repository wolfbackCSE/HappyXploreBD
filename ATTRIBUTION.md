# Data sources and attribution

| Data | Source | Licence / note |
|---|---|---|
| Bangladesh boundaries (544 upazila/thana areas, simplified) | geoBoundaries gbOpen BGD ADM3 (2020), commit `9469f09` — https://www.geoboundaries.org | CC BY 4.0. Underlying data: Bangladesh Bureau of Statistics (BBS) / OCHA ROAP. The copy in `data/source/` is the original; `index.html` embeds a further-simplified version. |
| District, division, upazila lists, postcodes, Dhaka city areas | `data/source/bd-*.json`, `dhaka-city.json` (supplied by the project owner; please confirm their original source/licence before redistributing) | Used to name areas and assign each to its district. |
| District names and official websites | National Portal of Bangladesh — https://bangladesh.gov.bd/views/district-list | Checked 6 Oct 2026. |
| "Famous for" products (★ = GI) | Department of Patents, Designs and Trademarks (DPDT) registered GI list — http://dpdt.gov.bd/pages/static-pages/6922dff0933eb65569e24bcf ; Unseen Bangladesh guide — https://unseenbangladesh.com/guide/famous | Facts only; no text copied. Some GI product→district links are inferred from product names. |
| Places to visit | Unseen Bangladesh guide — https://unseenbangladesh.com/guide/ | Top places per district as listed on the index page. |
| World country shapes | Datamaps world topology (`datamaps@0.5.9` (`datamaps.all.min.js`), MIT) via jsDelivr; based on Natural Earth (public domain) | Loaded at runtime. Disputed borders follow the dataset's own depiction. |
| Libraries | jsPDF 2.5.1, d3 3.5.3, topojson 1.6.9 (cdnjs) | MIT / BSD |
| Fonts | Noto Sans Bengali, Poppins (Google Fonts) | SIL OFL |
