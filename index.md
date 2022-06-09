
#### Academic year 2021/2022, University of Trento
<br>
<br>

### Project Description
The aim of the project is to build a knowledge graph (KG) concerning healthcare heterogeneous data about patients, professionals, facilities and other entities from European countries with different healthcare systems. This result could be the foundation to create a service which help the citizens to handle their own healthcare data, in a context in which the citizens moves around Europe. <br> <br>
In this project we used syntetic (alrady anonymized) data to create a prototype integration serving this purpose. We followed the iTelos development methodology and improved our soulution incrementaly - starting from hypothetical use cases all the way to the final, exploitable knowledge graph while evaluating each step of the procedure. <br> <br>
This solution can potentially be used in clinics, pharmacies, hospitals and research institutions by various personel. Security and data access aspects have not been covered in this project - the application level exploiting this KG should take care of these.
<br>
<br>

### Resources
#### Knowledge Resources:
- [FHIR](https://www.hl7.org/fhir)
- [Schema](https://schema.org)

#### Data Resources  
- [Synthea](https://synthea.mitre.org/) - 100 patients
- [EMRBOTS](http://www.emrbots.org) - 100 patients
- [FHIR SMART data](https://github.com/smart-on-fhir/sample-patients) - 67 patients

- All datasets have been retrieved in csv format. They vaired greatly in the number of object and data properties with Synthea being the richest one and FHIR SMART data being the poorest one. These datasets have all been synthetically generated, therefore there was no need for anonymization.
<br>
<br>

### ER description

- Core eTypes are green, common ones in blue and contextual ones in red.

<br>

- This diagram was defined by looking at the available data, the project’s purpose and the competency questions. However, this procedure made us rethink about all the possible competency questions our solutions can provide an answer to, therefore we decided expand. Doing this allowed us to incorporate a larger amount of diverse data while still maintaining sparsity at a fairly low level.

<br>

- We introduced the Person eType in order to avoid redundancy of defining basic information about our personas (Doctor and Patient). Both of these eTypes extend the eType Person with additional properties unique to them. Moreover, we changed the eType Allergy to be an extension of the eType Condition. Initially, there were two distinct eTypes due to the fact that they were categorized differently in our initial datasets. However, after observing that these entities share all attributes we connected them via IS-A relationship.

![](Images/ER.png)

<br>

- After filtering on the data level the following numbers of instances were obtained: 

![](Images/data_level_filtering.png)



