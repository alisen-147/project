
# Class Specification — ورکینو

## Customer
| بخش | توضیح |
|---|---|
| مسئولیت | ثبت درخواست خدمات و پیگیری آن‌ها |
| ویژگی‌ها | id, full_name, email, phone, password_hash, address, is_active |
| متدها | register(), login(), logout(), createRequest(), viewRequests(), submitReview() |
| روابط | Customer 1:N ServiceRequest، Customer 1:N Review |

## Specialist
| بخش | توضیح |
|---|---|
| مسئولیت | ارائه خدمات و مدیریت درخواست‌های دریافتی |
| ویژگی‌ها | id, full_name, email, phone, password_hash, bio, skills, service_area, estimated_rate, is_active |
| متدها | register(), login(), logout(), viewRequests(), acceptRequest(), rejectRequest(), updateProfile() |
| روابط | Specialist 1:N ServiceRequest، Specialist 1:N Review، Specialist 1:N AvailabilitySlot |

## Admin
| بخش | توضیح |
|---|---|
| مسئولیت | مدیریت کاربران و دسته‌بندی خدمات |
| ویژگی‌ها | id, full_name, email, password_hash, is_active |
| متدها | login(), logout(), manageUsers(), manageCategories(), viewStatistics() |
| روابط | مدیریت Customer، Specialist و ServiceCategory |

## ServiceCategory
| بخش | توضیح |
|---|---|
| مسئولیت | دسته‌بندی خدمات قابل ارائه |
| ویژگی‌ها | id, name, description |
| متدها | addCategory(), updateCategory(), deleteCategory() |
| روابط | ServiceCategory 1:N ServiceRequest، ارتباط N:M با Specialist |

## ServiceRequest
| بخش | توضیح |
|---|---|
| مسئولیت | نگهداری و پیگیری درخواست‌های خدمات |
| ویژگی‌ها | id, customer_id, specialist_id, category_id, description, location, budget, requested_at, status |
| متدها | assignSpecialist(), updateStatus(), cancelRequest() |
| روابط | ارتباط با Customer، Specialist و ServiceCategory؛ امکان ثبت Review |
| وضعیت‌ها | PENDING، ACCEPTED، REJECTED، COMPLETED، CANCELLED |

## Review
| بخش | توضیح |
|---|---|
| مسئولیت | ثبت امتیاز و نظر مشتری درباره متخصص |
| ویژگی‌ها | id, customer_id, specialist_id, request_id, rating, comment, created_at |
| متدها | submitReview(), updateReview() |
| روابط | ارتباط با Customer، Specialist و ServiceRequest |

## AvailabilitySlot
| بخش | توضیح |
|---|---|
| مسئولیت | ثبت زمان‌های در دسترس بودن متخصص |
| ویژگی‌ها | id, specialist_id, start_time, end_time, is_available |
| متدها | addSlot(), updateSlot(), removeSlot() |
| روابط | AvailabilitySlot N:1 Specialist |
