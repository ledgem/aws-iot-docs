# AWS IoT Core Developer Guide

-----
*****Copyright &copy; Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What is AWS IoT?](what-is-aws-iot.md)
   + [What AWS IoT can do](aws-iot-solutions.md)
   + [How AWS IoT works](aws-iot-how-it-works.md)
   + [Learn more about AWS IoT](aws-iot-learn-more.md)
   + [What's new in the AWS IoT console](whats-new-in-console.md)
+ [Getting started with AWS IoT Core](iot-gs.md)
   + [Set up your AWS account](setting-up.md)
   + [Try the AWS IoT Core interactive tutorial](interactive-demo.md)
   + [Try the AWS IoT quick connect](iot-quick-start.md)
      + [Testing connectivity with your device data endpoint](iot-quick-start-test-connection.md)
   + [Explore AWS IoT Core services in hands-on tutorial](iot-gs-first-thing.md)
      + [Create AWS IoT resources](create-iot-resources.md)
      + [Configure your device](configure-device.md)
         + [Create a virtual device with Amazon EC2](creating-a-virtual-thing.md)
         + [Use your Windows or Linux PC or Mac as an AWS IoT device](using-laptop-as-device.md)
         + [Connect a Raspberry Pi or another device](connecting-to-existing-device.md)
         + [Troubleshooting problems with the sample app](gs-device-troubleshoot.md)
   + [View MQTT messages with the AWS IoT MQTT client](view-mqtt-messages.md)
+ [Connecting to AWS IoT Core](connect-to-iot.md)
   + [Connecting to AWS IoT Core service endpoints](iot-connect-service.md)
   + [Connecting devices to AWS IoT](iot-connect-devices.md)
      + [Device communication protocols](protocols.md)
         + [MQTT](mqtt.md)
         + [HTTPS](http.md)
      + [MQTT topics](topics.md)
         + [MQTT message payload](topicdata.md)
         + [Reserved topics](reserved-topics.md)
      + [Configurable endpoints](iot-custom-endpoints-configurable.md)
         + [Creating and configuring AWS-managed domains](iot-custom-endpoints-configurable-aws.md)
         + [Creating and configuring custom domains](iot-custom-endpoints-configurable-custom.md)
         + [Managing domain configurations](iot-custom-endpoints-managing.md)
   + [Connecting to AWS IoT FIPS endpoints](iot-connect-fips.md)
+ [AWS IoT tutorials](iot-tutorials.md)
   + [Building demos with the AWS IoT Device Client](iot-tutorials-dc-intro.md)
      + [Tutorial: Preparing your devices for the AWS IoT Device Client](iot-dc-prepare-device.md)
         + [Step 1: Install and update the device's operating system](iot-dc-prepare-device-sys.md)
         + [Step 2: Install and verify required software on your device](iot-dc-prepare-device-sw.md)
         + [Step 3: Test your device and save the Amazon CA cert](iot-dc-prepare-device-test.md)
      + [Tutorial: Installing and configuring the AWS IoT Device Client](iot-dc-install-dc.md)
         + [Step 1: Download and save the AWS IoT Device Client](iot-dc-install-download.md)
         + [(Optional) Save the microSD card image](iot-dc-install-dc-save.md)
         + [Step 2: Provision your Raspberry Pi in AWS IoT](iot-dc-install-provision.md)
         + [Step 3: Configure the AWS IoT Device Client to test connectivity](iot-dc-install-configure.md)
      + [Tutorial: Demonstrate MQTT message communication with the AWS IoT Device Client](iot-dc-testconn.md)
         + [Step 1: Prepare the Raspberry Pi to demonstrate MQTT message communication](iot-dc-testconn-provision.md)
         + [Step 2: Demonstrate publishing messages with the AWS IoT Device Client](iot-dc-testconn-publish.md)
         + [Step 3: Demonstrate subscribing to messages with the AWS IoT Device Client](iot-dc-testconn-subscribe.md)
      + [Tutorial: Demonstrate remote actions (jobs) with the AWS IoT Device Client](iot-dc-runjobs.md)
         + [Step 1: Prepare the Raspberry Pi to run jobs](iot-dc-runjobs-prepare.md)
         + [Step 2: Create and run the job in AWS IoT](iot-dc-runjobs-prepare-define.md)
      + [Tutorial: Cleaning up after running the AWS IoT Device Client tutorials](iot-dc-cleanup.md)
   + [Building solutions with the AWS IoT Device SDKs](iot-tutorials-sdk-intro.md)
      + [Tutorial: Connecting a device to AWS IoT Core by using the AWS IoT Device SDK](sdk-tutorials.md)
         + [Tutorial: Using the AWS IoT Device SDK for Embedded C](iot-embedded-c-sdk.md)
      + [Creating AWS IoT rules to route device data to other services](iot-rules-tutorial.md)
         + [Tutorial: Republishing an MQTT message](iot-repub-rule.md)
         + [Tutorial: Sending an Amazon SNS notification](iot-sns-rule.md)
         + [Tutorial: Storing device data in a DynamoDB table](iot-ddb-rule.md)
         + [Tutorial: Formatting a notification by using an AWS Lambda function](iot-lambda-rule.md)
      + [Retaining device state while the device is offline with Device Shadows](iot-shadows-tutorial.md)
         + [Tutorial: Preparing your Raspberry Pi to run the shadow application](create-resources-shadow.md)
         + [Tutorial: Provisioning your device in AWS IoT](shadow-provision-cloud.md)
         + [Tutorial: Installing the Device SDK and running the sample application for Device Shadows](lightbulb-shadow-application.md)
         + [Tutorial: Interacting with Device Shadow using the sample app and the MQTT test client](interact-lights-device-shadows.md)
      + [Tutorial: Creating a custom authorizer for AWS IoT Core](custom-auth-tutorial.md)
      + [Tutorial: Monitoring soil moisture with AWS IoT and Raspberry Pi](iot-moisture-tutorial.md)
         + [Setting up AWS IoT](iot-moisture-setup.md)
            + [Step 1: Create the AWS IoT policy](iot-moisture-policy.md)
            + [Step 2: Create the AWS IoT thing, certificate, and private key](iot-moisture-create-thing.md)
            + [Step 3: Create an Amazon SNS topic and subscription](iot-moisture-create-sns-topic.md)
            + [Step 4: Create an AWS IoT rule to send an email](iot-moisture-create-rule.md)
         + [Setting up your Raspberry Pi and moisture sensor](iot-moisture-raspi-setup.md)
+ [Managing devices with AWS IoT](iot-thing-management.md)
   + [How to manage things with the registry](thing-registry.md)
   + [Thing types](thing-types.md)
   + [Static thing groups](thing-groups.md)
   + [Dynamic thing groups](dynamic-thing-groups.md)
+ [Tagging your AWS IoT resources](tagging-iot.md)
   + [Using tags with IAM policies](tagging-iot-iam.md)
   + [Billing groups](tagging-iot-billing-groups.md)
+ [Security in AWS IoT](security.md)
   + [AWS IoT security](iot-security.md)
   + [Authentication](authentication.md)
      + [Server authentication](server-authentication.md)
      + [Client authentication](client-authentication.md)
         + [X.509 client certificates](x509-client-certs.md)
            + [Create AWS IoT client certificates](device-certs-create.md)
            + [Create your own client certificates](device-certs-your-own.md)
               + [Manage your CA certificates](manage-your-CA-certs.md)
                  + [Create a CA certificate](create-your-CA-cert.md)
                  + [Register your CA certificate](register-CA-cert.md)
                     + [Create a CA verification certificate to register the CA certificate in the console](create-CA-verification-cert.md)
                  + [Deactivate a CA certificate](deactivate-ca-cert.md)
               + [Create a client certificate using your CA certificate](create-device-cert.md)
            + [Register a client certificate](register-device-cert.md)
               + [Register a client certificate manually](manual-cert-registration.md)
               + [Register a client certificate when the client connects to AWS IoT just-in-time registration (JITR)](auto-register-device-cert.md)
            + [Activate or deactivate a client certificate](activate-or-deactivate-device-cert.md)
            + [Attach a thing or policy to a client certificate](attach-to-cert.md)
            + [Revoke a client certificate](revoke-ca-cert.md)
            + [Transfer a certificate to another account](transfer-cert.md)
         + [IAM users, groups, and roles](iam-users-groups-roles.md)
         + [Amazon Cognito identities](cognito-identities.md)
      + [Custom authentication](custom-authentication.md)
         + [Understanding the custom authentication workflow](custom-authorizer.md)
         + [Creating and managing custom authorizers](config-custom-auth.md)
         + [Connecting to AWS IoT Core by using custom authentication](custom-auth.md)
         + [Troubleshooting your authorizers](custom-auth-troubleshooting.md)
   + [Authorization](iot-authorization.md)
      + [AWS IoT Core policies](iot-policies.md)
         + [AWS IoT Core policy actions](iot-policy-actions.md)
         + [AWS IoT Core action resources](iot-action-resources.md)
         + [AWS IoT Core policy variables](iot-policy-variables.md)
            + [Basic AWS IoT Core policy variables](basic-policy-variables.md)
            + [Thing policy variables](thing-policy-variables.md)
            + [X.509 Certificate AWS IoT Core policy variables](cert-policy-variables.md)
         + [Cross-service confused deputy prevention](cross-service-confused-deputy-prevention.md)
         + [AWS IoT Core policy examples](example-iot-policies.md)
            + [Connect policy examples](connect-policy.md)
            + [Publish/Subscribe policy examples](pub-sub-policy.md)
            + [Connect and publish policy examples](connect-and-pub.md)
            + [Retained message policy examples](retained-message-policy-examples.md)
            + [Certificate policy examples](certificate-policy-examples.md)
            + [Thing policy examples](thing-policy-examples.md)
            + [Basic job policy example](basic-jobs-example.md)
         + [Authorization with Amazon Cognito identities](cog-iot-policies.md)
      + [Authorizing direct calls to AWS services using AWS IoT Core credential provider](authorizing-direct-aws.md)
      + [Cross account access with IAM](cross-account-access.md)
   + [Data protection in AWS IoT Core](data-protection.md)
      + [Transport security in AWS IoT](transport-security.md)
      + [Data encryption in AWS IoT](data-encryption.md)
         + [Key management in AWS IoT](key-management.md)
   + [Identity and access management for AWS IoT](security-iam.md)
      + [How AWS IoT works with IAM](security_iam_service-with-iam.md)
      + [AWS IoT identity-based policy examples](security_iam_id-based-policy-examples.md)
      + [AWS managed policies for AWS IoT](security-iam-awsmanpol.md)
      + [Troubleshooting AWS IoT identity and access](security_iam_troubleshoot.md)
   + [Logging and Monitoring](security-logging.md)
   + [Compliance validation for AWS IoT Core](compliance.md)
   + [Resilience in AWS IoT Core](disaster-recovery-resiliency.md)
   + [Using AWS IoT Core with interface VPC endpoints](IoTCore-VPC.md)
   + [Infrastructure security in AWS IoT](infrastructure-security.md)
   + [Security monitoring of production fleets or devices with AWS IoT Core](security-monitoring.md)
   + [Security best practices in AWS IoT Core](security-best-practices.md)
+ [Monitoring AWS IoT](monitoring_overview.md)
   + [Configure AWS IoT logging](configure-logging.md)
   + [Monitor AWS IoT alarms and metrics using Amazon CloudWatch](monitoring-cloudwatch.md)
      + [Creating CloudWatch alarms to monitor AWS IoT](creating_alarms.md)
      + [AWS IoT metrics and dimensions](metrics_dimensions.md)
   + [Monitor AWS IoT using CloudWatch Logs](cloud-watch-logs.md)
      + [CloudWatch AWS IoT log entries](cwl-format.md)
   + [Log AWS IoT API calls using AWS CloudTrail](iot-using-cloudtrail.md)
+ [Rules for AWS IoT](iot-rules.md)
   + [Granting an AWS IoT rule the access it requires](iot-create-role.md)
   + [Pass role permissions](pass-role.md)
   + [Creating an AWS IoT rule](iot-create-rule.md)
   + [Viewing your rules](iot-view-rules.md)
   + [Deleting a rule](iot-delete-rule.md)
   + [AWS IoT rule actions](iot-rule-actions.md)
      + [Apache Kafka](apache-kafka-rule-action.md)
         + [Virtual private cloud (VPC) destinations](vpc-rule-action.md)
      + [CloudWatch alarms](cloudwatch-alarms-rule-action.md)
      + [CloudWatch Logs](cloudwatch-logs-rule-action.md)
      + [CloudWatch metrics](cloudwatch-metrics-rule-action.md)
      + [DynamoDB](dynamodb-rule-action.md)
      + [DynamoDBv2](dynamodb-v2-rule-action.md)
      + [Elasticsearch](elasticsearch-rule-action.md)
      + [HTTP](https-rule-action.md)
         + [Working with HTTP topic rule destinations](rule-destination.md)
            + [Certificate authorities supported by HTTPS endpoints in topic rule destinations](topic-rule-destination-ca-list.md)
      + [IoT Analytics](iotanalytics-rule-action.md)
      + [IoT Events](iotevents-rule-action.md)
      + [IoT SiteWise](iotsitewise-rule-action.md)
      + [Kinesis Data Firehose](kinesis-firehose-rule-action.md)
      + [Kinesis Data Streams](kinesis-rule-action.md)
      + [Lambda](lambda-rule-action.md)
      + [OpenSearch](opensearch-rule-action.md)
      + [Republish](republish-rule-action.md)
      + [S3](s3-rule-action.md)
      + [Salesforce IoT](salesforce-iot-rule-action.md)
      + [SNS](sns-rule-action.md)
      + [SQS](sqs-rule-action.md)
      + [Step Functions](stepfunctions-rule-action.md)
      + [Timestream](timestream-rule-action.md)
   + [Accessing cross-account resources using AWS IoT rules](accessing-cross-account-resources-using-rules.md)
   + [Error handling (error action)](rule-error-handling.md)
   + [Reducing messaging costs with Basic Ingest](iot-basic-ingest.md)
   + [AWS IoT SQL reference](iot-sql-reference.md)
      + [SELECT clause](iot-sql-select.md)
      + [FROM clause](iot-sql-from.md)
      + [WHERE clause](iot-sql-where.md)
      + [Data types](iot-sql-data-types.md)
      + [Operators](iot-sql-operators.md)
      + [Functions](iot-sql-functions.md)
      + [Literals](iot-sql-literals.md)
      + [Case statements](iot-sql-case.md)
      + [JSON extensions](iot-sql-json.md)
      + [Substitution templates](iot-substitution-templates.md)
      + [Nested object queries](iot-sql-nested-queries.md)
      + [Working with binary payloads](binary-payloads.md)
      + [SQL versions](iot-rule-sql-version.md)
+ [AWS IoT Device Shadow service](iot-device-shadows.md)
   + [Using shadows in devices](device-shadow-comms-device.md)
   + [Using shadows in apps and services](device-shadow-comms-app.md)
   + [Simulating Device Shadow service communications](using-device-shadows.md)
   + [Interacting with shadows](device-shadow-data-flow.md)
   + [Device Shadow REST API](device-shadow-rest-api.md)
   + [Device Shadow MQTT topics](device-shadow-mqtt.md)
   + [Device Shadow service documents](device-shadow-document.md)
   + [Device Shadow error messages](device-shadow-error-messages.md)
+ [Jobs](iot-jobs.md)
   + [What is AWS IoT Jobs?](jobs-what-is.md)
      + [Jobs key concepts](key-concepts-jobs.md)
      + [Jobs and job execution states](iot-jobs-lifecycle.md)
   + [Managing jobs](create-manage-jobs.md)
      + [Create and manage jobs by using the AWS Management Console](manage-job-console.md)
      + [Create and manage jobs by using the AWS CLI](manage-job-cli.md)
   + [Job templates](job-templates.md)
      + [Use AWS managed templates to deploy common remote operations](job-templates-managed.md)
         + [Create a job from AWS managed templates by using the AWS Management Console](job-template-manage-console-create.md)
         + [Create a job from AWS managed templates by using the AWS CLI](job-template-manage-cli-create.md)
      + [Create custom job templates](job-templates-create.md)
         + [Create custom job templates by using the AWS Management Console](job-templates-console.md)
         + [Create custom job templates by using the AWS CLI](job-templates-cli.md)
   + [Job configurations](jobs-configurations.md)
      + [How job configurations work](jobs-configurations-details.md)
      + [Specify additional configurations](jobs-configurations-specify.md)
         + [Specify job configurations by using the AWS Management Console](job-configurations-console.md)
         + [Specify job configurations by using the AWS IoT Jobs API](job-configurations-api.md)
   + [Devices and jobs](jobs-devices.md)
      + [Device workflow](jobs-workflow-device-online.md)
      + [Jobs workflow](jobs-workflow-jobs-online.md)
      + [Jobs notifications](jobs-comm-notifications.md)
   + [AWS IoT jobs APIs](jobs-api.md)
      + [Jobs management and control API and data types](jobs-management-control-api.md)
      + [Jobs device MQTT and HTTPS APIs and data types](jobs-mqtt-https-api.md)
         + [Jobs device MQTT API](jobs-mqtt-api.md)
         + [Jobs device HTTP API](jobs-http-device-api.md)
   + [Securing users and devices with AWS IoT Jobs](iot-jobs-security.md)
      + [Authorizing users and cloud services to use AWS IoT Jobs](iam-policy-users-jobs.md)
      + [Authorizing your devices to securely use AWS IoT Jobs on the data plane](iot-data-plane-jobs.md)
   + [Job limits](job-limits.md)
+ [AWS IoT secure tunneling](secure-tunneling.md)
   + [What is secure tunneling?](secure-tunneling-what-is.md)
      + [Secure tunneling concepts](secure-tunneling-concepts.md)
      + [How secure tunneling works](how-secure-tunneling-works.md)
      + [Secure tunnel lifecycle](tunnel-lifecycle.md)
   + [AWS IoT secure tunneling tutorials](secure-tunneling-tutorial.md)
      + [Open a tunnel and start SSH session to remote device](secure-tunneling-tutorial-open-tunnel.md)
   + [Local proxy](local-proxy.md)
      + [How to use the local proxy](how-use-local-proxy.md)
      + [Configure local proxy for devices that use web proxy](configure-local-proxy-web-proxy.md)
   + [Multiplex data streams and using simultaneous TCP connections in a secure tunnel](multiplexing.md)
      + [Multiplexing multiple data streams in a secure tunnel](multiplexing-multiple-streams.md)
      + [Using simultaneous TCP connections in a secure tunnel](multiplexing-simultaenous-tcp.md)
   + [Configuring a remote device and using IoT agent](configure-remote-device.md)
   + [Controlling access to tunnels](tunnel-access.md)
   + [Resolving AWS IoT secure ing connectivity issues by rotating client access tokens](iot-secure-tunneling-troubleshooting.md)
+ [Device provisioning](iot-provision.md)
   + [Provisioning devices that don't have device certificates using fleet provisioning](provision-wo-cert.md)
   + [Provisioning devices that have device certificates](provision-w-cert.md)
      + [Single thing provisioning](single-thing-provisioning.md)
      + [Just-in-time provisioning](jit-provisioning.md)
      + [Bulk registration](bulk-provisioning.md)
   + [Provisioning templates](provision-template.md)
   + [Pre-provisioning hooks](pre-provisioning-hook.md)
   + [Creating IAM policies and roles for a user installing a device](provision-create-role.md)
   + [Device provisioning MQTT API](fleet-provision-api.md)
+ [Fleet indexing](iot-indexing.md)
   + [Managing fleet indexing](managing-fleet-index.md)
      + [Manage thing indexing](managing-index.md)
      + [Manage thing group indexing](thinggroup-index.md)
   + [Querying for aggregate data](index-aggregate.md)
   + [Query syntax](query-syntax.md)
   + [Example thing queries](example-queries.md)
   + [Example thing group queries](example-thinggroup-queries.md)
   + [Fleet metrics](iot-fleet-metrics.md)
      + [Getting started tutorial](fleet-metrics-get-started.md)
      + [Managing fleet metrics](managing-fleet-metrics.md)
+ [MQTT-based file delivery](mqtt-based-file-delivery.md)
   + [What is a stream?](mqtt-based-file-delivery-what-is.md)
   + [Managing a stream in the AWS Cloud](mqtt-based-file-delivery-managing.md)
   + [Using AWS IoT MQTT-based file delivery in devices](mqtt-based-file-delivery-in-devices.md)
   + [An example use case in FreeRTOS OTA](mqtt-based-file-delivery-example.md)
+ [AWS IoT Device Defender](device-defender.md)
   + [Getting started with AWS IoT Device Defender](dd-tutorials.md)
      + [Setting up](dd-setting-up.md)
      + [Audit guide](audit-tutorial.md)
      + [ML Detect guide](dd-detect-ml-getting-started.md)
      + [Customize when and how you view AWS IoT Device Defender audit results](dd-suppressions-example.md)
   + [Audit](device-defender-audit.md)
      + [Audit checks](device-defender-audit-checks.md)
         + [CA certificate revoked but device certificates still active](audit-chk-revoked-ca-cert.md)
         + [Device certificate shared](audit-chk-device-cert-shared.md)
         + [Device certificate key quality](audit-chk-device-cert-key-quality.md)
         + [CA certificate key quality](audit-chk-ca-cert-key-quality.md)
         + [Unauthenticated Cognito role overly permissive](audit-chk-unauth-cognito-role-permissive.md)
         + [Authenticated Cognito role overly permissive](audit-chk-auth-cognito-role-permissive.md)
         + [AWS IoT policies overly permissive](audit-chk-iot-policy-permissive.md)
         + [Role alias overly permissive](audit-chk-iot-role-alias-permissive.md)
         + [Role alias allows access to unused services](audit-chk-role-alias-unused-svcs.md)
         + [CA certificate expiring](audit-chk-ca-cert-approaching-expiration.md)
         + [Conflicting MQTT client IDs](audit-chk-conflicting-client-ids.md)
         + [Device certificate expiring](audit-chk-device-cert-approaching-expiration.md)
         + [Revoked device certificate still active](audit-chk-revoked-device-cert.md)
         + [Logging disabled](audit-chk-logging-disabled.md)
      + [Audit commands](AuditCommands.md)
      + [Audit finding suppressions](audit-finding-suppressions.md)
   + [Detect](device-defender-detect.md)
      + [Security use cases](dd-detect-security-use-cases.md)
      + [Concepts](detect-concepts.md)
      + [Behaviors](detect-behaviors.md)
      + [ML Detect](dd-detect-ml.md)
      + [Custom metrics](dd-detect-custom-metrics.md)
      + [Device-side metrics](detect-device-side-metrics.md)
      + [Cloud-side metrics](detect-cloud-side-metrics.md)
      + [Scoping metrics in security profiles using dimensions](scoping-security-behavior.md)
      + [Permissions](device-defender-detect-permissions.md)
      + [Detect commands](detect-commands.md)
      + [How to use AWS IoT Device Defender detect](detect-HowToHowTo.md)
   + [Mitigation actions](dd-mitigation-actions.md)
      + [Mitigation action commands](mitigation-action-commands.md)
   + [Using AWS IoT Device Defender with other AWS services](dd-integration.md)
   + [Cross-service confused deputy prevention](dd-cross-service-confused-deputy-prevention.md)
   + [Security best practices for device agents](device-defender-DetectMetricsMessagesBestPract.md)
+ [Device Advisor](device-advisor.md)
   + [Setting up](device-advisor-setting-up.md)
   + [Getting started with Device Advisor in the console](da-console-guide.md)
   + [Device Advisor workflow](device-advisor-workflow.md)
   + [Device Advisor detailed console workflow](device-advisor-console-tutorial.md)
   + [Device Advisor test cases](device-advisor-tests.md)
      + [TLS](device-advisor-tests-tls.md)
      + [MQTT](device-advisor-tests-mqtt.md)
      + [Shadow](device-advisor-tests-shadow.md)
      + [Job Execution](device-advisor-tests-job-execution.md)
      + [Permissions and policies](device-advisor-tests-permissions-policies.md)
+ [Event messages](iot-events.md)
   + [Registry events](registry-events.md)
   + [Jobs events](events-jobs.md)
   + [Lifecycle events](life-cycle-events.md)
+ [AWS IoT Core for LoRaWAN](connect-iot-lorawan.md)
   + [What is AWS IoT Core for LoRaWAN?](connect-iot-lorawan-concepts.md)
      + [What is LoRaWAN?](connect-iot-lorawan-what-is-lorawan.md)
      + [How AWS IoT Core for LoRaWAN works](connect-iot-lorawan-what-is-iot-lorawan.md)
   + [Connecting gateways and devices to AWS IoT Core for LoRaWAN](connect-iot-lorawan-getting-started.md)
      + [Describe your AWS IoT Core for LoRaWAN resources](connect-iot-lorawan-describe-resource.md)
      + [Onboard your gateways to AWS IoT Core for LoRaWAN](connect-iot-lorawan-onboard-gateways.md)
         + [Consider frequency band selection and add necessary IAM role](connect-iot-lorawan-rfregion-permissions.md)
         + [Add a gateway to AWS IoT Core for LoRaWAN](connect-iot-lorawan-onboard-gateway-add.md)
         + [Connect your LoRaWAN gateway and verify its connection status](connect-iot-lorawan-gateway-connection-status.md)
      + [Onboard your devices to AWS IoT Core for LoRaWAN](connect-iot-lorawan-onboard-end-devices.md)
         + [Add your wireless device to AWS IoT Core for LoRaWAN](connect-iot-lorawan-end-devices-add.md)
         + [Add profiles to AWS IoT Core for LoRaWAN](connect-iot-lorawan-define-profiles.md)
         + [Add destinations to AWS IoT Core for LoRaWAN](connect-iot-lorawan-create-destinations.md)
         + [Create rules to process LoRaWAN device messages](connect-iot-lorawan-destination-rules.md)
         + [Connect your LoRaWAN device and verify its connection status](connect-iot-lorawan-device-connection-status.md)
   + [Configure position of wireless resources with AWS IoT Core for LoRaWAN](connect-iot-lorawan-configure-location.md)
      + [Configuring the position of LoRaWAN gateways](connect-iot-lorawan-location-gateways.md)
      + [Configuring position of LoRaWAN devices](connect-iot-lorawan-location-devices.md)
   + [Connecting to AWS IoT Core for LoRaWAN through a VPC interface endpoint](connect-iot-lorawan-interface-vpc-endpoint.md)
      + [Onboard AWS IoT Core for LoRaWAN control plane API endpoint](connect-iot-lorawan-onboard-control-plane-endpoint.md)
      + [Onboard AWS IoT Core for LoRaWAN data plane API endpoints](connect-iot-lorawan-onboard-lns-cups-endpoints.md)
         + [Create VPC interface endpoint and private hosted zone](connect-iot-lorawan-create-vpc-lns-cups.md)
         + [Use VPN to connect LoRa gateways to your AWS account](connect-iot-lorawan-create-vpc-vpn-connection.md)
   + [Managing gateways with AWS IoT Core for LoRaWAN](connect-iot-lorawan-manage-gateways.md)
      + [Configure beaconing and filtering capabilities of your LoRaWAN gateways](connect-iot-lorawan-gateway-configure.md)
         + [Configuring your gateways to send beacons to class B devices](connect-iot-lorawan-gateway-beaconing.md)
         + [Configuring your gateway's subbands and filtering capabilities](connect-iot-lorawan-subband-filter-configuration.md)
      + [Update gateway firmware using CUPS service with AWS IoT Core for LoRaWAN](connect-iot-lorawan-update-firmware.md)
         + [Generate the firmware update file and signature](connect-iot-lorawan-script-fwupdate-sigkey.md)
         + [Upload the firmware file to an S3 bucket and add an IAM role](connect-iot-lorawan-upload-firmware-s3bucket.md)
         + [Schedule and run the firmware update by using a task definition](connect-iot-lorawan-schedule-firmware-update.md)
      + [Choosing gateways to receive the LoRaWAN downlink data traffic](connect-iot-lorawan-gateway-participate.md)
   + [Managing devices with AWS IoT Core for LoRaWAN](connect-iot-lorawan-manage-end-devices.md)
      + [Manage communication between your LoRaWAN devices and AWS IoT](connect-iot-lorawan-device-cloud-communication.md)
         + [View format of uplink messages sent from LoRaWAN devices](connect-iot-lorawan-uplink-metadata-format.md)
         + [Queue downlink messages to send to LoRaWAN devices](connect-iot-lorawan-downlink-queue.md)
      + [Create multicast groups to send a downlink payload to multiple devices](connect-iot-lorawan-multicast-groups.md)
         + [Prepare devices for multicast and FUOTA configuration](connect-iot-lorawan-prepare-devices-multicast.md)
         + [Create multicast groups and add devices to the group](connect-iot-lorawan-create-multicast-groups.md)
         + [Monitor and troubleshoot status of your multicast group and devices in the group](connect-iot-lorawan-multicast-status.md)
         + [Schedule a downlink message to send to devices in your multicast group](connect-iot-lorawan-multicast-schedule-downlink.md)
      + [Firmware Updates Over-The-Air (FUOTA) for AWS IoT Core for LoRaWAN devices](connect-iot-lorawan-mc-fuota-overview.md)
         + [FUOTA process overview](connect-iot-lorawan-fuota-mc-process.md)
         + [Create FUOTA task and provide firmware image](connect-iot-lorawan-fuota-create-task.md)
         + [Add devices and multicast groups to a FUOTA task and schedule a FUOTA session](connect-iot-lorawan-fuota-add-devices.md)
         + [Monitor and troubleshoot the status of your FUOTA task and devices added to the task](connect-iot-lorawan-fuota-status.md)
   + [Monitoring your wireless resource fleet in real time using network analyzer](connect-iot-lorawan-network-analyzer-overview.md)
      + [Add necessary IAM role for network analyzer](connect-iot-lorawan-network-analyzer-iam.md)
      + [Create a network analyzer configuration and add resources](connect-iot-lorawan-network-analyzer-create-resources.md)
         + [Create a network analyzer configuration](connect-iot-lorawan-network-analyzer-create.md)
         + [Add resources and update the network analyzer configuration](connect-iot-lorawan-network-analyzer-resources.md)
      + [Stream network analyzer trace messages with WebSockets](connect-iot-lorawan-network-analyzer-api.md)
         + [Generate a presigned request with the WebSocket library](connect-iot-lorawan-network-analyzer-generate-request.md)
         + [WebSocket messages and status codes](conect-iot-lorawan-network-analyer-messages-status.md)
      + [View and monitor network analyzer trace message logs in real time](connect-iot-lorawan-network-analyzer-logs.md)
   + [Data security with AWS IoT Core for LoRaWAN](connect-iot-lorawan-security.md)
+ [Amazon Sidewalk Integration for AWS IoT Core](iot-sidewalk.md)
   + [Onboard Sidewalk devices with Amazon Sidewalk Integration for AWS IoT Core](iot-sidewalk-getting-started.md)
      + [Add your Sidewalk account credentials](iot-sidewalk-add-credentials.md)
      + [Add a destination for your Sidewalk device](iot-sidewalk-add-destination.md)
      + [Create rules to process Sidewalk device messages](iot-sidewalk-create-rules.md)
   + [Connect your Sidewalk device and view uplink metadata format](iot-sidewalk-connect-uplink-metadata.md)
+ [Monitoring and logging for AWS IoT Wireless using Amazon CloudWatch](connect-iot-lorawan-logging-monitoring.md)
   + [Configure Logging for AWS IoT Wireless](connect-iot-lorawan-configure-logging.md)
      + [Create logging role and policy for AWS IoT Wireless](connect-iot-lorawan-create-logging-role-policy.md)
      + [Configure logging for AWS IoT Wireless resources](connect-iot-lorawan-configure-resource-logging.md)
   + [Monitor AWS IoT Wireless using CloudWatch Logs](connect-iot-lorawan-cloud-watch-logs.md)
      + [View CloudWatch AWS IoT Wireless log entries](connect-iot-lorawan-cwl-format.md)
         + [Log entries for wireless gateways and wireless device resources](connect-iot-lorawan-wireless-log-entries.md)
      + [Use CloudWatch Insights to filter logs for AWS IoT Wireless](connect-iot-lorawan-cwl-insights.md)
+ [Event notifications for AWS IoT Wireless](iot-wireless-event-messages.md)
   + [Enable events for wireless resources](iot-wireless-control-events.md)
   + [Event notifications for LoRaWAN resources](iot-lorawan-events.md)
      + [LoRaWAN join events](iot-lorawan-join-events.md)
      + [Connection status events](iot-lorawan-gateway-events.md)
   + [Event notifications for Sidewalk resources](iot-sidewalk-events.md)
      + [Device registration state events](iot-sidewalk-device-events.md)
      + [Proximity events](iot-sidewalk-proximity-events.md)
      + [Message delivery status events](iot-sidewalk-message-delivery-events.md)
+ [Alexa Voice Service (AVS) Integration for AWS IoT](avs-integration-aws-iot.md)
   + [Getting started with Alexa Voice Service (AVS) Integration for AWS IoT on an NXP device](avs-integration-aws-iot-gs-nxp.md)
+ [AWS IoT Device SDKs, Mobile SDKs, and AWS IoT Device Client](iot-sdks.md)
+ [Troubleshooting AWS IoT](iot_troubleshooting.md)
   + [Diagnosing connectivity issues](diagnosing-connectivity-issues.md)
   + [Diagnosing rules issues](diagnosing-rules.md)
   + [Diagnosing problems with shadows](diagnosing-shadows.md)
   + [Diagnosing Salesforce IoT input stream action issues](diagnosing-salesforce.md)
   + [Fleet indexing troubleshooting guide](fleet-indexing-troubleshooting.md)
   + [Troubleshooting "Stream limit exceeded for your AWS account"](ota-troubleshooting-stream-limit.md)
   + [AWS IoT Device Defender troubleshooting guide](device-defender-troubleshoot.md)
   + [AWS IoT Device Advisor troubleshooting guide](device-advisor-troubleshooting.md)
   + [Troubleshooting device fleet disconnects](ota-troubleshooting-fleet-disconnects.md)
   + [AWS IoT errors](iot-errors.md)
+ [AWS IoT quotas](limits-iot.md)