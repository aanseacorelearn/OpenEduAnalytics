# OEA Data Schema Standardization

OEA data schemas aim to enhance sharing and transferability of OEA technical assets across differing Synapse environments. Because data sources and formats vary from one school system's Synapse environment to another, integrating common data standard into OEA module and packages allows for data science solutions to be built on a common foundation. Examples of common education data standards include:

-  [Ed-Fi Standards](https://techdocs.ed-fi.org/display/ETKB/Ed-Fi+Standards): The Ed-Fi Data Standard is the widely adopted, CEDS-aligned, open-source data standard developed by the educational community for the betterment of the community. The Ed-Fi Data Standard serves as the foundation for enabling interoperability among secure data systems and contains a Unifying Data Model designed to capture the meaning and inherent structure in the most important information in the K–12 education enterprise.
-  [Systems Interoperability Framework (SIF)](https://www.nsip.edu.au/systems-interoperability-framework): SIF, the Systems Interoperability Framework, is an open, industry supported standard used to link together data systems within the school sector. SIF is well established in the US, the UK and Australia. Application of the standard enables systems to interact and share data efficiently, securely and cost effectively, regardless of the application and technology platform.
-  [Caliper Analytics Specification](https://www.imsglobal.org/spec/caliper/v1p2): IMS Caliper Analytics® is a technical specification that describes a structured set of vocabulary that assists institutions in collecting learning and usage data from digital resources and learning tools. This data can be used to present information to students, instructors, advisers, and administrators to drive effective decision making and promote learner success.

OEA data schemas integrate parts of these education data standards into common data categories seen in all education systems. A summary of existing OEA schemas included:

- [Digital Engagement Schema](https://github.com/microsoft/OpenEduAnalytics/tree/main/schemas/schema_catalog/Digital_Engagement_Schema): Student and staff engagement with education technology (i.e. M365, tablet learning aps, learning management systems). Data of this type is typically log data for application logins and interactions.)
- [Attendance Schema](https://github.com/microsoft/OpenEduAnalytics/tree/main/schemas/schema_catalog/Attendance_Schema): Student daily attendance and absence records.

OEA data schemas are typically applied to data in Stage 2 (such as processed [OEA module](https://github.com/microsoft/OpenEduAnalytics/tree/main/modules) data). Data processed into an OEA schema can then be integrated into a given use case.
