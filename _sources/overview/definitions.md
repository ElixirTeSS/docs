# Definitions

Definitions of terms and user roles used across TeSS.

## Overall terms and concepts 

Definition of common terms used across TeSS, sorted alphabetically.

```{glossary}

Content provider
    Entities (such as academic institutions, non-profit organisations, portals) that provide training materials of relevance.

ELIXIR TeSS Portal
    The [ELIXIR TeSS](https://tess.elixir-europe.org/) portal, the training registry for Europe's distributed infrastructure for life-science data, is built using the TeSS Platform.

Event
    An event in TeSS is a link to a single training event sourced by a provider along with description and other meta information (e.g. date, location, audience, ontological categorization, keywords).
    
    Training events can be added manually or automatically harvested from a provider's website.

Exchange (TeSS-X)
    If a community runs its own instance then a TeSS-X plugin sets up an exchange with other instances.
    In the mTeSS-X project, we will show how several TeSS-instance catalogues exchange nominated training resources. 
    See [What do we mean by eXchange?](https://elixirtess.github.io/mTeSS-X/exchange) on the mTeSS-X project website for details.

Instance
    One installation of the TeSS Platform, on a server, managed by a technical administrator. An instance may have multiple spaces, if this option has been enabled by the administrator.
    
    Examples of TeSS instances can be viewed on the [global usages page](global).

Learning path
    A a pathway that guides learners through a set of modules (courses/materials) to be undertaken progressively (from lower- to higher-order thinking skills) to acquire the desired knowledge and skills on a subject by the end of the pathway.

mTeSS-X 
    The [mTeSS-X Project](mtess-x) (Multi-space Training e-Support System with eXchange) overcomes the fragmentation of training resources across Research Infrastructures and the European Science Clusters.
    The project aims to enhance existing TeSS-based training registries or catalogues like [ELIXIR TeSS (life sciences)](https://tess.elixir-europe.org/) and [PaN-Training (photon and neutron)](https://www.panosc.eu/training-catalogue/) by building an aggregator for these and similar platforms.

Space (mTeSS)
    A single TeSS instance presents multiple tailored spaces (catalogues) whose selections of training material are “views” on a global catalogue. 
    Each community registers, maintains and curates their material for their members in their own virtual space in the common portal environment.
    See [Introduction to spaces](../spaces/intro-spaces) for details.

TeSSHub
    The first TeSS instance with multiple spaces. This will be one of the outputs from the mTeSS-X project, where [ELIXIR TeSS (life sciences)](https://tess.elixir-europe.org/) and [PaN-Training (photon and neutron)](https://www.panosc.eu/training-catalogue/) will be multipe spaces running from the same server, appearing as distinct catalogue. 
    
    Communities will be welcome to request their own space on the TeSSHub, providing them with their own registry, without the need to host and maintain their own instance.  

TeSS Platform
    The main codebase which is used for development, written in Ruby on Rails. The code is open source and [available on GitHub](https://github.com/ElixirTeSS/TeSS) under a BSD 3-Clause licence. 

Training material
    In the context of TeSS, a training material is a link to a single online training material sourced by a content provider (such as a text on a Web page, presentation, video) along with description and other meta information (e.g. ontological categorization, keywords).
    
    Materials can be added manually or automatically harvested from a provider's website.
```

## Materials

Definitions of fields used to describe training materials, sorted in the order they appear when editing a material.

```{glossary}
Title
    A concise sentence that clearly indicates the topic of the training material. 
    It should provide context and help learners understand what the material will cover.

Description
    A short, informative summary that outlines the purpose, scope, key topic and of the training material. 
    It should help the learners and instructors understand the content and relevance of the training before engaging with it.

Resource Type
    The predominant category that describes the kind of learning material, for example, a presentation, video, handout, publication, poster.

Scientific Topics
    The scientific subject or field that the training material focuses on, for example, bioinformatics, genetics, biodiversity, genomics.

Keywords
    Free text about topics clearly identifying the training material.

License
    The most appropriate license that specifies the terms under which your training material and dataset can be used, modified, and distributed. 
    Various options of licenses, for example, Creative Commons License are available to choose from. 
    Free text is allowed if your license is not available in the menu.

Status
    The current state or stage of the training material indicating whether it is Active, Under development, or Archived.

Contact
    The individual responsible for communication regarding the training material, typically including name, affiliation, email address, and an ORCID identifier if possible.

DOI (Digital Object Identifier)
    A unique, persistent alphanumeric string assigned to the training material that provides a permanent link to its location for long-term accessibility and citation tracking.

Version
    A specific iteration or release of the training material document, labeled to track updates (for example, v1.0, v2.1).

Content Provider
    The organisation, institution, or individual responsible for providing, and maintaining the training material.

Authors
    Individuals who made substantial intellectual or technical contributions to the conception, design, execution of the training material.

Contributor
    Individuals or entities who provided specific assistance, technical input, data, or materials to the work but may not meet the full criteria for authorship.

Target Audience
    The intended group of users or learners for whom the training material is designed, such as researchers, students, postdocs, trainers.

Prerequisites
    The foundational knowledge, skills, or competencies that a learner or user must possess before engaging with the training content.

Competency Levels
    Gradations of expertise or proficiency expected of learners or users, categorised as beginner, intermediate, or advanced.

Learning Objectives
    Clearly defined, measurable statements describing the specific knowledge, skills a learner should acquire after completing the training course.

Events
    Workshops, seminars, conferences, summer or winter schools that contribute to or disseminate the training.

```


## Events

Definitions of fields used to describe events, sorted in the order they appear when editing an event.

```{glossary}
Type
    Describing the whether the event will be held Face-to-face, Online or both (hybrid).
 
Subtitle
    
URL
    Location where the event and its details are advertised on the internet.
 
Duration
    Time slot assigned/required for the event, for example, 2hrs, 2days.
 
Language of instruction
    The language in which the training/seminar/lecture will be delivered. 
    Select from the list of available options.
 
Address, Venue, City, Region, Postcode
    Physical location of the event if its being conducted Face-to-face.
 
Eligibility
    Options for registration. 
    To be chosen from one of the three: 1. First come first served, 2. Registration of Interest, 3. By invitation.
 
Organiser
    Institution/Organisation or the individual coordinating to organise the event.
 
Host institutions
    Institution/Organisation where the event will be held. 
 
Capacity
    Maximum number of participants that can take part in the event.
 
Event type
    The category of an event based on its purpose, format, and activities. 
    Can be chosen from the following options:
    - Awards and prizegivings
    - Meeting and conference
    - Receptions and networking
    - Workshops and courses
 
Nodes (ELIXIR Specific)
    The ELIXIR Node (Country) hosting the event 
 
Sponsors
    Institution/Organisation or funding bodies that funded that event.

```

## Roles

Definitions of user roles in TeSS. 

```{glossary}
Administrator
    The technical administrator, responsible for installation, configuration and maintenance of a TeSS instance.

Author
    Individuals and organisations involved in the preparation, creation or presentation of the published work.

Collaborator
    An individual who has been granted editing rights to a material, topic or learning path by the individual (owner) who created it.

Contributor 
    Individuals and organisations that contributed to the published work but are not authors.

Curator
    An individual who has been granted permission to create a learning path in TeSS while following their community’s editorial process, or edit the materials associated with a content provider or node.

Editor (of a content provider)
    A person with editing rights to a content provider.

Owner
    An individual who has created a material, topic or learning path in TeSS.

Space Manager
    The person responsible for managing a space within an instance.
```