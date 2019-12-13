# Swagger-OAS

### Swagger OAS Document Repository
** excludes any secOps information

User-hub:

12/12
Built component schemas for Users and Applications. 
Still having errors with user and app id in certain parameters. \
  **v1: Basic structure**
  
#### User / Users
  * getUsers
  * getUserById
  * createUser
  * updateUserById
  * deleteUserById

#### App
  * getApps
  * getAppbyId
  * createApp
  * updateAppbyId
  * deleteAppById
	
---
12/13
**Updated:** 
* Components: refactored and added several
* Moved parameters to path level 
*  Created:
	* getUserApps
	  * path: `user/{userId}/apps`
		* a user’s list of apps 1:m
		* `PUT` users app list
		* `POST` to users app list
		* `DELETE` from users app list
	* getUserOneApp
		* `user/{userId}/apps/{appId}`
		* from the user’s app list specific details on a single application
		* `-PUT-` immutable by user only for prefences
		* ??? `DELETE` user from app : remove `userId` from `AppId` may nee
  * getAppUsers
		* `apps/{appId}/users`
		* an app’s list of users 1:m
		- `POST` user to an app
		- `DELETE` user from an app
		- `GET` user from an app
	* getAppOneUser
		* `apps/{appId}/users/{userId}`
		* from the app’s list of users select a specific user (for reverse 		mapping relationships if in RDBM
Generated `KTOR Project` from `Swagger` doc and placed it in its own repository. 

---
