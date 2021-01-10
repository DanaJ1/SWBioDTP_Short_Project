# **Using Watershed Segmentation to Extract Out Cell Regions from Images for Further Analysis**

This is a short, preliminary piece of code which can be used to apply the Watershed Segmentation algorithm to **transform and segment cell cross-sections** captured within input image data. Once lightsheet fluorescence microscopy has been conducted, this part of the coding pipeline will be specifically adapted for the segmentation of **testes-specific** _**Drosophila melanogaster**_ **spermatids** acquired in multidimensional Carl Zeiss Image Data (CZI).

For the time being, however, this coded algorithm will be tested on two simple example images to assess and demonstrate the suitability of Watershed Segmentation for our desired aims and workflow (as stated in the accompanying report).

### **Running Instructions**

The script provided here is primarily adapted from example code freely available in online sci-kit image processing tutorials (van der Walt et al. 2014). Overall, it is relatively straightforward to run and requires minimal changes to be made because it is specific to the accompanying sample image data.

In brief:
1. Download **all** files supplied within this encompassing GitHub respository into a single file directory, including:
   * The Jupyter Notebook entitled **"Watershed_Final.ipynb"**, which contains the final version of the working coded script alongside guided comments and debugging annotations.
   * The two sample data TIFF files, each comprising an example input image of user-generated phantoms with individual cells acquired and modified from Yang et al. (2000). These GFP-expressing cell-like cross-sections are either distinct to one another or showing some degree of overlap, as saved in the **"No_Contacts.tif"** and **"With_Contacts.tif"** files, respectively.

2. Within the "Watershed_Final.ipynb" notebook, the Watershed Segmentation is run **twice** in succession. Image processing is therefore performed on both input images ("No_Contacts.tif" or "With_Contacts.tif") one after the other, and their corresponding outputs are saved separately.

3. Each scripted cell should be ran in the usual sequential, chronological order - consecutively from top to bottom. This will lead the user directly from file input, and loading as a numpy array, through to the global transformation itself and a graphical presentation of the final cell extraction for **both** image data files. Supporting comments are annotated alongside each stage of the script code, giving details as to what each section is actually doing/performing.

4. The next step of this workflow is the **acquisition of the segmented cell regions.** The resulting output is plotted and displayed within the Jupyter Notebook itself to demonstrate its sucess to the user; the first (furthest left) column depicts the original input image, the middle column shows the outcome of the Euclidean distance transform and the final column (on the right) reveals the separated objects presented in a multicoloured format to improve visual clarity.

5. The successful operation of Watershed Segmentation on **both** example images confirms its feasibility for applications in cell selection and information retrieval, regardless of fluorescent overlap.

6. Finally, each segmented cell is **looped over iteratively** and assigned a counter using the enumerate function. This means that both the individual cell regions and their associated indices can be kept track of, then returned and saved into a new, appropriate file format.*

_*NB. In practice, this would be to prepare for the next stages of analysis (e.g. finding the center as a vector from which surrounding protein concentrations can be calculated)._

### **References**

van der Walt, S. et al. 2014. scikit-image: image processing in Python. *PeerJ* 2, p. e453. doi: 10.7717/peerj.453.

Yang, M. et al. 2000. Whole-body optical imaging of green fluorescent protein-expressing tumors and metastases. *Proceedings of the National Academy of Sciences* 97(3), p. 1206. doi: 10.1073/pnas.97.3.1206.