# filter
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <center>
        <input type="text" id="search"><button onclick="btnfunc()">Search</button>
        <span id="msg"></span>
    </center>
</body>
<script>var employee = [{ name: "ankit", rollno: 1254, country: "india" },
    { name: "aman", rollno: 1254544, country: "us" },
    { name: "anand", rollno: 125754, country: "canada" },
    { name: "arun", rollno: 164254, country: "india" },
    { name: "ankit", rollno: 1254, country: "canada" },
    { name: "ankit", rollno: 1254, country: "us" },
    { name: "ankit", rollno: 1254, country: "india" },
    { name: "aman", rollno: 1254544, country: "us" },
    { name: "anand", rollno: 125754, country: "canada" },
    { name: "arun", rollno: 164254, country: "india" },
    { name: "ankit", rollno: 1254, country: "canada" },
    { name: "ankit", rollno: 1254, country: "us" }
    ]
    function btnfunc() {
        let tbl = `<table border='1' width='600' <tr><th>NAME</th><th>ROLLNO</th><th>COUNTRY</th></tr>`
        let searchValue = document.getElementById("search").value
        let filterdata = employee.filter(function (getvalue) {
            if (searchValue == getvalue.name)
                return getvalue.name == searchValue
            if (searchValue == getvalue.country)
                return getvalue.country == searchValue
            if (searchValue == getvalue.rollno)
                return getvalue.rollno == searchValue
        })
        filterdata.forEach(function (x) {
            tbl += `<tr><th>${x.name}</th><th>${x.rollno}</th><th>${x.country}</th></tr>`


        });
        document.getElementById("msg").innerHTML = tbl


    }
</script>

</html>[filter.zip](https://github.com/AnkitMehraV/filter/files/8130020/filter.zip)
