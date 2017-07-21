<html>
<head>
    <script src="https://code.jquery.com/jquery-1.9.1.min.js"></script>
    <script src="http://davidbau.com/encode/seedrandom.js"></script>
    <script>
    function query_random(query,Total,times){
        Math.seedrandom(query);
        var seed = [];
        //var Total = 10,times = 3000;
        for (var i=0;i<Total;i++)
            seed[i] = Math.random()*times;
            //seed[i] = Math.round(Math.random()*times).toFixed(2);
        //console.log(seed);
        return seed;
    }
    function softmax(arr) {
        return arr.map(function(value,index) { 
          return Math.exp(value) / arr.map( function(y /*value*/){ return Math.exp(y) } ).reduce( function(a,b){ return a+b })
        })
    }
    function round_array(arr,after){
       for (var i=0;i<arr.length;i++)
           arr[i] = arr[i].toFixed(after);
       return arr;
    }
    function generator(query){
        country_data = query_random(query,10,3000);
        S_age_data = softmax(query_random(query,4,10));
        //
        country_data = round_array(country_data,0);
        S_age_data = round_array(S_age_data,4);
        //console.log(country_data);
        //console.log(S_age_data);
        return [country_data,S_age_data];
    }
    $( document ).ready(function() {
        console.log( "document loaded" );

        var data = [],data2 = [];
        data = generator("pneumonia");
        data2 = generator("AIDS");
        console.log(data);
        console.log(data2);
        //pneumonia
        
        /*query_random("Mycetoma");
        query_random("pemphigus vegetans");
        query_random("Tapetoretinal Degeneration with Ataxia");*/
    });
 
    /*$( window ).on( "load", function() {
        console.log( "window loaded" );
    });*/
    </script>
</head>
<body>
    HEY
    <!--<iframe src="http://techcrunch.com"></iframe>-->
</body>
</html>
