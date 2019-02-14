Individual_Reconstruction_Analysis: this script is drafted for functional localizer processing. It unpacks the relevant dicoms; ensures the runs are valid; proceeds to scan scaninfo parse it for relevant run info; puts in the design files (for this specific PCA project). Lastly, there are cells that can be ignored at the end. These are only temporary.
LEADS
LEADS_redcapfill: this script will take all subjects in the recon directory and run the preproc, smoothing, and glmfit. Then it will create a matrix with all of redcap's info; will also pull in QC notes from LONI; my own QC notes; and all aparc+aseg stats (I think from raw data). How to optimize this data pulling; demographic data ill be fully shared later; need an effective way to add new fields without manually changing the RedCap Instrument spreadsheet.
Preprocessing_Workflow: this script is a short tutorial of nipype.
Swarm_Plot: this script generates swarm plots for LEADS subjects' aparc and asegand aseg stats.
Troubleshooting_Nipype: this script ensures everything needed for a nipype environment is installed.
leads_unpack: this script will unpack structural dicoms and ensure runs are valid; will choose the first structural run that is valid and print out a warning if the subject has > one. It creates execute.recon.list. It will also initiate a bash script on launchpad (execute.recon.bs) with all of the subjects that have not been run. Need to think about how to better automate this process so that I can run the same script and it will stop before manual edits; then run the script again after manual edits and know to implement. Also needs improvements by making codes/workspace in nipype; better organize variables that are redefined throughout script.
mytools
old_RedCap: this script is junk. Can be deleted.
visualization: this script prints out a visualization of the nipype workflow for spmflow preprocessing. Use as an example to generate more.
