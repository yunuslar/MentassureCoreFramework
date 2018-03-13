# MentassureCore Framework in Swift
MentassureCore Framework V3.2

##  User
Authenticated users should be added to Mentassure by this class. Also their friends can be added to Mentassure. Implement UserDelegate in your application to be notified when user is added, friend is added and leadership is got.

AddUser:
This method adds users  to Mentassure. Authentication is left to the application but each authenticated user should be added via this method.

AddFriend:
Inorder to get Leadership list among friends, each friend should be added by this method.

getLeadership:
You can get Leadership list among Country, City and Friends.

## DrivingInsight
This class performs trip tracking and driver scoring actions.
Each application should have only one LocationManager and MotionManager. Declare and set those global managers to drivingInsight class before the first usage.
Before using this class init it as follows:

drivingInsight.LocationManager = CLLocationManager()
drivingInsight.MotionManager = CMMotionManager()
drivingInsight.UserID = _userID

startTrip:
Starts a trip and records location and motion data.

stopTrip:
Stops the trip. Implement DrivingInsightDelegate in your application to be notified after trip finished successfully or trip failed for a reason.

CurrentTrip:
In your application you can use the current trip data by this property.

LastTrip:
In your application you can use the last trip data by this property.

getSummaryData:
You can get the summary data for all the trips for a user. Implement DrivingInsightDelegate in your application to be notified when summary data is ready.

getTripHistory:
Get all the history of the trips for the user given. Implement HistoryDataDelegate in your application to be notified when history data is ready.





