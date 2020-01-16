## Introduction

The government of Montreal would like to increase the city’s commercial growth rate. Montreal is the second-most populous municipality in Canada. Montreal is about 300 miles from Toronto, and it is connected to Toronto by the St. Lawrence River and Lake Ontario. Route 401 also connects the two cities. Montreal was the commercial capital of Canada until it was surpassed by Toronto in the 1970’s.

Montreal is led by a mayor, who is “first among equals” in the Montreal city council. The city council is democratically elected. It has representative from all of Montreal’s boroughs. (Montreal , like New York and Toronto, is subdivided into Boroughs.) Much of the council’s power is centralized in the Executive Committee.

In order to increase Montreal’s growth rate, the executive committee and the council would like to use data science in order to find businesses that could be enticed to open offices in Montreal. If a neighborhood (as designated by a postal code) in Toronto is similar to a neighborhood (as designated by a postal code) in Montreal, then businesses in the Toronto neighborhood are good candidates for enticements to open up offices in Montreal. Similarly, if a neighborhood in Toronto does not have a similar neighborhood in Montreal, businesses in that neighborhood are not good candidates for inducements by Montreal.

The city council would like to start with a pilot project to assess the viability of a project that groups neighborhoods this way. The pilot project would apply the process to the neighborhoods in one borough from each city.

In Montreal, the borough with the most neighborhoods is "Ville Marie", which includes the Downtown neighborhood and several other neighborhoods. In Toronto, the “Downtown” borough includes the downtown Toronto, so the Toronto Downtown borough is a good match for the Montreal Ville Marie borough.

By finding out which neighborhoods in Ville Marie are similar to neighborhoods in Toronto, the Montreal government can target potential business to open locations in Montreal by suggesting that certain neighborhoods in Montreal are similar to certain neighborhoods in Toronto. If a business has a successful location in Toronto neighborhood, then they are more likely to succeed if they open a location in a similar neighborhood in Montreal. On the other hand, if the business wants to open an office in a new neighborhood that is different, the Montreal government will have evidence of recommending different neighborhoods.

*Note:* In the first Wikipedia article I refer to below, the borough of Ville Marie is written as “Ville Marie” and as “Ville-Marie”, with the two-word version occurring slightly more often than the hyphenated version. In Google maps, it is frequently written to as Ville-Marie. The original name of Montreal was Ville-Marie (City of Mary). In modern times, “Ville Marie” and “Ville-Marie” are interchangeable.

### Literature Review

Data for this report was drawn from several sources. Since this is not a formal literature review, I am not using standard academic bibliography conventions.

#### Text Descriptions of Montreal, Ville Marie, and Toronto

https://en.wikipedia.org/wiki/Montreal

The above page describes Montreal. It includes descriptions of the boroughs. It contains a list of the neighborhoods in the borough of Ville Marie.

https://en.wikipedia.org/wiki/Ville-Marie,_Montreal

The above page contains more information about Ville Marie. It also contains a list of the neighborhoods in the borough of Ville Marie.

http://www.vieux.montreal.qc.ca/histoire/eng/v_mara.htm

The above page has a brief history of Montreal, from it’s beginnings as Ville-Marie.

https://en.wikipedia.org/wiki/Red-Light_District,_Montreal

The above page contains a description of the Red-Light District in Montreal. I’ve included it because it is in maps of Ville Marie, but it is just a small area. It isn’t a neighborhood.

https://en.wikipedia.org/wiki/Toronto

The above page contains information about Toronto.

#### Postal Code Information

https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_H

The above page contains all of the postal codes that are used in Montreal. It also contains some descriptive information about the neighborhoods. Some of it is in French, which is the predominant language of Montreal. (Montreal is the second-largest French-speaking city in the world, right behind Paris.) The neighborhood information is complimentary to information in the Wikipedia Montreal article.

https://en.wikipedia.org/wiki/List_of_postal_codes_of_Canada:_M

The above page contains information about Toronto postal codes.

http://www.strategiclists.com/wp/wp-content/uploads/2015/07/Canada-FSAS.pdf

The above document contains maps of the areas of all of the three-characters postal code prefixes in Canada. Page 43 contains postal codes prefixes in Montreal. This could be used as an alternate source of postal code data.

#### Maps Related to Ville Marie and Maps Related to Postal Code Prefixes that Contain Land in Ville Marie

https://www.google.com/maps/place/Ville-Marie,+Montreal,+QC,+Canada/@45.5127587,-73.5961059,13z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a4d31166b3d:0xe16252d7fe06209e!8m2!3d45.5087937!4d-73.5553019

The above page contains a map that shows the boundaries of Ville Marie.

https://www.google.com/maps/place/Montreal,+QC+H2L,+Canada/@45.5196257,-73.5705852,15z/data=!3m1!4b1!4m5!3m4!1s0x4cc91bb156926d11:0xcc9a6ca5eaf5dd80!8m2!3d45.522199!4d-73.5641471

