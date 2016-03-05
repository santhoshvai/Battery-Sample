# Battery-Sample

* Understanding battery drain
  * Used `batteryHistorian` to understand battery drain of the sample app
  * We can apply filter while charging to conserve battery, this was done in the activity.

* Wake Lock and Battery Drain || Remedy by Job Scheduler
  * Holding on the `wakeLock` for too long, we can drain the battery easily. Manual releasing also makes its usage tedious.
  * `jobScheduler API` makes the systen defer your wakelock task at appropriate situations with collectively other wakelocks
    *  `jobInfo` object and `service` needs to be created.
    * see the [DevBytes video](https://www.youtube.com/watch?v=QdINLG5QrJc&feature=youtu.be)

* Minimise cellularRadio usage || wait for WiFi
  * use `jobScheduler API` to defer tasks to only when WiFi is connected.
