---

---

Explore our ongoing projects by clicking on their titles for detailed descriptions. For student (honors and post-graduate) opportunities and research collaborations, please get in touch.

<nav>
<head>
    <style>
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            padding: 8px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        th {
            cursor: pointer;
        }
    </style>
</head>
<body>

<table id="projectsTable">
    <thead>
        <tr>
            <!-- Adding onclick attributes for sorting -->
            <th onclick="sortTable(0)">Name</th>
            <th onclick="sortTable(1)">Contact</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><a href="#rationalVaccine">Rational vaccine design using computational models</a></td>
            <td><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
        </tr>
        <tr>
            <td><a href="#machineLearning">Developing a machine learning model to predict disease outcome</a></td>
            <td><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
        </tr>
    </tbody>
</table>
</nav>

<script>
function sortTable(column) {
    var table, rows, switching, i, x, y, shouldSwitch;
    table = document.getElementById("projectsTable");
    switching = true;
    /* Make a loop that will continue until
    no switching has been done: */
    while (switching) {
        // Start by saying: no switching is done:
        switching = false;
        rows = table.rows;
        /* Loop through all table rows (except the
        first, which contains table headers): */
        for (i = 1; i < (rows.length - 1); i++) {
            // Start by saying there should be no switching:
            shouldSwitch = false;
            /* Get the two elements you want to compare,
            one from current row and one from the next: */
            x = rows[i].getElementsByTagName("TD")[column];
            y = rows[i + 1].getElementsByTagName("TD")[column];
            // Check if the two rows should switch place:
            if (x.innerHTML.toLowerCase() > y.innerHTML.toLowerCase()) {
                // If so, mark as a switch and break the loop:
                shouldSwitch = true;
                break;
            }
        }
        if (shouldSwitch) {
            /* If a switch has been marked, make the switch
            and mark that a switch has been done: */
            rows[i].parentNode.insertBefore(rows[i + 1], rows[i]);
            switching = true;
        }
    }
}
</script>

</body>
</html>


<hr>

<section id="rationalVaccine">
<h3>Rational vaccine design using computational models</h3> 

<p style="font-size:14px;">The past few years has seen an abundance in sequence data for viruses such as SARS-CoV-2, HIV and HCV. This information can be exploited for the rational design of vaccines, by building models which capture the patterns in the viral sequences. These patterns can be exploited to find weaknesses in the virus, which can then be used to design effective vaccines. </p> 

<h4> Representative publications</h4>
<ol style="font-size:14px;">
<li> MS Sohail, <span style="color: red;"> R. H. Y. Louie </span>, Z Hong, JP Barton, MR McKay. Inferring epistasis from genetic time-series data. Molecular Biology and Evolution 39 (10) </li>
<li> MS. Sohail*, <span style="color: red;"> R. H. Y. Louie* </span>, J. P. Barton, and M. R. McKay, “MPL resolves genetic linkage in fitness inference from complex evolutionary histories”, Nature Biotechnology. 2021 *Equal contribution </li>
<li>  A. A. Quadeer, M. R. McKay, J.P. Barton, <span style="color: red;"> R.H.Y. Louie </span>, “MPF-BML: a standalone GUI-based package for maximum entropy model inference”, Bioinformatics, 36 (7), pp 2278-2279, April, 2020 </li>
<li> A. A. Quadeer, <span style="color: red;"> R.H.Y. Louie </span>and M. R. McKay, "Identifying immunologically-vulnerable regions of the HCV E2 glycoprotein and broadly neutralizing antibodies that target them”, Nature Communications, 10 (1), pp. 1-11, 2019 </li>
<li> <span style="color: red;"> R. H. Y. Louie </span>, K. J. Kaczorowski, J. P. Barton, A. K. Chakraborty, and M. R. McKay, “The fitness landscape of the human immunodeficiency virus envelope proteins that are the targets of humoral immune responses”, Proceedings of the National Academy of Sciences of the USA (PNAS), 115:E564-E573, Jan 2018.  </li>
<li> A. A. Quadeer, <span style="color: red;"> R.H.Y. Louie </span>, K. Shekhar, A. K. Chakraborty, I. Hsing, and M. R. McKay, “Statistical linkage of mutations in the non-structural proteins of Hepatitis C virus exposes targets for immunogen design,” Journal of Virology, vol. 88, no. 13, pp. 7628-7644, July 2014 </li>
</ol>


<h4> More information</h4>
<p style="font-size:14px;"> Honors and postgraduate opportunities are available. Please send your CV and academic transcript to <a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a>.</p> 

</section>

<hr>

<section id="machineLearning">

<h3>Developing a machine learning model to predict disease outcome</h3> 

<p style="font-size:14px;"> Accurately predicting disease outcomes can have a significant impact on patient care, leading to early detection, personalized treatment plans, and improved clinical outcomes. Machine learning algorithms provide a powerful tool to achieve this goal by identifying novel biomarkers and drug targets for various diseases. By integrating machine learning algorithms with biological data, you will have the opportunity to push the boundaries of precision medicine and contribute to algorithms that can revolutionize the field. Such biological data includes single-cell datasets, where we have considerable experience.</p> 

<h4> Representative publications</h4>

<ol style="font-size:14px;">
<li> Yanping Yang, <span style="color: red;">R. H. Y. Louie</span> et al, "Chimeric Antigen Receptor T Cell Therapy Targeting Epithelial Cell Adhesion Molecule in Gastric Cancer: Mechanisms of Tumor Resistance", Cancers, 2023. </li>
<li>  R. H. Y. Louie et al, "CAR+ and CAR− T cells share a differentiation trajectory into an NK-like subset after CD19 CAR T cell infusion in patients with B cell malignancies", Nature Communications, 2023 </li>
<li> M Gupta, H Balachandran, <span style="color: red;">R. H. Y. Louie </span>, H Li, D Agapiou, E Keoshkerian, et al, “High activation levels maintained in receptor‐binding domain–specific memory B cells in people with severe coronavirus disease” Immunology and Cell Biology 101 (2), 142-155. 2023. </li>
<li>  C Cai, J Samir, MR Pirozyan, TN Adikari, M Gupta, P Leung, B Hughes, <span style="color: red;">R. H. Y. Louie </span> et al., Identification of human progenitors of exhausted CD8+ T cells associated with elevated IFN-γ response in early phase of viral infection. Nature Communications 13 (1), 7543. 2022. </li>
<li>  Kenneth P Micklethwaite, Kavitha Gowrishankar, Brian S Gloss, Ziduo Li, Janine A Street, Leili Moezzi, Melanie A Mach, Gaurav Sutrave, Leighton E Clancy, David C Bishop, <span style="color: red;">R. H. Y. Louie </span>, Curtis Cai, Jonathan Foox, Matthew MacKay, Fritz J Sedlazeck, Piers Blombery, Christopher E Mason, Fabio Luciani, David J Gottlieb, Emily Blyth. “Investigation of product-derived lymphoma following infusion of piggyBac-modified CD19 chimeric antigen receptor T cells”, Blood, 2021 </li>
<li>  <span style="color: red;">R. H. Y. Louie </span>and F. Luciani, “Recent advances in single‐cell multimodal analysis to study immune cells”, Immunology and Cell Biology, 2021. </li>
</ol>

<h4> More information</h4>
<p style="font-size:14px;"> Honors and postgraduate opportunities are available. Please send your CV and academic transcript to  <a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a>.</p> 

</section>

