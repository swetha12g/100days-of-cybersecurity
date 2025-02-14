# 🌐 HTTP Status Codes

HTTP status codes are issued by a server in response to a client’s request. They indicate whether the request was successful, redirected, or encountered an error.

![image](https://github.com/user-attachments/assets/9a56def4-167d-4081-92c0-e6c1e8be63f2)


## ⚡ Common HTTP Status Code Categories

| Status Code | Category       | Description                                        |
|------------|---------------|----------------------------------------------------|
| **1xx**    | Informational  | Request received, processing continues.          |
| **2xx**    | Success        | Request successfully processed.                   |
| **3xx**    | Redirection    | Further action needed to complete the request.   |
| **4xx**    | Client Errors  | Request contains bad syntax or cannot be fulfilled. |
| **5xx**    | Server Errors  | The server failed to process a valid request.    |

---

## 🔍 Detailed HTTP Status Codes

### ✅ **Success (2xx)**
| Code  | Meaning               | Description |
|-------|-----------------------|-------------|
| **200** | OK                    | Request succeeded, and the server responded with the requested data. |
| **201** | Created               | Request was successful, and a resource was created. |
| **204** | No Content            | Request was successful, but there is no content to return. |

---

### 🔀 **Redirection (3xx)**
| Code  | Meaning               | Description |
|-------|-----------------------|-------------|
| **301** | Moved Permanently     | The resource has been permanently moved to a new URL. |
| **302** | Found (Temporary)     | The resource has been temporarily moved to a different URL. |
| **304** | Not Modified          | The resource has not changed since the last request. |

---

### ⚠️ **Client Errors (4xx)**
| Code  | Meaning               | Description |
|-------|-----------------------|-------------|
| **400** | Bad Request           | The request was invalid or cannot be processed. |
| **401** | Unauthorized          | Authentication is required but missing or invalid. |
| **403** | Forbidden             | The request is understood, but the server refuses to fulfill it. |
| **404** | Not Found             | The requested resource does not exist. |

---

### 🚨 **Server Errors (5xx)**
| Code  | Meaning               | Description |
|-------|-----------------------|-------------|
| **500** | Internal Server Error | The server encountered an unexpected condition. |
| **502** | Bad Gateway           | The server received an invalid response from an upstream server. |
| **503** | Service Unavailable   | The server is overloaded or under maintenance. |
| **504** | Gateway Timeout       | The server did not receive a timely response from an upstream server. |

---

## 🚀 Conclusion

Understanding HTTP status codes is crucial for debugging, optimizing web applications, and improving user experience.

### 🔹 Want to test HTTP status codes? Try:
- [Postman](https://www.postman.com/) – API testing tool  
- [cURL](https://curl.se/) – Command-line HTTP requests  

### 🔗 References
- [MDN – HTTP Status Codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)  
- [RFC 7231 – HTTP/1.1 Status Code Definitions](https://datatracker.ietf.org/doc/html/rfc7231)  
