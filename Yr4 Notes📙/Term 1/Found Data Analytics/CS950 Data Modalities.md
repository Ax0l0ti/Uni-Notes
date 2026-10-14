# CS950 Data Modalities
---
> [!info]- File Details
> Includes information about this (genus:: Note) from [Year::3]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  08-10-2026
> > *Module :* [[]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#]]


--- 
> [!TIP]+ 🕰️* Speed run*
> Break down of topic 
> There are four types of attributes: 
> > [!NOTE]- Nominal (Categoric) 
> > Names, Strings, Attributes. Can use numbers to represent. HOWEVER, only mode can be used, not mean or range
> 
> > [!NOTE]- Binary
> > nominal attribute with only two categories: 0 or 1
> > Hamming distance 
> 
> > [!NOTE]- Ordinal
> > Ordered / Ranked e.g $A^*,A,B,C$
> 
> > [!NOTE]- Numeric
> > Interval vs ratio e.g Celcius vs Kelvin
> > Only 0 value in Kelvin, $5C$ is not half of $10C$
> 
> [[Distance Metrics]] 
> ### Storing Data
> > [!quote]- Tabular 
> > Data Sparse vs Dense
> > ![[Sparse Tabular Data Storage.png|400]]
> > Storage - CSV / Excel
> > SQL Scalable, Well Documented, data integrity, fast, multiple data views, built in backup & recovery
> > BUT Security risks, complex, Vendor Lock in 
>

> [!NOTE]
> > > 

---
Time Series
collected over regular intervals

Geo Spatial
Vector 
+Precise, Data rich, more efficient then raster, Resolution-independent due to vectorisation
-Combination complexity, Processing overhead, Most inputs are raster leading to Sense Inconsistency


• Advantages: • Reveals spatial patterns: Clusters of activity. • Reveals regional differences • Supports decision making: Which areas need support? • All of the above may not be clear to see in tabular data! • Compatible with other data modalities: Can be used in time-series. • Easy to gather?: Can be obtained from sensors.

• Disadvantages: • Complexity: The numbers have meanings (location). More difficult to understand than other modalities. • Different coordinate systems exist, and distance calculation can be difficult (the earth is curved!). • Noise: Inaccuracies in location gathering can change the meaning of the data. • Privacy Concerns • Large Data

![[CS950Data Modality.png]]