# Shootings Near Baltimore High Schools Analysis

## Overview

Fourteen juveniles in Baltimore have been shot within a block of a city high school between the hours of 7 a.m. and 7 p.m. since 2015. Twenty-seven teenagers were shot within a two block radius of a high school and most of those shootings occurred in 2022.

All but one of the shootings in the past seven years occurred near high schools in the Black butterfly, areas of the city with historical disinvestment and segregation. Shootings have been on the rise since the pandemic. 

## Methodology 

This analysis of Open Baltimore Part 1 crime victims database defines shooting victims differently than the Baltimore Police Department. The database defines shooting victims as someone who was shot but was not killed. This analysis includes both those shooting victims and homicide victims who were killed with a firearm.

This analysis spatially joins school address latitude and longitude coordinates to real property polygons in order to determine the location of school property parcels.

Thirty one high school parcels were included in this analysis, although there are more than 31 high schools in the city. In some cases, multiple high schools were located at a single parcel, causing duplicate geometries. In these situations, one unique record for the parcel was kept by distincting on the address in the real property data, and a column indicating how many high schools were located at the parcel was created by grouping and counting these duplicate addresses. 

We removed five high schools from our analysis, including virtual schools, vocational “P-Tech” schools and schools that serve juveniles that are incarcerated. 

We include incidents that occurred between 7 am and 7 pm, reasoning that students might still be at school or at after school programs during the hours between 3 and 7 pm, even when school has officially ended. We include 18 year old victims in our definition of juvenile, because some 18 year olds are still in high school. 

When counting shootings within an X number of blocks of a shapefile, we counted 100 meters for each block in addition to 50 meters for the immediate street. In some parts of the city, this may not a literal block.

## Limitations 

There are known errors in the public Part 1 Crimes Database. The database is also frequently changing. Crimes that were once classified as homicides are often reclassified, making it difficult to recreate mid-year BPD reports at the end of the year. A slight variation is to be expected.

Data on neighborhood demographic composition is from the 2020 American Community Survey, which may not necessarily be representative of current 2023 demographics. 

## License

Copyright 2023, The Venetoulis Institute for Local Journalism

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

   1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

  2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

  3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.