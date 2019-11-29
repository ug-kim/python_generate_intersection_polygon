# python_generate_polygon
Generate polygon using python shapely, geopandas, and rtree.
<br>
## This is generating intersection polygon between geojson file and specific lon/lat size box.

## Requirements
+ Python < 3.8
+ GeoPandas
  + When you install geopandas, you may be better making new virtual environment like that
    + conda create --name Test python=3.7 geopandas --yes
+ shapely
+ matplotlib (for showing the test result)
+ time (for showing time the function took, optional)
<br>
## Explanation
<br>
### First example
When I try to use shapely module intersection function, it has some problems. This function was not woking at specific images, but I cannot find which image is not working. I think it just this functions's bugs.
So I try to change the method to get intersection area of polygon and box.
<br>
### Second example
I try to use geopandas overlay(how="intersection"). It works well to all images, but there is small problems. This fuction takes time too much so when I try to get a lot of images, it is not efficient. So I try to use index like rtree for improving speed.
<img width="737" alt="스크린샷 2019-11-29 오전 10 11 55" src="https://user-images.githubusercontent.com/38632805/69837156-ce108080-1290-11ea-95b1-9adcc273035c.png">
<br>
### Thrid example
I try to use geopandas sjoin(spatial join which use rtree index maybe). It works well to all image, and speed is also faster than before. So I use this function to my project.
<img width="733" alt="스크린샷 2019-11-29 오전 10 12 13" src="https://user-images.githubusercontent.com/38632805/69837166-d8cb1580-1290-11ea-8bfa-4816a8f448f0.png">
