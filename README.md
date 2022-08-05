# MUCAD

MUCAD stands for _**Mu**ltispectral dataset for **ca**mouflage **d**etection_ and contains multiple camouflaged objects that were captured with a multispectral camera system. The [captures directory](captures) contains a single image file for each band per capture. Each capture maps to a ground truth mask in the [targets directory](targets), in which each camouflaged object has been annotated with a unique color. The color coding (RGB) is defined in the [labels file](labels.yaml). MUCAD contains 23 captures in total.

Detailed information about MUCAD and our research, in which we evaluated several algorithms for detecting the camouflaged objects in the dataset, can be found in our [publication](https://doi.org/10.3390/rs14153755).

### File Structure

- captures
    - <capture_a>_<band_a>.png
    - <capture_a>_<band_b>.png
    - <capture_a>_<band_c>.png
    - ...
    - <capture_b>_<band_a>.png
    - ...
- targets
    - <capture_a>.png
    - <capture_b>.png
    - ...

### Bands

Each capture consists of 7 different bands: visual (VIS), blue, green, red, edge-infrared (EIR), near-infrared (NIR), long-wave infrared (LWIR). 

| Band  | Center Wavelength  | Bandwidth  |
| :---: | :---: | :---: |
|  VIS | - | - |
| blue | 475nm | 32nm |
| green | 560nm | 27nm |
| red | 668nm | 14nm |
| EIR | 717nm | 12nm |
| NIR | 842nm | 57nm |
| LWIR | 10.5μm  | 6μm |

### Targets

The following camouflaged objects were captured in the dataset: 

1. gray tarpaulin 
2. green tarpaulin 
3. artificial grass matt
4. artificial hedge
5. 2D camouflage net
6. 3D camouflage net
7. 2 Persons in different military uniforms
8. 2 gray cars.

All targets were placed in visually similar appearing environments.

## Cite

If you use our dataset in your research please cite the following publication:

```
  @article{rs14153755,
    author         = {Hupel, Tobias and Stütz, Peter}, 
    title          = {Adopting Hyperspectral Anomaly Detection for Near Real-Time Camouflage Detection in Multispectral Imagery},
    journal        = {Remote Sensing},
    volume         = {14},
    year           = {2022},
    number         = {15},
    article-number = {3755},
    url            = {https://www.mdpi.com/2072-4292/14/15/3755},
    issn           = {2072-4292},
    abstract       = {Tactical reconnaissance using small unmanned aerial vehicles has become a common military scenario. However, since their sensor systems are usually limited to rudimentary visual or thermal imaging, the detection of camouflaged objects can be a particularly hard challenge. With respect to SWaP-C criteria, multispectral sensors represent a promising solution to increase the spectral information that could lead to unveiling camouflage. Therefore, this paper investigates and evaluates the applicability of four well-known hyperspectral anomaly detection methods (RX, LRX, CRD, and AED) and a method developed by the authors called local point density (LPD) for near real-time camouflage detection in multispectral imagery based on a specially created dataset. Results show that all targets in the dataset could successfully be detected with an AUC greater than 0.9 by multiple methods, with some methods even reaching an AUC relatively close to 1.0 for certain targets. Yet, great variations in detection performance over all targets and methods were observed. The dataset was additionally enhanced by multiple vegetation indices (BNDVI, GNDVI, and NDRE), which resulted in generally higher detection performances of all methods. Overall, the results demonstrated the general applicability of the hyperspectral anomaly detection methods for camouflage detection in multispectral imagery.},
    doi            = {10.3390/rs14153755}
  }
```
