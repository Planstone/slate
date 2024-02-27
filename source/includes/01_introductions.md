# Introduction

This is the Planstone Events API. You can use our API to access your Events in Planstone, which can get information on Sessions, Speakers, Abstracts, Posters, and Disclosures.

## Overview
- The API uses HTTP Basic Authentication

- You are expected to pull this data into your infrastructure and serve it to the end consumer/user.  

- SPA / Ajax access to the API is not allowed.

- Your API access is global to your account, so this data should be transformed and sanitized for your specific use case and access controlled where necessary.

- Your level of access to the API will be contingent on your contract with Planstone.

- The Planstone Events API updates every 15 minutes from production data; there are no mechanisms to filter, review, or otherwise block data to the API.

- The API is read-only.

- The number of fields that the API contains may change based on the event.  Specifically, there may be Custom Fields, Tracks, Groups, and Credits for different events.  These objects are discoverable and iterable. 

- For resources/assets (handout files, audio files, video files, posters), you are expected to host these files and not link back to the Planstone Infrastructure within your application.  

- The API results are paginated.  Each call will return up to 100 results.  If there are more results, the API will state how many pages of data there are in the result.  It’s the caller's responsibility to iterate over the number of pages.

- This is important for any API consumer.

- The API can return either XML or JSON results.  You tell the API this is based on the Accept HTTP header.

- Planstone can provision accounts for your other vendors to pull directly from Planstone.  By granting access to their data to another vendor, the client assumes they have permission to do so.  (re: Any privacy laws regarding PII, ex: GDPR )

- Example - Mobile App to prime the app with sessions, speakers, handouts

- Example - AV Company to prime presentation system for sessions, speakers, handouts - and to link directly to presentation system from Planstone

- Example - Marketing Website to publish event details

- Example - Registration to pull and sync sessions and speakers

