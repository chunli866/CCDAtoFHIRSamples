# Why this repo was created?
The HL7 Cross Group Project workgroup (https://confluence.hl7.org/display/CGP/Cross-Group+Projects+Home) launched a project (https://confluence.hl7.org/display/CGP/C-CDA+to+and+from+US+Core+Mapping) to develop a mapping between the C-CDA 2.1 and FHIR R4 US Core standards. Because various vendors have developed their own mappings of the C-CDA documents to FHIR resources, there is a need to coordinate these efforts and to align them with the guideline that is currently under development. For this reason, we created this repo to host a non-PHI CCD construct as a shared inbound document, and asked vendors to use their mapping engine to produce outbound FHIR resources/bundle/composition. This allows for comparison of the mapping outcomes for the same source document across different vendors in the field. To help align the mappings, we have also hosted weekly calls and FHIR Connectathon track to discuss the different perspectives. For more information, please visit https://confluence.hl7.org/pages/viewpage.action?pageId=139662703.

# What is in this repo?
This repo includes an inbound CCD construct, and outbound FHIR mappings. 

# How is this repo organized?
The "Input" folder hosts the shared input CCD, the Output and Reformatted folder host the output FHIR artifacts. In the FHIR folders, they are further broken down by different clincial domains to facilitate easy comparison. Each vendor's file are indicated in the filename. The difference between those in the "Output" path and "Reformatted" path are in the order of the data elements within the mapped resources. The former contains the data elements in their original order from vendor's submission, whereas the data elements are re-ordered in the "Reformatted" path, so that they follow the same sequence to allow easier comparison between vendors. The "Scripts" path contains the JavaScript script and related node package information to allow vendors to reformat their own individual resource.

# How may I use the repo?
Start with the input CCD to understand the inbound data, and then check out the Output or Reformatted folder for the FHIR resources of the respective clinical domains. 

# How may I contribute?
The easiest way to contribute is to download the input CCD from the "Input" folder, run it through your C-CDA to FHIR mapping engine, and upload the outbound composition/bundle in the Output/Bundle-Complete folder (please create a new folder to represent your company). 
You might then choose to parse the data to the individual clinical domains and upload to the respective subfolders in the "Output" path, and/or use the script to reorder the data elements in your individual FHIR resource and upload to the "Reformatted" path. You may also email cli@diameterhealth.com to get assistance in parsing your bundle to individual resources and reorder them.

# How may I get additional information or assistance?
You may contact Chun Li at cli@diameterhealth.com. 

