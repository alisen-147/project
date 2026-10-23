
# Class Diagram — ورکینو

## ۱. مقدمه

این دیاگرام کلاس‌های اصلی سیستم ورکینو، ویژگی‌های آن‌ها و روابط بین آن‌ها را نشان می‌دهد.

## ۲. کلاس‌ها

### ۲.۱ User
| ویژگی | نوع |
|---|---|
| id | int |
| full_name | string |
| email | string |
| phone | string |
| password_hash | string |
| is_active | bool |

### ۲.۲ Customer
| ویژگی | نوع |
|---|---|
| address | string |

### ۲.۳ Specialist
| ویژگی | نوع |
|---|---|
| bio | string |
| skills | string |
| service_area | string |
| estimated_rate | decimal |

### ۲.۴ Admin

ویژگی‌های این کلاس از کلاس `User` به ارث می‌رسند.

### ۲.۵ ServiceCategory
| ویژگی | نوع |
|---|---|
| id | int |
| name | string |
| description | string |

### ۲.۶ ServiceRequest
| ویژگی | نوع |
|---|---|
| id | int |
| customer_id | int |
| specialist_id | int |
| category_id | int |
| description | string |
| location | string |
| budget | decimal |
| requested_at | datetime |
| status | RequestStatus |

### ۲.۷ Review
| ویژگی | نوع |
|---|---|
| id | int |
| customer_id | int |
| specialist_id | int |
| request_id | int |
| rating | int |
| comment | string |
| created_at | datetime |

### ۲.۸ AvailabilitySlot
| ویژگی | نوع |
|---|---|
| id | int |
| specialist_id | int |
| start_time | datetime |
| end_time | datetime |
| is_available | bool |

### ۲.۹ RequestStatus (enum)
| مقدار | توضیح |
|---|---|
| PENDING | در انتظار پاسخ متخصص |
| ACCEPTED | پذیرفته‌شده |
| REJECTED | ردشده |
| COMPLETED | تکمیل‌شده |
| CANCELLED | لغوشده |

## ۳. روابط

- `User` ← `Customer` (ارث‌بری)
- `User` ← `Specialist` (ارث‌بری)
- `User` ← `Admin` (ارث‌بری)
- `Customer 1:N ServiceRequest`
- `Specialist 1:N ServiceRequest`
- `ServiceCategory 1:N ServiceRequest`
- `Customer 1:N Review`
- `Specialist 1:N Review`
- `ServiceRequest 1:0..1 Review`
- `Specialist 1:N AvailabilitySlot`
- `Specialist N:M ServiceCategory`

نکته: `specialist_id` در درخواست می‌تواند خالی باشد؛ چون درخواست ممکن است هنوز به متخصصی تخصیص داده نشده باشد. `RequestStatus` نیز یک `enum` است، نه یک کلاس معمولی.
