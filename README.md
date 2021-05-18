# oauth2




1. curl -X POST -vu clientapp:123456 http://localhost:9096/oauth/token -H "Accept: application/json" -d "password=spring&username=admin&grant_type=password&scope=read%20write&client_secret=123456&client_id=clientapp"

 {"access_token":"bfd4fa85-43ae-45bf-8207-cfe7985f8840","token_type":"bearer","refresh_token":"4ac10b93-e1f5-4892-897d-a56d67993e66","expires_in":43199,"scope":"read write"}* Connection #0 to host localhost left intact
 
 2. curl http://localhost:9096/greeting -H "Authorization: Bearer ff16372e-38a7-4e29-88c2-1fb92897f558"
 
 
# username & password
1. curl -X POST -vu clientapp:123456 http://localhost:9097/oauth/token -H "Accept: application/json" -d "password=password&username=usergmail&grant_type=password&scope=read%20write&client_secret=123456&client_id=clientapp"

{"access_token":"e2706fe5-e914-4c1c-8699-2dd0e3aae2a6","token_type":"bearer","refresh_token":"609e8cd3-d6ca-4ced-8eec-0464b47137f9","expires_in":43199,"scope":"read write"}* Connection #0 to host localhost left intact

#refresh token
2. curl -X POST -vu clientapp:123456 http://localhost:9097/oauth/token -H "Accept: application/json" -d "grant_type=refresh_token&refresh_token=8da300f6-8f57-427f-b828-de7c50bb41b2&client_secret=123456&client_id=clientapp"

{"access_token":"299ef40c-e79d-48cb-a3b4-c7b90436884d","token_type":"bearer","refresh_token":"99294e25-ed57-4537-b9ba-d25a7c581c40","expires_in":43199,"scope":"read write"}* Connection #0 to host localhost left intact
