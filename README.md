# List of all countries and flags (JSON)

    -**Could use this package for get 'Telephone code'.**
    -**Or for getting important informations about any country.**
    -**...**

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

## Example with ajax
```js

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

## See the result after fetching json file with ajax

<div align="center">
    <img src="demo/img/result.png" with="100%">
</div>

#### Happy conding
