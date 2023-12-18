# iNaturalist Australia - taxon status updates

Taxa in iNaturalist have statuses and obfuscation levels that can be set for regions that the ALA is responsible for maintaining in Australia. Bulk loads can be submitted to iNaturalist in December/January using these [templates and checklists](https://docs.google.com/spreadsheets/d/1yTwWh4d-lHeaBGCB9m70-HKEMtvrquHsPu3Zrgz9BcE/edit#gid=1531097917)

Current statuses per iNaturalist taxonID are available in the iNaturalist site export, accessible via an iNaturalist AU site admin(inaturalist-australia-9-conservation_statuses.xls).

**Steps:**
1. Extract all the current statuses in Australian jurisdictions in the export (eg.AU or Australia place, .gov.au in the URL or user 708886)
2. Resolve the taxon name for each using the iNaturalist Taxon DwCA at https://www.inaturalist.org/taxa/inaturalist-taxonomy.dwca.zip (~350MB) or the iNat taxon API (if the taxon is inactive in iNaturalist). File output: `inat-aust-status-taxa.csv` containing Australian conservation statuses
3. State by state establish the changes that need to be made:
   * **new** - any new species that appear in the state lists but do not have a status in inaturalist (ADD)
   * **updates** - any changes to statuses (update template, action='UPDATE')
   * **removals** - any statuses which were added by us previously (user_id = 708886) list which are incorrect (update template, action='REMOVE')
   * **flags** - check for statuses by other users that need to be flagged