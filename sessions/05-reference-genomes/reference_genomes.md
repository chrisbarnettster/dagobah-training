layout: true
class: inverse
---
class: special, center
![GATC Logo](../shared-images/gcc2017_logo_black.png)

# Reference Genomes in Galaxy


**Slides: @blankenberg, @Slugger70**


.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---

layout: true
class: left, inverse

---
class: left, middle, center
![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)

## Please interrupt



*We are here to answer questions!*

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
class: left
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Overview
.large[
* **Intro to built in datasets**
* Some problems
* Data Managers
]

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
class: left
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Built in Data

![List_of_data.png](images/i06-List_of_data.png)



.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
class: left

## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Data, what data?
.large[
* Some genomes are large! Human, Mouse, Coral
* Some tools require indices of the genomes.
* The indices take a long time to build!
* Better to pre-build the indices.
]

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]

---
class: left

## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png) The old ways..
.large[
* Very manual process
* Install tool and indexer
* Download the genome
* Index via command line
* Edit 3 different config files
* Make sure you use \<tabs\> not \<spaces\> in tab separated data

]
---
class: left
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Overview
.large[
* Intro to built in datasets
* **Some problems**
* Data Managers
]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Some Problems!
.large[
* Time consuming!
  * ~30 minutes work just to add a new genome to 1 tool!

* Administrator needs to know:
  * how to index **every** tool
  * expected format of the reference data
  * format of the .loc file
]
.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Typical conversation

.middle[![ref-problem-1.png](images/Ref-problem-1.png)]

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Typical conversation

.middle[![ref-problem-2.png](images/Ref-problem-2.png)]

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Typical conversation

.middle[![ref-problem-3.png](images/Ref-problem-3.png)]

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Typical conversation

.middle[![ref-problem-4.png](images/Ref-problem-4.png)]

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---

## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Other concerns

.large[
* **Accessible?**
  * Manually download genome FASTA files
  * Download, compile, run bwa index; which options?
* **Reproducible?**
  * Only if the person performing manual steps keeps good notes
* **Transparent?**
  * Send email to sysadmin asking for notes
  * Restart Galaxy server for new entries
]

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
class: left
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Overview
.large[
* Intro to built in datasets
* Built in data hierarchy
* Some problems
* **Data Managers**
]
(now we're onto the good stuff!)
---

## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Data Managers
.large[
* Allows for the **creation of built-in** (reference) data
	* underlying data
	* data tables
	* \*.loc files

* Specialized Galaxy tools that can only be accessed by an admin

* Defined **locally** or installed from **ToolShed**
]
.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---

## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Data Managers
.large[
* **Flexible** framework
  * Not just genomic data
  * Run Data Managers through UI
  * Workflow compatible
  * API
* Examples
  * Adding new genome builds (dbkeys)
  * Fetching genome (fasta) sequences
  * Building short read mapper indices for genomes
]
.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]

---

## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Special class of Galaxy tool

Looks just like a normal Galaxy tool!

![Data-manager-ui.png](images/Data-manager-ui.png)


.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]

---

## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Data Managers Admin
.large[
* Located on the Galaxy's Admin Tab under **Local Data**
]
![data_managers_tool_list.png](images/data_managers_tool_list.png)

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Data Managers Admin

.large[
* UI tools to fetch reference genomes/build indices
* View progress of index build jobs
* View contents of tool data tables
]
![data_table_ui.png](images/data_table_ui.png)

.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Further reading

.large[
* Galaxy Wiki Page on Data Managers
  * Details
  * Building
  * Examples

https://wiki.galaxyproject.org/Admin/Tools/DataManagers
]
.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
---
## ![GATC Logo](../shared-images/gcc2017_logo_black_2in.png)  Exercise Time!



.footnote[\#usegalaxy \#GCC2017 / @galaxyproject]
