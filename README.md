
# Monthly Reports
This repository includes the code that runs the monthly reports and generate statistics for fractional cover for Australian regions
The code in this repository initially grabs data from NCI. See below for details.
This code sits in CSIRO's network in 

    /datasets/work/lw-lpdaac/work/fc-wron/data/monthly_fc_run/monthly_reports/
(windows equivalent: `\\fs1-cbr.nexus.csiro.au\{lw-lpdaac}\work\fc-wron\data\monthly_fc_run\monthly_reports`)

## Overview
This repository is the last of a 4-part workflow used for creating the MODIS Fractional Cover product and derived reports and statistics. 
The flowchart below shows the 4 part process. An editable version of the flowchart can be accessed in https://docs.google.com/drawings/d/14qGEwsMeR98Kbnfan5z8smXKcpzJiENMwNrS4_r7dhA/edit?usp=sharing

![flowchart MODIS FC overview](MODIS_Fractional_Cover_pipeline.svg)

## Steps:
 1. Copy data (Aus FC mosaics) from GADI  
 2. Submit monthly reports (jobs) for NRM regions
 3. Submit monthly reports (jobs) for LGA regions
 4. Submit monthly reports (jobs) for big regions (separate code)
 5. Calculate statistics for Stephan
 6. Calculate statistics (saved to a separate csv file)

## specifics
This code sits in CSIRO's network in 

    /datasets/work/lw-lpdaac/work/fc-wron/data/monthly_fc_run/monthly_reports/

The scripts are triggered initially by `automated_jobs.sh`: 

    bash automated_jobs.sh

then: 

    bash run_calculate_stats_all.sh
and then: 

    bash sbatch_aggregate_statistics_fc.sh

All this is run weekly via a cron job -**COMPLETE WHEN Cron jobs are set up**- 


## notes
1.  See in NCI files are up to date in `/g/data/tc43/modis-fc/v310/tiles/8-day` and `/g/data/tc43/modis-fc/v310/tiles/monthly`. Process and scripts as per  [https://bitbucket.csiro.au/projects/LANDSCAPES/repos/geoglam/browse](https://bitbucket.csiro.au/projects/LANDSCAPES/repos/geoglam/browse)
2.  Run/check automated process for creating mosaics as per  [https://bitbucket.csiro.au/projects/LANDSCAPES/repos/fc_mosaics/browse](https://bitbucket.csiro.au/projects/LANDSCAPES/repos/fc_mosaics/browse)
3.  To copy all the files from NCI, run `copy_monthly_data.sh` (this is done in `automated_jobs.sh`)



