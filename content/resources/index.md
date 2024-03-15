---


---

Here are software packages developed by members of our group.

<head>
    <title>Sortable Table with Permanent Arrows</title>
    <style>
        .table-responsive {
            width: 100%;
            margin: 0 auto;
        }
        .table-bordered, .table-bordered td, .table-bordered th {
            border: 1px solid #ddd;
        }
        td, th {
            padding: 8px;
            text-align: left;
        }
        th {
            color: white;
            cursor: pointer;
        }
        th .arrow {
            color: white;
            font-size: 12px;
            margin-left: 5px;
        }
        .text-center {
            text-align: center;
        }
    </style>
</head>
<body>

<table class="table-responsive table-bordered">
    <tr>
        <th class="text-center">Brief Description <span class="arrow">&#9660;</span></th>
        <th class="text-center">Contact <span class="arrow">&#9660;</span></th>
        <th class="text-center">Description <span class="arrow">&#9660;</span></th>
        <th colspan="2"></th>
    </tr>
    <!-- Table rows go here -->
</table>

<script>
// JavaScript for sorting the table
function sortTable(n) {
    var table, rows, switching, i, x, y, shouldSwitch, dir, switchcount = 0;
    table = document.querySelector(".table-responsive");
    switching = true;
    // Set the sorting direction to ascending:
    dir = "asc";
    while (switching) {
        switching = false;
        rows = table.rows;
        for (i = 1; i < (rows.length - 1); i++) {
            shouldSwitch = false;
            x = rows[i].getElementsByTagName("TD")[n];
            y = rows[i + 1].getElementsByTagName("TD")[n];
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
            } else if (switchcount == 0 && dir == "desc") {
                dir = "asc";
                switching = true;
            }
        }
    }
    // Update arrows based on the current sorting direction
    var arrows = table.querySelectorAll('.arrow');
    arrows.forEach(function(arrow) {
        arrow.innerHTML = dir == "asc" ? "&#9650;" : "&#9660;";
    });
}

// Attach the sort function to each header
document.querySelectorAll('.table-responsive th').forEach(function(header, index) {
    if (index < 3) { // Assuming the first three headers are sortable
        header.addEventListener('click', function() {
            sortTable(index);
        });
    }
});
</script>

</body>

