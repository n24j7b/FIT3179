java c
FIT3179 Data Visualisation 
Week 9   Homework: Create a   Map with Vega-Lite 
Introduction 
This is an assessed homework and is   worth   1%   of   your ﬁnal   mark. The goal of   this homework is to create a map with Vega-Lite that is   useful for your   Data Visualisation 2 assignment. You will get feedback about your map on   Moodle and in the Week 10 studio, and you can later include   an   improved version   of   your map in your submission for the Data Visualisation 2 assignment.
Task 
The task is to create a map that is relevant for your Visualisation 2 domain.
Search a dataset that you want to visualise.   The dataset does not need to include   longitude/latitude information; you can link your data with existing geoshape information that you download from naturalearthdata.org or another data   source. Select a map idiom that is well suited for your dataset and makes sense   in the      context of   your Visualisation 2 project. In the unusual case that creating a   map   does not make sense for your domain and your tutor has given you an exemption from including a map in the Visualisation 2 assignment, you are still   required to create a map for this homework. You may choose any topic in this    case.
Submission 
A report is to be submitted in   PDF format through the submission   link   on the   Week 9   Moodle page. The page limit of   the   report   content   is two   pages. Write a   report with the following content:
● Your name,   Monash student   ID,   lab, tutor   name
● A   URL of   your publicly accessible web page on   GitHub that   embeds the
map that you created.   Note that a link to the   JSON deﬁnition of   the map is   not accepted; a   URL of a   HTML web page is   required   instead.   Refer to the Week 4 (section 4) and Week 7 (section   1.3) studio materials for publishing   a Vega-Lite visualisation with a GitHub page.
● A screen capture of   your   map.
● One short bullet point for   each   of   the following   items:
o   The domain of   your visualisation
o   The visualised dataset (attribute types, source and author, etc.)
o   Data transformation that you applied (if any), such as normalisation   by area or   population.
o   Ajustiﬁcation for the type of map idiom used.   For example, explain   why you chose to create a proportional   symbol map instead   of a choropleth map or a   dot   map.
Hints for Creating an Outstanding Map 
●            Your dataset should not be too   large. While   it   is technically   possible to   load datasets of multiple megabytes, large datasets   must   be avoided   if possible, because your ﬁnal visualisation will load slowly. To reduce the   size of   your dataset, you may
o      remove attributes that are not needed,
o      remove geometry that is not shown on your map   by clipping the   geometry (see the week 8 studio exercise ),
o      simplify detailed geometry with mapshaper.
●            Your map shoul include a graticule, that is,   lines of constant   longitude and   latitude. The naturalearthdata.com site provides shapeﬁles with graticules   at diﬀerent resolutions. The maps below   include a graticule with a 30-degree resolution.
● Consider including additional map layers   if useful   and   relevant for your map.   For example,you may want to include lakes and   rivers,   major   roads, major cities, etc. Naturalearthdata.com is the best   resource for   map   layers   that show the entire world or large sections of   Earth. 
●          Including a shaded relief image for showing terrain or   including satellite   images or other raster imagery wou代 写FIT3179 Data Visualisation
代做程序编程语言ld   be great but   is   not trivial with Vega-Lite, so this   is optional.
● It is tempting to   include very detailed geometry in   maps.   However,   it   is often better to use simpler geometry (also known as “generalised” geometry), as details are distracting and add a lot   of noise   and visual clutter. The ﬁ   rst map below uses data for a   scale   of   1:10   million. This   is too   detailed for this map scale.   The second map uses data for a scale   of   1:110      million. The outlines of continents are much less   noisy and visually pleasing to look at. If   your geometry data is too detailed,   use   mapshaper   to simplify   it. 

●          Use ﬁgure-ground: select bright and desaturated colours for larger areas   and elements that are the ground of   your map. For example, in the second map above, the continents and the oceans are shown with bright   colours, and all lines (including outlines of continents) are   bright grey or blue.   In the second map, only the small dots indicating   major   cities   use pure   black. 
● http://colorbrewer.org is an essential tool for selecting   colours for   maps.
● Select map projections   judicially. Start with the “equirectangular” projection, then use https://projectionwizard.org for selecting an optimum   projection when mapping only parts of   the   world.   Modify your projection            in   Vega-Lite: 
https://vega.github.io/vega-lite/docs/projection.html#projection-types 
Note that TopoJSON can only contain longitude/latitude coordinates.
Mapshaper.org can convert from various Cartesian coordinate systems to spherical longitude and latitude coordinates in case your geometry   is   not   in longitude/latitude coordinates. 
●       You can   use   map   idioms that   require   additional tools to   build   besides   Vega-Lite, such as bin   maps   or   dot   maps.
Marking Rubric 
0 points when the URL is not   included,   does   not work,   or   does   not   link to a   Vega-Lite   map embedded in a   HTML document.   Minus 20% for each   of   the   following   issues:
●       Data is not normalised for a   map   idiom that   requires   normalised data   (e.g.   choropleth).
●         An inappropriate map projection is   used,   especially when   a world   map projection is used for a regional map. The   projection   parameters are   not   appropriate (hint: use https://projectionwizard.org)
●         The map contains too much   empty white space (as   in the example   below),   or the area shown is zoomed out (e.g., a map showing the   entire world when the topic is for Australia only).

●         An inappropriate map idiom is   used (for   example, a   choropleth   map for   absolute values).
●         The map does not contain a graticule, an ocean   background   (for   a world   map), countries, states, or other reference layer. An   example   is shown below:

● Data absence creates holes inchoropleth maps, as   in the example   below. 

● A legend is essential to   understanding,   but   it   is   lacking.
●         The colour channel is wrong for the mapped data, for example, a   diverging colour scale is used for   a   sequential attribute. 
●       Map symbols coalesce such that information is   not   readable, or too   many   diﬀerent colours are used, as in the   example   below. 

● Legends, titles and tooltips use attribute names, such as “pop_sqkm”   .
● The mapped information topic   or units   are   not   indicated.
● Poor map title (a good title may contain the topic, the area, and a time).



         
加QQ：99515681  WX：codinghelp
