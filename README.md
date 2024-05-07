<p align="center">
  <a href="https://github.com/EnAccess/OpenSmartMeter">
    <img
      src="https://drive.google.com/uc?id=1gtL_p7l3HbOcCzc09A7KW5d7B5qn-BDs"
      alt="OpenSmartMeter"
      width="640"
    >
  </a>
</p>
<p align="center">
    9-10 May | Open Source in Energy Access Symposium Hackathon
</p>

---

## Validation algorithm of energy production data

**Stack:** Python (for being the predominant language in DataScience, but any other language will do as well)

**Helpful experiences:** DataSciences, Time-Series analysis, model training

**Abstract:** Validation of energy production data is an important topic in energy access. There is a lot of work or validation algorithms happening on different platforms, for example, Prospect, Odyssey, or D-REC.

Goal of this challenge is to develop, document and publish a reliable and reusable model to predict the validity of user provided energy production data.
A2EI will provide a training and test dataset. Participants will train their model on the test data set and publish validation results, like AUC etc..

**Expected outcome:** Presentation of the models performance statistics and documentation about the core features of the model.

**Getting Started:**
- Join the OSEAS24 Discord server: https://community.oseas.org/
- Introduce yourself in #introductions channel and join this topic’s channel
- Confirm you have access to the following Repos
  - https://github.com/EnAccess/oseas24-energy-production-data-validation
- For physical participants: Bring a computer (and required Adapters) for some hacking 🤖🧑‍💻
- Full details on setup are below.

Contact person(s): Brianna / Razvan

**Further information and resources:**

- https://odysseyenergysolutions.com/
- https://prospect.energy/
- https://drecs.org/


## Before We Start
The dataset that we’re working with is from meters measuring electricity usage in a set of health clinics in Sierra Leone.  You can use your own tool(s) of choice to visualize and work with the data, but to get you started, we’ve set up the data in the [hackathon_oseas](https://gitlab.com/prospect-energy/prospect-server/-/tree/hackathon_oseas?ref_type=heads) branch in the [prospect-server](https://gitlab.com/prospect-energy/prospect-server) gitlab repo.  This will allow you to visualize the data using a Prospect dashboard that we’ve already set up to look specifically at these meters.

Requirements and instructions to access the data are in the [README](https://gitlab.com/prospect-energy/prospect-server), but some requirements that would be helpful to prepare in advance are:
1. Download [Docker](https://docs.docker.com/get-docker/).
1. Clone the [prospect-server](https://gitlab.com/prospect-energy/prospect-server) repo locally.
1. Checkout the hackathon_oseas branch.  (Note that this is not yet finalized, so you’ll have to re-pull it before Thursday.)
1. Run `docker compose up` in a terminal within the repo folder to start the container.  This should allow you to access both the **Postgres** database with the hackathon data in it, and the **Prospect** interface where you can look at it more interactively.  The endpoints for both of these are described in Section 3 of the README.


## To Access Postgres
If you open your favorite SQL client, you can access the Postgres DB using the connection parameters in [Section 3](https://gitlab.com/prospect-energy/prospect-server#3-overview-about-all-endpoints) of the README:

![](jpg/01_postgres.jpg)

There are two main tables, `data_meters` and `data_meters_ts`.  Both are described in the Prospect table documentation [here](https://app.prospect.energy/docs).

