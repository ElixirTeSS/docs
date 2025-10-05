# Definitions

Definitions of terms and user roles used across TeSS.

## Terms 

Definition of common terms used across TeSS.

### Content provider

Entities (such as academic institutions, non-profit organisations, portals) that provide training materials of relevance.

### Event

An event in TeSS is a link to a single training event sourced by a provider along with description and other meta information (e.g. date, location, audience, ontological categorization, keywords).

Training events can be added manually or automatically harvested from a provider's website.


### Exchange (TeSS-X)

If a community runs its own instance then a TeSS-X plugin sets up an exchange with other instances.
In the mTeSS-X project, we will show how several TeSS-instance catalogues exchange nominated training resources. 
See [What do we mean by eXchange?](https://elixirtess.github.io/mTeSS-X/exchange) on the mTeSS-X project website for details.


### Instance

One installation of the TeSS Platform, on a server, managed by a technical administrator. An instance may have multiple spaces, if this option has been enabled by the administrator.

Examples of TeSS instances can be viewed on the [global usage page](https://elixirtess.github.io/mTeSS-X/global) of the mTeSS-X project website.


### Learning path

A a pathway that guides learners through a set of modules (courses/materials) to be undertaken progressively (from lower- to higher-order thinking skills) to acquire the desired knowledge and skills on a subject by the end of the pathway.


### mTeSS-X Project

The [mTeSS-X Project](https://elixirtess.github.io/mTeSS-X) (Multi-space Training e-Support System with eXchange) overcomes the fragmentation of training resources across Research Infrastructures and the European Science Clusters.
The project aims to enhance existing TeSS-based training registries or catalogues like [ELIXIR TeSS (life sciences)](https://tess.elixir-europe.org/) and [PaN-Training (photon and neutron)](https://www.panosc.eu/training-catalogue/) by building an aggregator for these and similar platforms.


### Space (mTeSS)

A single TeSS instance presents multiple tailored spaces (catalogues) whose selections of training material are “views” on a global catalogue. 
Each community registers, maintains and curates their material for their members in their own virtual space in the common portal environment.
See [What do we mean by Multi-space/tenancy?](https://elixirtess.github.io/mTeSS-X/multi-space) on the mTeSS-X project website for details.


### TeSSHub

The first TeSS instance with multiple spaces. This will be one of the outputs from the mTeSS-X project, where [ELIXIR TeSS (life sciences)](https://tess.elixir-europe.org/) and [PaN-Training (photon and neutron)](https://www.panosc.eu/training-catalogue/) will be multipe spaces running from the same server, appearing as distinct catalogue. 

Communities will be welcome to request their own space on the TeSSHub, providing them with their own registry, without the need to host and maintain their own instance.  


### TeSS Platform

The main codebase which is used for development, written in Ruby on Rails. The code is open source and [available on GitHub](https://github.com/ElixirTeSS/TeSS) under a BSD 3-Clause licence. 


### TeSS Portal

Shorthand for the [ELIXIR TeSS](https://tess.elixir-europe.org/) portal, the training registry for Europe's distributed infrastructure for life-science data, built using the TeSS Platform. 


### Training material

In the context of TeSS, a training material is a link to a single online training material sourced by a content provider (such as a text on a Web page, presentation, video) along with description and other meta information (e.g. ontological categorization, keywords).

Materials can be added manually or automatically harvested from a provider's website.



## Roles

Definitions of user roles in TeSS. 

### Administrator

The technical administrator, responsible for installation, configuration and maintenance of a TeSS instance.

### Author

Individuals and organisations involved in the preparation, creation or presentation of the published work.

### Collaborator

An individual who has been granted editing rights to a material, topic or learning path by the individual (owner) who created it.

### Contributor 

Individuals and organisations that contributed to the published work but are not authors.

### Curator

An individual who has been granted permission to create a learning path in TeSS while following their community’s editorial process, or edit the materials associated with a content provider or node.

### Editor (of a content provider)

A person with editing rights to a content provider.

### Owner

An individual who has created a material, topic or learning path in TeSS.

### Space Manager

The person responsible for managing a space within an instance.
