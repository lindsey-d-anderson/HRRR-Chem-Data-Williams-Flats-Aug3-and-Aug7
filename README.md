# HRRR-Chem Data for the Williams Flats Wildifre on August 3 and August 7

Last updated by Lindsey D. Anderson on June 29, 2025

Data files can be downloaded here and viewed using tools such as Panopoly (https://www.giss.nasa.gov/tools/panoply/) or ncview (https://cirrus.ucsd.edu/~pierce/software/ncview/quick_intro.html).

Variables are described bellow: 
* Min Latitude, Max Latitude: 47, 49
* Min Longitude, Max Longitude: -119.5, -116.5

Files named based on type of simulation, which is desribed in Anderson et al. 2025 (submitted to AGU JGR: Atmospheres):
* BaseCase: HRRR-Chem (Control) 
* hwp_v1: NO$_x$-Updated HRRR-Chem
* hwp_HalfVOC: NO$_x$-Updated HRRR-Chem Half VOC
* BaseCase_HalfVOC: HRRR-Chem Half VOC
* BaseCase_2xVOC: HRRR-Chem Twice VOC
* BaseCase_FlamFrac_55: HRRR-Chem (45% Emissions at Surface)


  dimensions:
    * Time = 1 ;
    * bottom_top = 50 ;
    * bottom_top_stag = 51 ;
    * south_north = 90 ;
    * string19 = 19 ;
    * west_east = 89 ;

  variables:
    * float HWP(Time,south_north,west_east) ;
      HWP:_FillValue = NaNf ;
      HWP:FieldType = 104 ;
      HWP:MemoryOrder = "XY " ;
      HWP:description = "hourly wildfire potential" ;
      HWP:units = "" ;
      HWP:stagger = "" ;
      HWP:coordinates = "XLAT XLONG XTIME" ;
      NOTE: HWP was presented by dividing this HWP by 10 based on the Equation S1

    * float PHOTR4(Time,bottom_top,south_north,west_east) ;
      PHOTR4:_FillValue = NaNf ;
      PHOTR4:FieldType = 104 ;
      PHOTR4:MemoryOrder = "XYZ" ;
      PHOTR4:description = "NO2 Photolysis Rate" ;
      PHOTR4:units = "min{-1}" ;
      PHOTR4:stagger = "" ;
      PHOTR4:coordinates = "XLAT XLONG XTIME" ;

    * float PM2_5_DRY(Time,bottom_top,south_north,west_east) ;
      PM2_5_DRY:_FillValue = NaNf ;
      PM2_5_DRY:FieldType = 104 ;
      PM2_5_DRY:MemoryOrder = "XYZ" ;
      PM2_5_DRY:description = "pm2.5 aerosol dry mass" ;
      PM2_5_DRY:units = "ug m^-3" ;
      PM2_5_DRY:stagger = "" ;
      PM2_5_DRY:coordinates = "XLAT XLONG XTIME" ;

    * float SCALE_FACTOR_NO(Time,south_north,west_east) ;
      SCALE_FACTOR_NO:_FillValue = NaNf ;
      SCALE_FACTOR_NO:FieldType = 104 ;
      SCALE_FACTOR_NO:MemoryOrder = "XY " ;
      SCALE_FACTOR_NO:description = "scale_factor of NO for bb emissions" ;
      SCALE_FACTOR_NO:units = "" ;
      SCALE_FACTOR_NO:stagger = "" ;
      SCALE_FACTOR_NO:coordinates = "XLAT XLONG XTIME" ;

    * float SCALE_FACTOR_NO2(Time,south_north,west_east) ;
      SCALE_FACTOR_NO2:_FillValue = NaNf ;
      SCALE_FACTOR_NO2:FieldType = 104 ;
      SCALE_FACTOR_NO2:MemoryOrder = "XY " ;
      SCALE_FACTOR_NO2:description = "scale_factor of NO2 for bb emissions" ;
      SCALE_FACTOR_NO2:units = "" ;
      SCALE_FACTOR_NO2:stagger = "" ;
      SCALE_FACTOR_NO2:coordinates = "XLAT XLONG XTIME" ;

    * char Times(Time,south_north,west_east,string19) ;
      Times:coordinates = "XLAT XLONG XTIME" ;

    * float XLAT(Time,south_north,west_east) ;
      XLAT:_FillValue = NaNf ;
      XLAT:FieldType = 104 ;
      XLAT:MemoryOrder = "XY " ;
      XLAT:description = "LATITUDE, SOUTH IS NEGATIVE" ;
      XLAT:units = "degree_north" ;
      XLAT:stagger = "" ;
      XLAT:coordinates = "XLONG XLAT" ;

    * float XLONG(Time,south_north,west_east) ;
      XLONG:_FillValue = NaNf ;
      XLONG:FieldType = 104 ;
      XLONG:MemoryOrder = "XY " ;
      XLONG:description = "LONGITUDE, WEST IS NEGATIVE" ;
      XLONG:units = "degree_east" ;
      XLONG:stagger = "" ;
      XLONG:coordinates = "XLONG XLAT" ;

    * float XTIME(Time) ;
      XTIME:_FillValue = NaNf ;
      XTIME:FieldType = 104 ;
      XTIME:MemoryOrder = "0  " ;
      XTIME:description = "minutes since 2019-08-07 00:00:00" ;
      XTIME:stagger = "" ;
      XTIME:units = "minutes since 2019-08-07" ;
      XTIME:calendar = "proleptic_gregorian" ;

    * float co(Time,bottom_top,south_north,west_east) ;
      co:_FillValue = NaNf ;
      co:FieldType = 104 ;
      co:MemoryOrder = "XYZ" ;
      co:description = "CO mixing ratio" ;
      co:units = "ppmv" ;
      co:stagger = "" ;
      co:coordinates = "XLAT XLONG XTIME" ;

    * float hcho(Time,bottom_top,south_north,west_east) ;
      hcho:_FillValue = NaNf ;
      hcho:FieldType = 104 ;
      hcho:MemoryOrder = "XYZ" ;
      hcho:description = "HCHO mixing ratio" ;
      hcho:units = "ppmv" ;
      hcho:stagger = "" ;
      hcho:coordinates = "XLAT XLONG XTIME" ;

    * double height_mid(Time,bottom_top_stag,south_north,west_east) ;
      height_mid:_FillValue = NaN ;
      height_mid:FieldType = 104 ;
      height_mid:MemoryOrder = "XYZ" ;
      height_mid:description = "perturbation geopotential" ;
      height_mid:stagger = "Z" ;
      height_mid:units = files say "m2 s-2" but the units are m ;
      height_mid:coordinates = "XLAT XLONG XTIME" ;

    * float hourly_mean_frp(Time,south_north,west_east) ;
      hourly_mean_frp:_FillValue = NaNf ;
      hourly_mean_frp:FieldType = 104 ;
      hourly_mean_frp:MemoryOrder = "XY " ;
      hourly_mean_frp:description = "mean fire radiative power" ;
      hourly_mean_frp:stagger = "" ;
      hourly_mean_frp:units = "MW" ;
      hourly_mean_frp:coordinates = "XLAT XLONG XTIME" ;

    * float no(Time,bottom_top,south_north,west_east) ;
      no:_FillValue = NaNf ;
      no:FieldType = 104 ;
      no:MemoryOrder = "XYZ" ;
      no:description = "NO mixing ratio" ;
      no:units = "ppmv" ;
      no:stagger = "" ;
      no:coordinates = "XLAT XLONG XTIME" ;

    * float no2(Time,bottom_top,south_north,west_east) ;
      no2:_FillValue = NaNf ;
      no2:FieldType = 104 ;
      no2:MemoryOrder = "XYZ" ;
      no2:description = "NO2 mixing ratio" ;
      no2:units = "ppmv" ;
      no2:stagger = "" ;
      no2:coordinates = "XLAT XLONG XTIME" ;

    * float o3(Time,bottom_top,south_north,west_east) ;
      o3:_FillValue = NaNf ;
      o3:FieldType = 104 ;
      o3:MemoryOrder = "XYZ" ;
      o3:description = "O3 mixing ratio" ;
      o3:units = "ppmv" ;
      o3:stagger = "" ;
      o3:coordinates = "XLAT XLONG XTIME" ;

    * float pan(Time,bottom_top,south_north,west_east) ;
      pan:_FillValue = NaNf ;
      pan:FieldType = 104 ;
      pan:MemoryOrder = "XYZ" ;
      pan:description = "PAN mixing ratio" ;
      pan:units = "ppmv" ;
      pan:stagger = "" ;
      pan:coordinates = "XLAT XLONG XTIME" ;
