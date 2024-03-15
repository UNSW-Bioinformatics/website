---


---

Here are software packages developed by members of our group.

<table class = "table-responsive table-bordered">
  <tr>
  <td style = "font-weight:bold" class = "text-center">Brief Description</td>
  <td style = "font-weight:bold" class = "text-center">Contact</td>
  <td style = "font-weight:bold" class = "text-center">Description</td>
  <td colspan = "2"></td>
  </tr>
  <tr>
  <td style = "padding-left:10px;">MPF-BML</td>
  <td style = "padding-left:10px;"><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
  <td style = "padding-left:10px;padding-right:10px;">Minimum probability flow–Boltzmann Machine Learning (MPF–BML) performs fast and accurate inference of maximum entropy model parameters. This has been previously applied to viral-sequence data to design efficient vaccines.</td>
  <td style = "padding-left:5px;padding-right:5px;"><a href = "https://github.com/raymondlouie/MPF-BML" style = "color:#ce1126">Software</a></td> <td style="padding-left:5px;"><a href = "https://academic.oup.com/bioinformatics/article/36/7/2278/5680343?login=false" style = "color:#ce1126;">Journal Article</a></td>
  </tr>
  <tr>
  <td style = "padding-left:10px;">MPL</td>
  <td style = "padding-left:10px;"><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
  <td style = "padding-left:10px;padding-right:10px;">Marginal path likelihood (MPL) infers selection from evolutionary histories that resolves genetic linkage.</td>
  <td style = "padding-left:5px;padding-right:5px;"><a href = "https://github.com/raymondlouie/WF-MPL" style = "color:#ce1126">Software</a></td> <td style="padding-left:5px;"><a href = "https://www.nature.com/articles/s41587-020-0737-3" style = "color:#ce1126;">Journal Article</a></td>
  </tr>

  <tr>
  <td style = "padding-left:10px;">EGAD</td>
  <td style = "padding-left:10px;"><a href="mailto:">Sara Ballouz</a></td>
  <td style = "padding-left:10px;padding-right:10px;">EGAD: ultra-fast functional analysis of gene networks</td>
  <td style = "padding-left:5px;padding-right:5px;"><a href = "https://bioconductor.org/packages/release/bioc/html/EGAD.html" style = "color:#ce1126">Software</a></td> <td style="padding-left:5px;"><a href = "https://academic.oup.com/bioinformatics/article/33/4/612/2664343" style = "color:#ce1126;">Journal Article</a></td>
  </tr>

</table>

<head>
    <title>Sortable Table with Arrows</title>
    <style>
        th {
            cursor: pointer;
            position: relative;
        }
        th:hover::after {
            content: ' ⇅'; /* Default arrow indicating sortable */
        }
        .ascending::after {
            content: ' ↑'; /* Arrow for ascending sort */
        }
        .descending::after {
            content: ' ↓'; /* Arrow for descending sort */
        }
        th, td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        tr:hover {
            background-color: #f5f5f5;
        }
    </style>
</head>
<body>

<h2>Sortable Table with Arrows</h2>
<p>Click on the headers to sort the table.</p>

<table id="sortableTable">
    <thead>
        <tr>
            <th onclick="sortTable(0, this)">Name</th>
            <th onclick="sortTable(1, this)">Age</th>
            <th onclick="sortTable(2, this)">Country</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>John Doe</td>
            <td>35</td>
            <td>USA</td>
        </tr>
        <tr>
            <td>Jane Smith</td>
            <td>25</td>
            <td>UK</td>
        </tr>
        <tr>
            <td>Emma Jones</td>
            <td>30</td>
            <td>Canada</td>
        </tr>
    </tbody>
</table>

<script>
function sortTable(column, thElement) {
    var table, rows, switching, i, x, y, shouldSwitch, dir = "asc", switchcount = 0;
    table = document.getElementById("sortableTable");
    switching = true;
    // Remove arrow from all headers
    var allHeaders = table.getElementsByTagName("TH");
    for (i = 0; i < allHeaders.length; i++) {
        allHeaders[i].classList.remove("ascending", "descending");
    }
    /* Make a loop that will continue until
    no switching has been done: */
    while (switching) {
        switching = false;
        rows = table.rows;
        for (i = 1; i < (rows.length - 1); i++) {
            shouldSwitch = false;
            x = rows[i].getElementsByTagName("TD")[column];
            y = rows[i + 1].getElementsByTagName("TD")[column];
            if (dir == "asc") {
                if (x.innerHTML.toLowerCase() > y.innerHTML.toLowerCase()) {
                    shouldSwitch = true;
                    break;
                }
            } else if (dir == "desc") {
                if (x.innerHTML.toLowerCase() < y.innerHTML.toLowerCase()) {
                    shouldSwitch = true;
                    break;
                }
            }
        }
        if (shouldSwitch) {
            rows[i].parentNode.insertBefore(rows[i + 1], rows[i]);
            switching = true;
            switchcount++;
        } else {
            if (switchcount == 0 && dir == "asc") {
                dir = "desc";
                switching = true;
            }
        }
    }
    if (dir == "asc") {
        thElement.classList.add("ascending");
    } else {
        thElement.classList.add("descending");
    }
}
</script>

</body>