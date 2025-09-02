# API Documentation
"name": "Jane Doe",
"email": "jane@example.com"
}
```


---


### 3.3 Update User Information
**Endpoint:**
```
PUT /users/{id}
```


**Description:** Updates details of an existing user.


**Request Body:**
```json
{
"name": "Jane Smith"
}
```


**Response:**
```json
{
"id": 102,
"name": "Jane Smith",
"email": "jane@example.com"
}
```


---


### 3.4 Delete a User
**Endpoint:**
```
DELETE /users/{id}
```


**Description:** Deletes a user by ID.


**Response:**
```json
{
"message": "User deleted successfully"
}
```


---


## 4. Error Codes
| Code | Message | Description |
|------|---------|-------------|
| 400 | Bad Request | Invalid input data |
| 401 | Unauthorized | Missing or invalid API key |
| 404 | Not Found | User not found |
| 500 | Server Error | An unexpected error occurred |


---


## 5. Examples


### Example: cURL Request
```bash
curl -X GET "https://api.example.com/v1/users/101" \
-H "Authorization: Bearer <your_api_key>"
```


### Example: JavaScript (fetch)
```javascript
fetch("https://api.example.com/v1/users/101", {
headers: {
Authorization: "Bearer <your_api_key>"
}
})
.then(res => res.json())
.then(data => console.log(data));
```


---


**End of Document**
