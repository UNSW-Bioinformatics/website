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
        .sortable .arrow.asc, .sortable .arrow.desc {
            position: absolute;
            right: 5px;
            top: 50%;
            color: black; /* Changed to black for visibility */
            transform: translateY(-50%);
        }
        .sortable .arrow.desc {
            display: none; /* Hide descending arrow by default */
        }
        .sortable th.asc .arrow.desc, .sortable th.desc .arrow.asc {
            display: none; /* Hide the non-active arrow */
        }
        .sortable th.asc .arrow.asc, .sortable th.desc .arrow.desc {
            display: inline; /* Show the active arrow */
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
      <th class="text-center" onclick="sortTable(0)">Brief Description <span class="arrow asc">▲</span><span class="arrow desc">▼</span></th>
      <th class="text-center" onclick="sortTable(1)">Contact <span class="arrow asc">▲</span><span class="arrow desc">▼</span></th>
      <th class="text-center" onclick="sortTable(2)">Description <span class="arrow asc">▲</span><span class="arrow desc">▼</span></th>
      <th colspan="2" class="text-center">Links</th>
    </tr>
  </thead>
  <tbody>
    <!-- Table body remains unchanged -->
  </tbody>
</table>

<script>
// JavaScript remains unchanged
</script>

</body>
