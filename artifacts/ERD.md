![rowhealth-erd](https://github.com/user-attachments/assets/4e34d484-aa05-4da5-93e4-3f5b1f8ba1d9)

```
+-------------------------------------------------------------------+
| CUSTOMERS                                                         |
+-------------------------------------------------------------------+
| customer_id                                           | STRING    |
| campaign_id                                           | STRING    |
| first_name                                            | STRING    | 
| last_name                                             | STRING    | 
| state                                                 | STRING    |
| first_touch                                           | STRING    |
| plan                                                  | STRING    |
| signup_date                                           | DATE      |
+--------------------------------------------+----------------------+

+-------------------------------------------------------------------+
| CLAIMS                                                            |
+-------------------------------------------------------------------+
| claim_id                                              | INTEGER   |
| customer_id                                           | STRING    |
| claim_date                                            | DATE      |
| claim_category                                        | STRING    | 
| claim_amount                                          | FLOAT     |
| covered_amount                                        | FLOAT     |
+--------------------------------------------+----------------------+

+-------------------------------------------------------------------+
| CAMPAIGNS                                                         |
+-------------------------------------------------------------------+
| campaign_id                                           | STRING    |
| campaign_category                                     | STRING    | 
| campaign_type                                         | STRING    | 
| cost                                                  | FLOAT     | 
| impressions                                           | INTEGER   | 
| clicks                                                | INTEGER   |
+--------------------------------------------+----------------------+
```
