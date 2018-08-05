# Errors

CORE returns the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- You screwed up.
401 | Unauthorized -- Your JWT has expired or been revoked.
403 | Forbidden -- You dont have the access rquired to do the thing
404 | Not Found -- Probably a typo or incorrect request method.
418 | I'm a teapot -- You shouldn't brew coffee in a teapot.
500 | Internal Server Error -- We screwed up. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
