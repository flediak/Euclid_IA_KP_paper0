# cost files
- cost_chain71_0.2Rfit40.0_lowz40sdss40hagn20.csv
- cost_chain72_0.2Rfit40.0_lowzB40sdss40hagn20.csv
- contain sampling points in parameter space of IA model component for galaxy misalignment

## chain 71:
- this chain was run to minimize the chisq_cent

## chain 72B:
- this chain was run to minimize the chisq_sat
- B refers to a run in which the bright LOWZ samples L1 and L2 were down weighted when computing the total chisq due to strong differences between FS2 and observations in the small scale clustering signal wgg

## columns
- ***runID***: iteration step in calibration procedure
- ***jobID***: jobID of a given parameter combination within one runID 
- ***[p0-p5]_cent***: parameters of misalignment model for central galaxies
- ***[p0-p5]_sat***: parameters of misalignment model for satellite galaxies
- ***chisq***: total chisq, defined over scale range 0.2<r<40.0 Mpc/h
- ***chisq_cent***: total chisq deinfed over scale range 5.0<r<40.0 Mpc/h
- ***chisq_sat***: total chisq deinfed over scale range 0.2<r<5.0 Mpc/h
- ***dkl***: Kullback-Leibler-Divergenz, defined over scale range 0.2<r<40.0 Mpc/h
- ***dkl_cent***: Kullback-Leibler-Divergenz, defined over scale range 0.2<r<40.0 Mpc/h
- ***dkl_sat***: Kullback-Leibler-Divergenz, defined over scale range 0.2<r<40.0 Mpc/h

## read files using pandas
```import pandas as pd```

```cost_cent = pd.read_csv('cost_chain71_0.2Rfit40.0_lowz40sdss40hagn20.csv')```

```cost_sat = pd.read_csv('cost_chain72_0.2Rfit40.0_lowzB40sdss40hagn20.csv')```

# correlation measurements
## name convention
- folders: ```D-[density sample]_S-[shape sample]/run[runID]```
- files for random realizations: ```[correlation typ]_r[runID]_p[jobID]_rep[1-3].csv```
- files for average over random realizations: ```[correlation typ]_r[runID]_p[jobID].csv```
- example: ```D-lowz_S-lowz.l4/run0/wgp_r0_p0_rep1.csv```
- ***sampling points in cost files can be linked to files with correlation measurements via runID and jobID***

## columns

### wgp

### eta
