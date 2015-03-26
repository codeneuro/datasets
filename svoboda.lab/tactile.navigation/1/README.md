## Example two-photon calcium imaging data

Calcium imaging in mouse vibrissal somatosensory cortex using two-photo laser scanning microscopy, while the animal performs a tactile virtual reality behavior (described in Sofroniew et al., 2014, Journal of Neuroscience). Data used as an example dataset in Freeman et al., 2014, Nature Methods.

Data aquired by Nicholas Sofroniew in the lab of Karel Svoboda at Janelia Research Campus.

Location on S3
- `s3n://neuro.datasets/svoboda.lab/tactile.navigation/1/`

Contents
- `images` (folder containing binary images representation)
- `series` (folder containing binary time series representation)
- `params/covariates.json` (behavioral covariates)
- `info.json` (data set dimensions and other properies)

Load data using the [Thunder library](https://github.com/thunder-project/thunder), an open source project built on Spark, also avaialble through [spark-packages.org](http://spark-packages.org/package/freeman-lab/thunder).

```
from thunder import ThunderContext
tsc = ThunderContext(sc)
imgs = tsc.loadImages('insert/final/path/images')
series = tsc.loadSeries('insert/final/path/series')
params = tsc.loadParams('insert/final/path/params/covariates.json')
```
