// scrape_politico.js

var webPage = require('webpage');
var page = webPage.create();

var fs = require('fs');
var path = ‘pa_county_potus_res.html'

page.open('http://www.politico.com/2016-election/results/map/president/pennsylvania/', function (status) {
  var content = page.content;
  fs.write(path,content,'w')
  phantom.exit();
});