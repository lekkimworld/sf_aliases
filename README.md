# sf_aliases
Simple bash aliases to retrieve info from status.salesforce.com

# Installation
1. Clone the repository onto disk e.g. into `sf_aliases`
2. Edit your `.bash_profile` to source the `sf_functions` file
3. Restart your Terminal or source `.bash_profile`

## Example .bash_profile
\# salesforce functions
source ~/sf_aliases/sf_functions

# Requirements
The functionality uses the jq JSON parser at https://stedolan.github.io/jq/

# Examples
`$ sf_help
Salesforce CLI actions:
-----------------------
- sf_status
  Shows status for instance ID
  Syntax : sf_status 
  Example: sf_status na44

- sf_release
  Shows release version of supplied instance ID
  Syntax: sf_release 
  Example: sf_release na44

- sf_instance
  Get instance ID from hostname
  Syntax: sf_instance 
  Example: sf_instance org62.lightning.force.com

- sf_status_raw
  Shows raw JSON
  Syntax: sf_status_raw

------------------------
$ sf_instance na44.salesforce.com
na44
$ sf_instance lekkim-trailhead-dev-ed.my.salesforce.com
eu11
$ sf_release eu11
Winter '17 Patch 18.10
$ sf_release na44
Spring '17 Patch 5.5
$ sf_status eu11
Release Version : Winter '17 Patch 18.10
Active          : true
Status          : OK
Environment     : production
$ sf_status cs85
Release Version : Spring '17 Patch 6
Active          : true
Status          : OK
Environment     : sandbox
$ sf_instance lekkim-trailhead-dev-ed.my.salesforce.com | sf_release
Winter '17 Patch 18.10
$ sf_instance lekkim-trailhead-dev-ed.my.salesforce.com | sf_status
Release Version : Winter '17 Patch 18.10
Active          : true
Status          : OK
Environment     : production`
