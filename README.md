globe
=====

CTA working on code for special project

var data = [
    [
    'seriesA', [ latitude, longitude, magnitude, latitude, longitude, magnitude, ... ]
    ],
    [
    'seriesB', [ latitude, longitude, magnitude, latitude, longitude, magnitude, ... ]
    ]
];
var container = document.getElementById( 'container' );
var globe = new DAT.Globe( container );
var xhr = new XMLHttpRequest();
xhr.open( 'GET', 'myjson.json', true );
xhr.onreadystatechange = function() {
    if ( xhr.readyState === 4 && xhr.status === 200 ) {
            var data = JSON.parse( xhr.responseText )
                   for ( var i = 0; i < data.length; i ++ ) {
            globe.addData( data[i][1], 'magnitude', data[i][0] );
        }
              globe.createPoints();
                      globe.animate();

    }

};
xhr.send( null );
