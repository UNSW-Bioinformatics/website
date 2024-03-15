---


---

Here are software packages developed by members of our group.


<head>
    <title>Sortable Table with Permanent White Arrows</title>
    <style>
        .table-responsive {
            width: 100%;
            margin-bottom: 15px;
            overflow-y: hidden;
            overflow-x: auto;
            border: 1px solid #ddd;
            -webkit-overflow-scrolling: touch;
            -ms-overflow-style: -ms-autohiding-scrollbar;
            border-collapse: collapse;
        }
        .table-bordered th, .table-bordered td {
            border: 1px solid #ddd !important;
        }
        th {
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
            position: relative;
        }
        .arrow {
            color: white;
            position: absolute;
            right: 5px;
            top: 50%;
            transform: translateY(-50%);
        }
        .arrow::before {
            content: '▼';
        }
        .arrow::after {
            content: '▲';
            position: absolute;
            right: 0;
            top: -100%;
        }
        th, td {
            text-align: left;
            padding: 8px;
        }
        tr:nth-child(even) {background-color: #f2f2f2;}
    </style>
</head>
<body>

<table class="table-responsive table-bordered">
    <thead>
        <tr>
            <th class="text-center">Brief Description <span class="arrow"></span></th>
            <th class="text-center">Contact <span class="arrow"></span></th>
            <th class="text-center">Description <span class="arrow"></span></th>
            <th colspan="2" class="text-center">Links</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="padding-left:10px;">MPF-BML</td>
            <td style="padding-left:10px;"><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
            <td style="padding-left:10px;padding-right:10px;">Minimum probability flow–Boltzmann Machine Learning (MPF–BML) performs fast and accurate inference of maximum entropy model parameters. This has been previously applied to viral-sequence data to design efficient vaccines.</td>
            <td style="padding-left:5px;padding-right:5px;"><a href="https://github.com/raymondlouie/MPF-BML" style="color:#ce1126">Software</a></td>
            <td style="padding-left:5px;"><a href="https://academic.oup.com/bioinformatics/article/36/7/2278/5680343?login=false" style="color:#ce1126;">Journal Article</a></td>
        </tr>
        <tr>
            <td style="padding-left:10px;">MPL</td>
            <td style="padding-left:10px;"><a href="mailto:r.louie@unsw.edu.au">Raymond Louie</a></td>
            <td style="padding-left:10px;padding-right:10px;">Marginal path likelihood (MPL) infers selection from evolutionary histories that resolves genetic linkage.</td>
            <td style="padding-left:5px;padding-right:5px;"><a href="https://github.com/raymondlouie/WF-MPL" style="color:#ce1126">Software</a></td>
            <td style="padding-left:5px;"><a href="https://www.nature.com/articles/s41587-020-0737-3" style="color:#ce1126;">Journal Article</a></td>
        </tr>
        <tr>
            <td style="padding-left:10px;">EGAD</td>
            <td style="padding-left:10px;"><a href="mailto:">Sara Ballouz</a></td>
            <td style="padding-left:10px;padding-right:10px;">EGAD: ultra-fast functional analysis of gene networks</td>
            <td style="padding-left:5px;padding-right:5px;"><a href="https://bioconductor.org/packages/release/bioc/html/EGAD.html" style="color:#ce1126">Software</a></td>
            <td style="padding-left:5px;"><a href="https://academic.oup.com/bioinformatics/article/33/4/612/2664343" style="color:#ce1126;">Journal Article</a></td>
        </tr>
    </tbody>
</table>

<script>
// JavaScript code for sorting will go here
</script>

</body>

