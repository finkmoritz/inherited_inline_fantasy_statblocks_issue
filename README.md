# Overview

This project reproduces a bug with the Fantasy Statblock plugin when using inherited inline statblocks.

# Setup

Install & enable the Fantasy Statblocks plugin and enable the setting "Automatically Parse Frontmatter for Creatures".

# Issue

[[Inline Human John Doe]] inherits from [[Inline Human]] which in turn inherits from Commoner. Both files contain the file property "statblock: inline".
While [[Inline Human]] contains all attributes of a Commoner and defines its type as "Human", the [[Inline Human John Doe]] contains only the type "Human".

# Expected Behaviour

[[Inline Human John Doe]] is expected to contain all attributes of Commoner **and** [[Inline Human]].

The desired outcome can already be achieved by not using the file property "statblock: inline" and manually clicking "Save to Bestiary" on the [[Human]]. In this case, [[Human John Doe]] does indeed contain all attributes of [[Human]] and a Commoner.