

# Class Specification — Workino

## 1. User

**Type:** Abstract Class

The base class for all system users. It stores the information shared by customers, specialists, and admins.

| Attribute | Type | Description |
|---|---|---|
| `userId` | `int` | User identifier |
| `fullName` | `string` | Full name |
| `email` | `string` | User email |
| `phone` | `string` | Phone number |
| `passwordHash` | `string` | Hashed password |
| `isActive` | `bool` | Account status |

| Operation | Description |
|---|---|
| `register()` | Registers a user |
| `login()` | Logs in to the account |
| `updateProfile()` | Updates common user information |

## 2. Customer

A customer searches for services and submits service requests.

| Attribute | Type | Description |
|---|---|---|
| `address` | `string` | Customer address |

| Operation | Description |
|---|---|
| `viewRequests()` | Views previous requests |
| `submitRequest()` | Submits a service request |
| `reviewSpecialist()` | Submits a rating and review |

**Relationships:** Inherits from `User`. A customer can submit multiple service requests and write multiple reviews.

## 3. Specialist

A specialist provides services, handles requests, and manages professional information.

| Attribute | Type | Description |
|---|---|---|
| `bio` | `string` | Specialist introduction |
| `skills` | `string` | Skills and expertise |
| `serviceArea` | `string` | Service location or area |
| `estimatedRate` | `decimal` | Estimated service rate |

| Operation | Description |
|---|---|
| `viewRequests()` | Views service requests |
| `acceptRequest()` | Accepts a request |
| `rejectRequest()` | Rejects a request |
| `updateProfile()` | Updates professional information |

**Relationships:** Inherits from `User`. A specialist can offer services in multiple categories, handle multiple requests, receive reviews, and manage availability slots.

## 4. Admin

The admin manages user accounts and service categories and monitors the system.

| Operation | Description |
|---|---|
| `manageUsers()` | Manages customer and specialist accounts |
| `manageCategories()` | Manages service categories |
| `viewStatistics()` | Views system statistics |

**Relationships:** Inherits from `User` and works with the relevant classes to manage accounts and categories.

## 5. ServiceCategory

Represents a category of services, such as repairs, cleaning, or technical services.

| Attribute | Type | Description |
|---|---|---|
| `categoryId` | `int` | Category identifier |
| `name` | `string` | Category name |
| `description` | `string` | Category description |

| Operation | Description |
|---|---|
| `addCategory()` | Adds a category |
| `updateCategory()` | Updates a category |

**Relationships:** A category can contain multiple service requests. Each request belongs to one category. A specialist can offer services in multiple categories.

## 6. ServiceRequest

Stores the details and status of a customer's service request.

| Attribute | Type | Description |
|---|---|---|
| `requestId` | `int` | Request identifier |
| `description` | `string` | Description of the required service |
| `location` | `string` | Service location |
| `budget` | `decimal` | Customer's proposed budget |
| `requestedAt` | `DateTime` | Request creation time |
| `status` | `RequestStatus` | Current request status |

| Operation | Description |
|---|---|
| `updateStatus()` | Updates the request status |
| `cancelRequest()` | Cancels the request |

**Relationships:** Each request belongs to one customer and one service category. A request can have no assigned specialist or one assigned specialist. A completed request can have one review.

## 7. Review

Stores a customer's rating and feedback about a specialist. This is an optional feature.

| Attribute | Type | Description |
|---|---|---|
| `reviewId` | `int` | Review identifier |
| `rating` | `int` | Rating given by the customer |
| `comment` | `string` | Review text |
| `createdAt` | `DateTime` | Review creation time |

| Operation | Description |
|---|---|
| `submitReview()` | Submits a review |
| `updateReview()` | Updates a review |

**Relationships:** Each review is written by one customer, belongs to one specialist, and is associated with one completed service request.

## 8. AvailabilitySlot

Stores the time periods when a specialist is available. This is an optional feature.

| Attribute | Type | Description |
|---|---|---|
| `slotId` | `int` | Time slot identifier |
| `startTime` | `DateTime` | Start time |
| `endTime` | `DateTime` | End time |
| `isAvailable` | `bool` | Availability status |

| Operation | Description |
|---|---|
| `setAvailability()` | Sets the availability status |

**Relationships:** Each availability slot belongs to one specialist. A specialist can have multiple availability slots.

## 9. RequestStatus

An enumeration used by `ServiceRequest` to represent the possible states of a request.

| Value | Description |
|---|---|
| `PENDING` | Waiting for review |
| `ACCEPTED` | Accepted by a specialist |
| `REJECTED` | Rejected by a specialist |
| `IN_PROGRESS` | Service is in progress |
| `COMPLETED` | Service is completed |
| `CANCELLED` | Request is cancelled |

`RequestStatus` is an enumeration, not a regular class.
