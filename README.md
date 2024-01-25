# List of all countries and flags (JSON)

## Structure of packages in the project

```bash

countries
    |--demo
    |   |--css
    |   |   |--bootstrap.min.css
    |   |--flags
    |   |--countries.json
    |   |--index.html
    |--flags
    |--countries.grouped.continent.json
    |--countries.grouped.continent.min.json
    |--countries.json
    |--countries.min.json
countries

```

## Use this packege
### Example with ajax
```jquery
$(document).ready(function () {
            $.ajax({
                type: "Get",
                url: "countries.json",
                dataType: "json",
                success: function (data) {
                    $.each(data, function (index, country) {
                        $('#countries tbody').append('<tr>' +
                            '<td><img src="' + country['flag'] + '" height="20" width="30"></td>' +
                            '<td>' + country['nameEn'] + '</td>' +
                            '<td>' + country['nameFr'] + '</td>' +
                            '<td>' + country['nameAr'] + '</td>' +
                            '<td>' + country['code'].alpha_2 + '</td>' +
                            '<td>' + country['code'].alpha_3 + '</td>' +
                            '<td>' + country['code'].un + '</td>' +
                            '<td>' + country['telephoneCode'] + '</td>' +
                            '<td>' + country['continent'] + '</td>' +
                            '</tr>'
                        );
                    });
                },
                error: function () {
                    alert("Error: json file not found !");
                }
            });
        });

```

