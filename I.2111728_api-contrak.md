## Matakuliah
<details>
<summary> Klik untuk Ekspan </summary>

### Create Matakuliah
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matakuliah </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama matkul" : "Bahasa Pemograman 2",
    "Dosen" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
    "jumlah sks" : "3"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Matakuliah Berhasil diinput",
    "data" : {
        "kodemk" : 001,
        "nama matkul" : "Bahasa Pemograman 2",
        "Dosen" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
        "Jumlah sks" : "3"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Matakuliah Telah digunakan",
    "data" : {
        "value" : "Bahasa Pemograman 2",
        "property" : "nama matkul",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Matakuliah By kodemk
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matakuliah </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/matakuliah?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "kodemk" : 001,
        "nama matkul" : "Bahasa Pemograman 2",
        "Dosen" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
        "jumlah sks" : "3"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Matakuliah tidak ditemukan",
    "data" : {
        "value" : Bahasa Pemograman 2,
        "property" : "nama matkul",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Matakuliah All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matakuliah </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "kodemk" : 001,
            "nama matkul" : "Bahasa Pemograman 2",
            "Dosen" : "MA’SHUM ABDUL JABBAR, S.KOM, M.T.I.",
            "Jumlah sks" : "3"
        }
        {
            "kodemk" : 002,
            "nama matkul" : "Basis Data 2",
            "Dosen" : "UUS FIRDAUS, S.KOM, M.T.I.",
            "Jumlah sks" : "3"
        }

        {
            "kodemk" : 003,
            "nama matkul" : "Aljabar Linear",
            "Dosen" : "HILMY ALIY ANDRA PUTRA, S.SI, M.SI.",
            "Jumlah sks" : "3"
        }

        {
            "kodemk" : 004,
            "nama matkul" : "Jaringan Komputer",
            "Dosen" : "AZHARUDIN, S.KOM, M.PD.",
            "Jumlah sks" : "4"
        }

        {
            "kodemk" : 005,
            "nama matkul" : "Pendidikan Kampus Bertauhid",
            "Dosen" : "ARIF IRAWAN, S.AG., M.A",
            "Jumlah sks" : "4"
        }

        {
            "kodemk" : 006,
            "nama matkul" : "Bahasa Inggris",
            "Dosen" : "NURUL ANNISA YUNIARTI, S.PD., M.PD.",
            "Jumlah sks" : "3"
        }
    ]
}    
```


</td>
</tr>
</table>

### Update Matakuliah
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matakuliah </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
            "kodemk" : 002,
            "nama matkul" : "Basis Data 2",
            "Dosen" : "UUS FIRDAUS, S.KOM, M.T.I.",
            "Jumlah sks" : "3"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Matakuliah Berhasil diubah",
    "data" : {
            "kodemk" : 002,
            "nama matkul" : "Basis Data 2",
            "Dosen" : "UUS FIRDAUS, S.KOM, M.T.I.",
            "Jumlah sks" : "3"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Matakuliah Telah digunakan",
    "data" : {
        "value" : "Basis Data 2",
        "property" : "nama matkul",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Matakuliah tidak ditemukan",
    "data" : {
        "value" : 002,
        "property" : "kodemk",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Matakuliah
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/matakuliah </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/matakuliah?id=1234 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=1234 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : [] 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Matakuliah tidak ditemukan",
    "data" : {
        "value" : 002,
        "property" : "kodemk",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>

