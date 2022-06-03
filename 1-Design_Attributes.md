# Design process and design attributes

The status of Diversity Cyber Council as a nonprofit organisation provides some unique constraints that we feel are important to be reflected in the design.

## Primary design attributes

### Modularity (feature self-containment)
As a nonprofit organisation, Diversity Cyber Council might not have access to the same resources as commercial organisations at all times. When building the Spotlight platform, it might be more beneficial to divide the work between multiple groups. Similarly, as the platform evolves, features will be added, modified or phased out. By having the system designed so that each domain is self-contained, each team can be smaller and easier to deliver. This also allows the platform as a whole to be more flexible, and minimise the amount needed when adding or evolving features.

### Total cost of ownership
As nonprofits have to be mindful of costs, the final solution should minimise ongoing operations costs and anything that would form a long-running expense for the organisation. This includes both computation and licensing costs, as well as any staff needed to maintain it. Once built, the platform should be as efficient as possible.

## Secondary design attributes

### Stability
Diversity Cyber Council operates on the trust of communities, and this could easily be lost if the platform is not available

### Data-Driven
As one of the problems is decentralisation and lack of visibility of nonprofit organisations, we must ensure we capture all possible interactions to be able to address the gaps.


# What is and what is not designed

## What we have focused on

- The functional split of services, and defining responsibilities of each one
- Defining and describing interactions between services
- Identifying and describing non-functional and supporting services needed to deliver capabilities
- Describing the technology of the solution
- Identifying the minimal data needed for the platform to function, and keeping the design flexible enough to expand with additional data fields in the future

## What we have not done

- Narrow solutions down to a particular language, library, framework or hosting unless strongly dictated by the requirements. We feel that in general cases most implementations would be interchangeable, and strongly dependent on people who would be available. If some functionality would be best provided by 3rd party products, we aimed to provide matching alternatives to choose from. We did our best to pick up 3rd parties who have free or nonprofit plans

## What we have wished we have done but ran out of time

- Design entities in the data tables and API calls
- Capture more nuanced benefits and tradeoffs discussion in architecture decision logs

