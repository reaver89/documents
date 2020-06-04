# Failed Requests alerts on Application Insights

## Tickets names samples

- FailedRequests-Alert-ordersnow-ecommerce
- FailedRequests-Alert-productmetadata-ue-prod
- FailedRequests-Alert-shippingserviceAI

## Alert Context

- **Monitoring service**: Platform
- **Signal Type**: Metric
- **Condition Type**: SingleResourceMultipleMetricCriteria

## Generic Alert Condition

| Alert Names | Alert Subject | Operator | Value | Aggregation | Window Size |
|:-:|:-:|:-:|:-:|:-:|:-:|
| *Generic Values* | *[[Metric Value]]* | *>=* | *[[Threshold]]* | *Count* | *PT15M* |
| FailedRequests-Alert-ordersnow-ecommerce | ~ | >= | 1 | Count | PT15M |
| FailedRequests-Alert-productmetadata-ue-prod | ~ | >= | 1 | Count | PT15M |
| FailedRequests-Alert-shippingserviceAI | ~ | >= | 1 | Count | PT15M |

## Alert's description

This alert appears when the metric value exceeds the threshold (f.e. 1) of failed requests count

## Triage

1. Navigate to the affected Application Insights overview -> **Failures**  section
2. Review failures and answer these questions:
   - Are requests still failing?
   - What is HTTP failure code?
   - What is the failing step at the E2E-transaction view

## Resolution

- Let customer always know about HTTP-5XX failures;
- Let customer know about HTTP-4XX in case of series of failures;
- Attach information from the KB about the HTTP event occurred: [KB0001-HTTP5XX](/kb/KB0001-HTTP.5XX-Codes.md) and [KB0002-HTTP4XX](/kb/KB0002-HTTP.4XX-Codes.md)

## Answer template

Ticket delegated to customer.

Please, review the affected resource to figure out the root cause of the {{ERROR_NAME}} error.
It is an HTTP response status code that indicates that {{ERROR_DESCRIPTION}}

You can find more information about this error and troubleshoot steps here: {{ERROR_TROUBLESHOOTING}}

**Example:**

---
Ticket delegated to customer.

Please, review the affected resource to figure out the root cause of the HTTP 400 (Bad request) error. It is an HTTP response status code that indicates that [[EXAMPLE OF DESCRIPTION]](/kb/KB0002-HTTP.4XX-Codes.md#400-Bad-Request)

You can find information about troubleshoot steps
[here](/kb/KB0002.1-HTTP.400-TroubleShooting.md)
