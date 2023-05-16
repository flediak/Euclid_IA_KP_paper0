# read files using pandas

import pandas as pd

cost_cent = pd.read_csv('cost_chain71_0.2Rfit40.0_lowz40sdss40hagn20.csv')
cost_sat = pd.read_csv('cost_chain72_0.2Rfit40.0_lowzB40sdss40hagn20.csv')

# columns
- ***runID***: iteration step in calibration procedure
- ***[p0-p5]_cent***: parameters of misalignment model for central galaxies
- ***[p0-p5]_sat***: parameters of misalignment model for satellite galaxies
- ***jobID***: jobID of a given parameter combination within one runID 
- ***chisq***: total chisq, defined over scale range 0.2<r<40.0 Mpc/h
- ***chisq_cent***: total chisq deinfed over scale range 5.0<r<40.0 Mpc/h
- ***chisq_sat***: total chisq deinfed over scale range 0.2<r<5.0 Mpc/h
- ***dkl***: Kullback-Leibler-Divergenz, defined over scale range 0.2<r<40.0 Mpc/h
- ***dkl_cent***: Kullback-Leibler-Divergenz, defined over scale range 0.2<r<40.0 Mpc/h
- ***dkl_sat***: Kullback-Leibler-Divergenz, defined over scale range 0.2<r<40.0 Mpc/h

# chain 71:
- this chain was run to minimize the chisq_cent

# chain 72B:
- this chain was run to minimize the chisq_sat
- B refers to a run in which the bright LOWZ samples L1 and L2 were down weighted when computing the total chisq due to strong differences between FS2 and observations in the small scale clustering signal wgg
