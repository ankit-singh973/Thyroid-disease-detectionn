<!DOCTYPE html>
<html lang="en">
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,700" rel="stylesheet">
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/all.css" integrity="sha384-B4dIYHKNBt8Bc12p+WXckhzcICo0wtJAoU8YZTY5qE0Id1GSseTk6S+L3BlXeVIU" crossorigin="anonymous">


<head>

    <title>Thyroid Detection </title>

</head>



<style>
        body {
            background-color:rgb(541, 129, 123);
            color: rgb(10, 5, 5);
            text-align: center;
            padding-right: 90px;
            font-family:Roboto;
            font-size: 20px;


        }
        .banner {
        position:relative;
        height: 380px;
        background-image: url("https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQoGu43I5JdP_y2YTXS_QobRhRPeymZSjnqDA&usqp=CAU");      background-size: cover;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        }

</style>

<body>
    <div class="banner">
    </div>

<h1 style="font-size: 26; text-align: center; font-weight: bold;margin-top: 5%"><u>Thyroid Detection</u></h1>
<br>


    <!-- Inputs to our model-->
<form action="{{ url_for('predict')}} " method="post">
        <label for="age">Age</label><br>
            <input type="number" class="form-control" name="age" id="age" min="1" max="100" placeholder="(1, 100)" step="any" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%"  required><br>

            <label for="sex">Sex</label><br>
            <input type="number" class="form-control" name="sex" id="sex" min="0" max="1" placeholder="Male - 1, Female - 0" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>

             <label for="on_thyroxine">On Thyroxine</label><br>
            <input type="number" class="form-control" name="onthyroxine" id="on_thyroxine" min="0" max="1" placeholder="(0, 1)" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>

            <label for="sick">Sick</label><br>
            <input type="number" class="form-control" name="sick" id="sick" min="0" max="1" placeholder="Yes - 1, No - 0" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>

            <label for="query_hypothyroid">Query Hypothyroid</label><br>
            <input type="number" class="form-control" name="queryhypothyroid" id="query_hypothyroid" min="0" max="1" placeholder="Yes - 1, No - 0" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>

            <label for="psych">Psychological Symptoms</label><br>
            <input type="number" class="form-control" name="psych" id="psych" min="0" max="1" placeholder="Yes - 1, No - 0" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>

            <label for="t3">T3 Level</label><br>
            <input type="number" class="form-control" name="T3" id="t3" min="0.05" max="10.6" placeholder="(0.05, 10.6)" step="any" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>

            <label for="tt4">TT4 Level</label><br>
            <input type="number" class="form-control" name="TT4" id="tt4" min="0.31" max="2.12" placeholder="(0.31, 2.12)" step="any" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>

            <label for="fti">Free Thyroxine Index (FTI)</label><br>
            <input type="number" class="form-control" name="FTI" id="fti" min="2.0" max="395.0" placeholder="(2.0, 395.0)" step="any" style="font-size: 14pt; height: 20px; width:200px;margin-bottom:1%" required><br>




    <button type="submit" class="btn btn-primary btn-block btn-large" style="padding: 10px 15px" >Predict</button>
    <h3><mark>{{ prediction_text }}</mark></h3>
    <br><br>

</form> <br><br><br><br>



</div>



    </body>
</html>
