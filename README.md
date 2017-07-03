# l2DN
t2lDN
http://www.c-sharpcorner.com/article/consuming-asp-net-web-api-rest-service-in-asp-net-mvc-using-http-client/
https://www.codeproject.com/Articles/826359/Consuming-ASP-NET-WEB-API-using-ASP-NET-MVC-and-Re
https://www.w3schools.com/howto/howto_js_filter_table.asp




@model IEnumerable<SummerCamp.Web.Models.Announcement>

@{
    ViewBag.Title = "Index";
}

<h2>Index</h2>

<table id="myTable">
    <tr>
        <th>
            Category Name
        </th>
        <th>
            Title
        </th>

        <th>
            Closed
        </th>
        
        <th>
            Id
        </th>


    </tr>

    @foreach (var item in Model)
    {
        <tr>
            <td>
                @item.CategoryName
            </td>

            <td>
                @item.Title
            </td>
            <td>
                @item.Closed
            </td>
            
            <td>
                @item.Id
            </td>
            <td>
                @Html.ActionLink("Edit", "Edit", new { id = item.Id }) |
                @Html.ActionLink("Details", "Details", new { id = item.Id }) |
                @Html.ActionLink("Delete", "Delete", new { id = item.Id })
            </td>
        </tr>
    }

    <head>
        <style>
            * {
                box-sizing: border-box;
            }

            #myInput {
                background-image: url('/css/searchicon.png');
                background-position: 10px 10px;
                background-repeat: no-repeat;
                width: 100%;
                font-size: 16px;
                padding: 12px 20px 12px 40px;
                border: 1px solid #ddd;
                margin-bottom: 12px;
            }

            #myTable {
                border-collapse: collapse;
                width: 100%;
                border: 1px solid #ddd;
                font-size: 18px;
            }

                #myTable th, #myTable td {
                    text-align: left;
                    padding: 12px;
                }

                #myTable tr {
                    border-bottom: 1px solid #ddd;
                }

                    #myTable tr.header, #myTable tr:hover {
                        background-color: #f1f1f1;
                    }
        </style>
    </head>
    <body>

        <h2>My Customers</h2>

        <input type="text" id="myInput" onkeyup="myFunction()" placeholder="Search for names.." title="Type in a name">

        

        <script>
            function myFunction() {
                var input, filter, table, tr, td, i;
                input = document.getElementById("myInput");
                filter = input.value.toUpperCase();
                table = document.getElementById("myTable");
                tr = table.getElementsByTagName("tr");
                for (i = 0; i < tr.length; i++) {
                    td = tr[i].getElementsByTagName("td")[0];
                    if (td) {
                        if (td.innerHTML.toUpperCase().indexOf(filter) > -1) {
                            tr[i].style.display = "";
                        } else {
                            tr[i].style.display = "none";
                        }
                    }
                }
            }
        </script>

    </body>

</table>
