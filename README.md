
QuickTime Video
================================================================================

Credits
-----------------------------------------------

Developer
-----------------------------------------------
Nicolaas [at] sunnysideup.co.nz

Requirements
-----------------------------------------------
see composer.json

Documentation
-----------------------------------------------
see http://silverstripe-webdevelopment.com/flowplayer




Installation Instructions
-----------------------------------------------
1. Find out how to add modules to SS and add module as per usual.

2. Review configs and add entries to mysite/_config/config.yml
(or similar) as necessary.
In the _config/ folder of this module
you should to find some examples of config options (if any).


3. add <% include QuickTimeVideo %> to your template

4. add the following to any SiteTree class

	static $has_one = array(
		"QuickTimeVideo" => "QuickTimeVideo"
	);

	function getCMSFields() {
		$fields = parent::getCMSFields();
		$fields->addFieldToTab("Root.Content.Movie", new FileIFrameField("QuickTimeVideo", "Quick Time Video"));
		return $fields;
	}



