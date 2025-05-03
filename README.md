# L2_featuresN File Processing

The L2_featuresN.hdf5 file was processed using Python, h5py, and pandas. The primary goal was to extract data and metadata from the file and convert it into a more accessible CSV format. The L2_featuresN.hdf5 file was obtained by using the Tierpsy Tracker.

Key Steps:

File Inspection: The L2_featuresN.hdf5 file was inspected to identify its structure and contents, including groups and datasets.

Dataset Extraction:

The following datasets were extracted and converted to individual CSV files:

blob_features

features_stats

timeseries_data

trajectories_data

Non-dataset items were handled as follows:

coordinates: This HDF5 group contains 3D datasets ('dorsal_contours', 'skeletons', 'ventral_contours'). These datasets were extracted and stored as JSON strings within individual CSV files to preserve their 3D structure.

provenance_tracking: This HDF5 group contains metadata attributes ('CLASS', 'TITLE', 'VERSION'). These attributes were extracted and written to a single-row CSV file.

Output Format:

Extracted datasets were saved as CSV files.

3D coordinate data ('dorsal_contours', 'skeletons', 'ventral_contours') was stored as JSON strings within individual CSV files.

Metadata attributes from 'provenance_tracking' were saved as a single-row CSV file.

Libraries Used:

h5py: For reading and navigating the HDF5 file structure.

pandas: For creating and exporting DataFrames to CSV files.

numpy:  For handling numerical data.

json: For converting 3D coordinate data to JSON strings.

Purpose:

The processing steps outlined above were performed to make the data contained within the L2_featuresN.hdf5 file more readily available for analysis. The conversion to CSV format allows for easier manipulation and exploration of the data using standard data analysis tools.  The 3D coordinate data was stored as JSON to preserve its original structure, and the provenance tracking metadata was extracted to maintain important information about the data's origin.
