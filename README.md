# menu
teaching menu
<html>
<head>
   <title>University of Sheffield Teaching and Learning Approaches Menu</title>
 
  <!-- <link href="nobelists.js" type="application/json" rel="exhibit/data" />-->
 
   <script src="http://api.simile-widgets.org/exhibit/2.2.0/exhibit-api.js"
           type="text/javascript"></script>
            <script>
  var zebraStyler = function(item, database, tr) {
      if (tr.rowIndex % 2) {
          tr.style.background = '#ffb5a3';
      } else {
          tr.style.background = '#a3ffee';
      }
  }
  </script>
  <link rel="exhibit/data" 
       type="application/jsonp"
       href="https://spreadsheets.google.com/feeds/list/19xLEUp9A0SBke2voaW6HsaLjHdOS728HzB1C9RTFMFg/od6/public/basic?hl=en_US&alt=json-in-script"
       ex:converter="googleSpreadsheets" />	
      
   <style>
       body {
           margin: 1in;
		   font-family: "Arial", "Arial", "Arial", "Arial", "Arial", "sans-serif";
       }
	   table{ font: small-caps;}
       table.nobelist {
           border:     0px solid #ddd;
           padding:    0.5em;
		  
       }
       div.name {
           font-weight: bold;
           font-size:large;
       }
       .discipline {
       }
       .year {
           font-style:  italic;
       }
       .relationship {
           color:  #888;
       }
       .co-winners {
       }
   </style>
</head> 
<body>
   <h1>Teaching  and Learning Approaches</h1>
   <table width="15%">
       <tr valign="top">
           <td ex:role="viewPanel">

                  
                    <table ex:role="lens" class="nobelist" cellpadding="2">
                   <tr>
                       <td><img ex:src-content=".imageURL" /></td>
                       <td>
                           <div ex:content=".label" class="name"></div>
                           <div>
                               <span ex:content=".discipline" class="discipline"></span>
                               <!--<span ex:content=".nobel-year" class="year"></span>-->
                           </div>
                           <div ex:if-exists=".technology" class="technology"><br /><b>Enabling Technologies: </b>
                               <span ex:content=".technology"></span>
                           </div>
                           <div ex:content=".relationship-detail" class="relationship"></div>
                       </td>
                   </tr>
               </table>
               <div ex:role="exhibit-view"
                   ex:viewClass="Exhibit.TabularView" 
                   ex:columns=" .approach, .label, .definition, .benefits-approach, .activity, .technology, .benefits-technology, .examples "
                   ex:columnLabels="Type, Approach, Definition, Benefit of this Approach, Activity, Suitable Technology, Benefit of using Technology, Case Studies "
                   ex:columnFormats="list, list, list, list, list, list, list, list
                  "
                   ex:sortColumn="1"
                   ex:sortAscending="true"
                   ex:border = "1"
                   ex:cellSpacing = "0"
                   ex:cellPadding = "8"
                    ex:rowStyler="zebraStyler">
               </div>
             
               
            </td>
           <td width="25%">
               <div ex:role="facet" ex:facetClass="TextSearch"></div>
                              
               <div ex:role="facet" ex:expression=".approach" ex:facetLabel="Teaching or Learning Approach" ex:height="100%"></div>
               <div ex:role="facet" ex:expression=".label" ex:facetLabel="Approach" ex:height="100%" ex:width="100%"></div>
               <div ex:role="facet" ex:expression=".technology-filter" ex:facetLabel="Technology" ex:height="100%"></div>
         
           </td>
       </tr>
   </table>
</body>
</html>
