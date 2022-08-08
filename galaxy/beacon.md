# Participate in the [beacon-network](https://beacon-network.org/#/)!

The beacon network is a search engine for genetic variants developed by the 
[Global Alliance for Genomics and Health](https://www.ga4gh.org/).
Variants are provided by a network of individual web services called
[beacons](https://beacon-network.org/#/about).

There is a beacon instance running on galaxy.eu that can be used by every galaxy user to provide data to the beacon
network


## What will be shared with the network

Beacon will get questions of the form _"Do you have information about the following mutation?"_ and respond 
with _Yes_ or _No_

<div style="border: 1px solid red; border-radius: 5px; background-color: rgba(255,0,0,0.07); padding: 8px 16px;">
Even sensitive data can be shared as it is not possible to reconstruct files or even identify samples from such queries.

</div>


## How to share variants

You can share variants from any _vcf_ or _vcf.bgzip_ file by following the steps below

#### 1. Make sure your file satisfies the conditions below

---

* Defines at least one sample
> some mappers will not add the _FORMAT_ and subsequent sample columns of only one sample is processed
* For each variant, includes values for __AC__ or __AN__ in the info field
* File has been compued for a human genome e.g. _GRCh38_, _hg19_,... and has the reference assigned to it in galaxy
  (which is done automatically by most mappers)
---

#### 2. Make sure beacon sharing is enabled in your user settings

There is a setting to opt in to beacon sharing.
(TODO: write more)

#### 3. Switch to History `___BEACON_PICKUP___`

If you have no such history you can simply create it

#### 4. Add the file to Histoy `___BEACON_PICKUP___`

#### 5. Wait
The beacon database is rebuilt every night. Your variants will appear tomorrow :joy:


## How to share actual data

Assume a person P searches for a specific variant that shows up in one of your data files. P will only get the 
information that there is _someone_ on the galaxy.eu server that has _some_ information about the variant.

P then has to contact galaxy admin A as only admins with direct database access can find out which
variant stems from which file.

A will then contact you and give you contact details for B so you can negociate a potential data access.


## How to remove data

Remove files from the beacon history to stop sharing it