---


---

Here are software packages developed by members of our group.



<head>
    <title>Sortable Table with Arrows</title>
    <style>
        .sortable th {
            cursor: pointer;
            position: relative;
            padding-right: 25px; /* Make space for the arrow */
        }
        .sortable .arrow {
            position: absolute;
            right: 5px;
            top: 50%;
            transform: translateY(-50%);
        }
        .asc::after {
            content: '▲';
        }
        .desc::after {
            content: '▼';
        }
        .table-responsive, .table-bordered {
            border: 1px solid #ddd;
            width: 100%;
            border-collapse: collapse;
        }
        .table-responsive td, .table-bordered td {
            border: 1px solid #ddd;
            padding: 8px;
        }
        .text-center {
            text-align: center;
        }
    </style>
</head>
<body>

<table class="table-responsive table-bordered sortable">
  <thead>
    <tr>
      <th class="text-center" onclick="sortTable(0)">Brief Description <span class="arrow"></span></th>
      <th class="text-center" onclick="sortTable(1)">Contact <span class="arrow"></span></th>
      <th class="text-center" onclick="sortTable(2)">Description <span class="arrow"></span></th>
      <th colspan="2" class="text-center">Links</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>MPF-BML</td>
      <td><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
      <td>Minimum probability flow–Boltzmann Machine Learning (MPF–BML) performs fast and accurate inference of maximum entropy model parameters. This has been previously applied to viral-sequence data to design efficient vaccines.</td>
      <td><a href="https://github.com/raymondlouie/MPF-BML" style="color:#ce1126">Software</a></td>
      <td><a href="https://academic.oup.com/bioinformatics/article/36/7/2278/5680343?login=false" style="color:#ce1126;">Journal Article</a></td>
    </tr>
    <tr>
      <td>MPL</td>
      <td><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
      <td>Marginal path likelihood (MPL) infers selection from evolutionary histories that resolves genetic linkage.</td>
      <td><a href="https://github.com/raymondlouie/WF-MPL" style="color:#ce1126">Software</a></td>
      <td><a href="https://www.nature.com/articles/s41587-020-0737-3" style="color:#ce1126;">Journal Article</a></td>
    </tr>
    <tr>
      <td>EGAD</td>
      <td><a href="mailto:">Sara Ballouz</a></td>
      <td>EGAD: ultra-fast functional analysis of gene networks</td>
      <td><a href="https://bioconductor.org/packages/release/bioc/html/EGAD.html" style="color:#ce1126">Software</a></td>
      <td><a href="https://academic.oup.com/bioinformatics/article/33/4/612/2664343" style="color:#ce1126;">Journal Article</a></td>
    </tr>
  </tbody>
</table>

<script>
function sortTable(column) {
    var table, rows, switching, i, x, y, shouldSwitch, dir = "asc", switchcount = 0;
    table = document.querySelector(".sortable");
    switching = true;
    while (switching) {
        switching = false;
        rows = table.getElementsByTagName("TR");
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
    // Update arrows
    var allHeaders = table.querySelectorAll("th");
    allHeaders.forEach(function(header) {
        header.querySelectorAll(".arrow").forEach(function(arrow) {
            arrow.className = "arrow"; // Reset
        });
    });
    var currentArrow = allHeaders[column].querySelector(".arrow");
    if (dir === "asc") {
        currentArrow.classList.add("asc");
    } else {
        currentArrow.classList.add("desc");
    }
}
</script>

</body>

