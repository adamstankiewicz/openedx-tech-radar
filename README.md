# Open edX Tech Radar

The [Open edX Tech Radar Visualization](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fopenedx.github.io%2Fopenedx-tech-radar%2Fopen-edx-primary-radar.csv) is generated by code hosted in here in [https://github.com/openedx/openedx-tech-radar](https://github.com/openedx/openedx-tech-radar). The assets used for the visualization are [published to Github Pages](https://openedx.github.io/openedx-tech-radar/) for consumption by Thoughtworks' service.

## Why?

A technology radar serves as a reference and an onboarding tool for the technologies
used in the Open edX Platform, giving us all deeper insight into the composition and
history of the software which we collectively steward.  It’s a living document that
records our technology decisions as they change over time, evaluating their level of
adoption and suitability to the platform’s needs.

Today we don’t have a “one-stop shop” for this sort of information, and often teams
and individuals are left to reinvent the wheel when making technology choices.  We
hope that creating a comprehensive Technology Radar for Open edX will save engineers
time and make our code more approachable to each other through consistency of approach
and implementation.

Creating a technology radar involves gathering information from all corners of the
engineering organization, so it only makes sense to do this in a collaborative way.

[See Thoughtworks Tech Radar FAQ for more information](https://www.thoughtworks.com/radar/faq), as
well as this [Open edX Tech Radar document](https://openedx.atlassian.net/wiki/spaces/AC/pages/2844786770/Open+edX+Technology+Radar).

This repo holds individual JSON files describing the Open edX Primary Tech Radar, created
collaboratively by the community in [the original Tech Radar workshop spreadsheet](https://docs.google.com/spreadsheets/d/1ntg2fy7EBR0TFGktyORyv3W-K1bOmhr5Z4EU6WzdSWE/edit#gid=0).

Building a radar from a Google sheet requires users to sign in to Google and give Thoughtworks read access
to their Google docs. Publishing a CSV from this repo allows us to bypass this, and moving forward will
give us the ability to make changes to the Radar in a trackable manner.

## How?

This repository includes a few scripts for translating CSV radar definitions into JSON and back
again. The build for this repository takes the JSON files in the `radars` sub-directory and
combines them into CSV files for each radar that's checked in (currently only the "primary" radar)

This CSV is then published to the web, where it can be picked up by https://radar.thoughtworks.com
and turned into a Tech Radar on the fly.

See the README in `scripts` for more details.
