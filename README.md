# NHSE FHIR PRogrammes IG repo

This repo is the source for all FHIR assets to https://simplifier.net/nhs-england-programme-implementation-guides.

Due to validation confilcts with the programmes assets, along with read/write access for programmes it has been decided to separate each programme into their own repo. This repo is used to collate the assets and export to Simplifier.

## Connect New Programme Repo

- Create a new repo
- create the following secrets:
  - `AGGREGATOR_PAT` - personal access token with *repo: Full control of private repositories* selected, see [creating-a-personal-access-token-classic](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic)
  - `ONTO_CLIENT_ID` - your termserver id
  - `ONTO_CLIENT_SECRET` - your termserver secret
- copy and add the workflows https://github.com/ryma2fhir/FHIR_IG_PATHOLOGY_TEST/tree/main/.github/workflows
- add the repo path to https://github.com/ryma2fhir/FHIR_IG_BASE_TEST/blob/main/programme-repos.txt

## Create a New Package

- Create a bake file in Simplifier
- add only the files you need to the bake command, see [https://simplifier.net/nhs-england-programme-implementation-guides/pathology-snapshot-with-draft](pathology-snapshot-with-draft) for an example. Note: only a single `- files:` can be added in a single block, if more than one needed use multiple blocks
- test bake by pressing the green play button
- copy the yaml file to `package.bake.yaml`. This is the file used for package creation.
- For new package use `Create new package` with the package name being `fhir.r4.nhsengland.<programme>`
- To upversion an existing package use the burger bar next to the latest package and choose `create new version`

 See https://docs.fire.ly/projects/Simplifier/data_governance_and_quality_control/simplifierPackages.html#bake-pipeline for more details 
  