The above map shows the area contained in the H2L postal code prefix. It shows that Gay Village is in H2L. It also shows that part of the Le Plateau-Mont-Royal borough is in H2L. Since the prior analysis of Toronto was based on postal codes, I am using postal codes for this analysis even though some postal codes for Ville Marie also include neighborhoods from neighboring boroughs. One reason for doing this because Ville Marie contains Downtown Montreal, and I want to compare Downtown Montreal with Downtown Toronto.

https://www.google.com/maps/place/Montreal,+QC+H2X,+Canada/@45.5124287,-73.5844915,14z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a4b85d8bcad:0xe808bc984c0f9884!8m2!3d45.5132931!4d-73.5694014

The above map shows the area contained in the H2X postal code prefix. It shows that the Latin Quarter and Quartier Des Spectacles are in this area.

https://www.google.com/maps/place/Montreal,+QC+H2Y,+Canada/@45.5058532,-73.5643487,15z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a57232611a5:0x1bb3ff57ab036bb4!8m2!3d45.5052277!4d-73.5557318

The above map shows the area contained in the H2Y postal code prefix. Visual inspection shows that this area is entirely contained in Ville Marie.

https://www.google.com/maps/place/Montreal,+QC+H2Z,+Canada/@45.5053444,-73.5664642,16z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a5073be9d71:0x78f81b587eb5ccfe!8m2!3d45.5039113!4d-73.56321

The above map shows the area contained in the H2Z postal code prefix. Visual inspection shows that this area is entirely contained in Ville Marie.

https://www.google.com/maps/place/Montreal,+QC+H3A,+Canada/@45.5057312,-73.5851572,15z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a478d7d0b9d:0x1926a7f8491bef0!8m2!3d45.5035028!4d-73.5768503

The above map shows the area contained in the H3A postal code prefix. Careful visual inspection shows that it is contained in Ville Marie.

https://www.google.com/maps/place/Montreal,+QC+H3B,+Canada/@45.5011524,-73.5776599,15z/data=!4m5!3m4!1s0x4cc91a449d667617:0x43dba850448c97f1!8m2!3d45.4999144!4d-73.568918

The above map shows the area contained in the H3B postal code prefix. It contains a small area clearly inside of Ville Marie.

https://www.google.com/maps/place/Montreal,+QC+H3C,+Canada/@45.5023151,-73.5815692,13z/data=!3m1!4b1!4m5!3m4!1s0x4cc91af750b653c5:0x22f1d6a9e7709636!8m2!3d45.4927605!4d-73.5614161

The above map shows the area contained in the H3C postal code prefix. It contains the southeast portion of Ville Marie as well as Saint Helen's Island and Notre-Dame Island. Most of these areas are part of Ville Marie. Although this area extends beyond the boundaries of Ville Marie, most of the area in this postal code prefix is in Ville Marie.

https://www.google.com/maps/place/Montreal,+QC+H3G,+Canada/@45.4992627,-73.5897737,15z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a400aac7669:0xdfdfa1a5fddbe76f!8m2!3d45.499505!4d-73.582556

The above map shows the area contained in the H3G postal code prefix. It is contained within the Ville Marie boundaries.

https://www.google.com/maps/place/Montreal,+QC+H3H,+Canada/@45.5007627,-73.6110584,14z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a3d4cb16127:0xae3b8217ecd04d10!8m2!3d45.5026595!4d-73.5957654

The above map shows the area contained in the H3H postal code prefix. Except for part of the Notre Dame des Neiges Cemetery, all of this area is in Ville-Marie.

https://www.cimetierenotredamedesneiges.ca/en/burial-location

The above contains a map of the Notre Dame des Neiges Cemetery.

https://www.google.com/maps/place/Cit%C3%A9+du+Havre,+Montreal,+QC+H3C+3R4,+Canada/@45.4922451,-73.5611646,14z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a92b6a7ca67:0x98893b8c6ef71512!8m2!3d45.492247!4d-73.543655

The above map shows the location of Cité du Havre, and also shows that the postal code of Cité du Havre starts with H3C.

https://www.google.com/maps/place/Complexe+Le+Gleneagles/@45.4951439,-73.5965341,17z/data=!3m1!4b1!4m5!3m4!1s0x4cc91a10cd7ec55d:0x6d7594c72c8f65c5!8m2!3d45.4951439!4d-73.5943401

The above map shows the location of Îlot-Trafalgar-Gleneagles, and shows that the postal code of this location is H3H.

https://www.google.com/maps/place/Montreal,+QC+H2K,+Canada/@45.5298121,-73.5652603,15z/data=!3m1!4b1!4m5!3m4!1s0x4cc91bbe9e7b629b:0xc8cba6ffa90d0989!8m2!3d45.5301959!4d-73.5527213

The above map shows the area contained in the postal codes that starts with H3H. It shows that Sainte-Marie is in H3H.
