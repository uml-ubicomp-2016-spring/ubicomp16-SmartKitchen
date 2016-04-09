# SmartKitchen
A Kitchen application made to make remembering what is in your kitchen simpler. No more remembering whether or not you need to buy
milk or if the milk expired. You can scan the barcode on your milk, when you bought it, set the inventory using the simple web application,
and open the application at the grocery store to know if you need milk or not.

# Contributors
Harrison Kelly, Brian Day, AjayKumar Sarikonda

# Progress (Week 3/28)

* Harrison Kelly
    * Fixed a UI caching issue and stubbed out the async calls for the new REST api. Also
    made a slight modification to the REST api and connected the /getLatestInventory/ call.
    * Got rid of the unused icons and changed the ordering of the Latest Inventory so that
    it was actually the latest and not the first three items, also changed the ordering of the Inventory
    to show the latest at the top.
    * Made the REST API pep8 compliant.
    * Added localization support to the REST api to make it simpler to change languages.
    * Added utility methods for the REST api to keep the file clean.
    * Wrote the "addInventory" REST call.
    * Turned on refreshing on the UI and made sure that it worked with the "addInventory" REST call, also connected
    other calls and enabled "deleting" (when the REST call is completed).
    * Connected the three different health status REST calls.
    * Added localized i18n messages and support for: English, French, and Spanish.
    * Fixed issue with alerts circle not being clickable.
    * Added a popup for editing the inventory items (not fully implemented) and began working on the styling for the main
    inventory container.
    * Added a default "expiration date" when an item is added to the inventory so that it isn't blank by default. Also fixed
    a reload issue where there were duplicates and ng-repeat did not like it.

* Brian Day
    * Started from scratch on scanner part of project it is now correctly threaded. Using zbarimg directly now
    and piping its output into our code. Scanner is also connected to the rest api, scanner health POST's to the
    rest api for now, may change
    * Scanner more flushed out, processes and threads die correctly when exited

* Ajay
    * Working on addInventory and setExpiration methods in REST API where i am getting more errors

# Progress (Week 4/04)

* Harrison Kelly
    * Fixed an issue of CORS not allowing us to make a rest call from :8000 to :5000.
    * Fixed an issue of Safari not liking the use of "const" and wouldn't display the page.
    * Fixed an issue where the inventory controller was being loaded multiple times.
    * Added missing function comments and alerts.
    * Updated cached items with possibly new expiration dates.
    * Connected the "edit" button with a popup that allows users to change the expiration date. The REST call is connected, just
    waiting for it to be written.
    * Fixed the latest refresh date to show the actual refresh date/time.
