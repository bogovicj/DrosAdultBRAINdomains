Drosophila Adult Brain Template and Domains
=====================

This is the location of the main brain template created from JFRCtemplate2010 with labeled domains from the mask dated 19/08/13.

Recommended files
-----------------
| Kind | File | voxel size | dims |
|------|------|------------|------|
| nc82 template | [JFRCtemplate2010.nrrd](../master/template/JFRCtemplate2010.nrrd) | 0.622088 µm isotropic | 1024 x 512 x 218 |
| Label Field | [JFRCtempate2010.mask130819_Original.nrrd](../master/template/JFRCtempate2010.mask130819_Original.nrrd) | uncalibrated | 1024 x 512 x 218 |

[nrrd format](teem.sourceforge.net/nrrd) images can be opened in [Fiji](http://fiji.sc/)/[ImageJ](http://imagej.nih.gov/ij/), [Amira](http://www.vsg3d.com/amira)
(with [plugin](https://github.com/jefferis/hxNrrdIO)) and many 
[medical imaging software packages](http://www.nitrc.org/search/?type_of_search=group&offset=0&removeterm=&cat=511%3ANrrd&compare=&term%5B%5D=nrrd). 

Source Data
-----------
The source images for the template and mask files were:

| file | md5 | voxel size | dims | 
|------|-----|------------|------|
| JFRCtemplate.tif | 6e7f4e54cd630d389784132c7108a284 | 1 x 1 x 1 | 3 x 1024 x 512 x 218|
| JFRCtempate2010.mask130819.am | d0a40b38d1a0045a423d947ebf1778d2 | 1 x 1 x 1.47 | 1024 x 512 x 218 |

### Template data
JFRCtemplate.tif was generated by Arnim Jenett and colleagues at Janelia Farm as part of the FlyLight project reported in [Jenett et al 2012](http://dx.doi.org/10.1016/j.celrep.2012.09.011). It contained 3 identical copies of the same image channel, an nc82 staining of a single female brain. This was 8 bit uncalibrated data. The original image was acquired with a 20x dry objective on a Zeiss confocal. The lateral resolution was 0.622088 and the slice spacing was 1 micron (uncorrected for air/mounting medium mismatch). This data was later upsampled to 0.622088 isotropic, with 218 slices in Z.

#### JFRC2
We have resaved this original data using the 0.622088 isotropic calibration and commonly refer to this as the **JFRC2** template. It is available as [JFRCtemplate2010.nrrd](../master/template/JFRCtemplate2010.nrrd) in [nrrd format](teem.sourceforge.net/nrrd), which consists of a plain text header concatenated with a gzipped data block.

`JFRCtemplate2010.nrrd` header:
```
NRRD0004
# This NRRD file was generated by pynrrd
# on 2014-05-07 13:49:45(GMT).
# Complete NRRD file format specification at:
# http://teem.sourceforge.net/nrrd/format.html
type: uint8
dimension: 3
space dimension: 3
sizes: 1024 512 218
space directions: (0.622088,0.0,0.0) (0.0,0.622088,0.0) (0.0,0.0,0.622088)
endian: big
encoding: gzip
space units: "?m" "?m" "?m"
```

### Label field data
The label field segmentation describing standardised neuropil domains was generated by Arnim Jenett (Janelia Farm Research Campus), Kazunori Shinomiya and Kei Ito (University of Tokyo) based on the template data described above.There have been at least two iterations of the label field data, the most recent dated 130819, `JFRCtempate2010.mask130819.am`.

The label field in Amira format was resaved as an 8 bit nrrd file with integer levels between 0 and 85, [JFRCtempate2010.mask130819_Original.nrrd](../master/combinedIndexFiles/JFRCtempate2010.mask130819_Original.nrrd). The levels are defined in [Original_Index.tsv](../master/refData/Original_Index.tsv).

`JFRCtempate2010.mask130819_Original.nrrd` header:
```
# This NRRD file was generated by pynrrd
# on 2014-04-30 12:14:26(GMT).
# Complete NRRD file format specification at:
# http://teem.sourceforge.net/nrrd/format.html
type: uint8
dimension: 3
space dimension: 3
sizes: 1024 512 218
space directions: (0.9990234375,0.0,0.0) (0.0,0.998046875,0.0) (0.0,0.0,1.46325688073)
endian: big
encoding: gzip
space units: "pixel" "pixel" "pixel"
```
