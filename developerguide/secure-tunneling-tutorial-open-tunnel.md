# Open a tunnel and start SSH session to remote device<a name="secure-tunneling-tutorial-open-tunnel"></a>

In this tutorial, you open a tunnel and use it to start an SSH session to a remote device\. The remote device is behind firewalls that block all inbound traffic, making direct SSH into the device impossible\. Before you begin, make sure that you understand how to [register a device in the AWS IoT registry](https://docs.aws.amazon.com/iot/latest/developerguide/register-device.html) and [connect a device to the AWS IoT device gateway](https://docs.aws.amazon.com/iot/latest/developerguide/sdk-tutorials.html)\.

## Prerequisites<a name="tunneling-tutorial-prerequisites"></a>
+ The firewalls the remote device is behind must allow outbound traffic on port 443\.
+ You have created an IoT thing named `RemoteDeviceA` in the AWS IoT registry\.
+ You have an IoT device agent running on the remote device that connects to the AWS IoT device gateway and is configured with an MQTT topic subscription\. This tutorial includes a snippet that shows you how to implement an agent\. For more information, see [IoT agent snippet](configure-remote-device.md#agent-snippet)\.
+ You must have an SSH daemon running on the remote device\.
+ You have downloaded the local proxy source code from [GitHub](https://github.com/aws-samples/aws-iot-securetunneling-localproxy) and built it for the platform of your choice\. We'll refer to the built local proxy executable file as `localproxy` in this tutorial\.

## Open a tunnel<a name="open-tunnel"></a>

If you configure the destination when calling `OpenTunnel`, the secure tunneling delivers the destination client access token to the remote device over MQTT and the reserved MQTT topic \(`$aws/things/RemoteDeviceA/tunnels/notify`\)\. For more information, see [Reserved topics](reserved-topics.md)\. Upon receipt of the MQTT message, the IoT agent on the remote device starts the local proxy in destination mode\. You can omit the destination configuration if you want to deliver the destination client access token to the remote device through another method\. For more information, see [Configuring a remote device and using IoT agent](configure-remote-device.md)\.

**To open a tunnel in the console**

1. In the [AWS IoT console](https://console.aws.amazon.com/iot/), navigate to **Manage** and choose **Tunnels**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/iot/latest/developerguide/images/tunnels-page.png)

1. Choose **Create tunnel**\.

1. Enter a tunnel description, the thing name for which you want to open a tunnel, the service to be used such as SSH or FTP, a tunnel timeout duration, and resource tags as key\-value pairs to help you identify your resource\.

1. Download the client access tokens for the source and destination\. The tokens will not be available to download after you choose **Done**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/iot/latest/developerguide/images/tunnel-success.png)

1. Select **Done**\.

## Start the local proxy<a name="start-local-proxy"></a>

Open a terminal on your laptop, copy the source client access token, and use it to start the local proxy in source mode\. In the following command, the local proxy is configured to listen for new connections on port 5555\.

\./localproxy \-r us\-east\-1 \-s 5555 \-t *source\-client\-access\-token*

**Note**  
The AWS Region in this command must be the same AWS Region where the tunnel was created\.

\-r  
Specifies the AWS Region where your tunnel is created\.

\-s  
Specifies the port to which the proxy should connect\.

\-t  
Specifies the client token text\.

**Note**  
If you receive the following error, set up the CA path\. For information, see [GitHub](https://github.com/aws-samples/aws-iot-securetunneling-localproxy)\.  
`Could not perform SSL handshake with proxy server: certificate verify failed`

## Start an SSH session<a name="start-ssh-session"></a>

Open another terminal and use the following command to start a new SSH session by connecting to the local proxy on port 5555\.

ssh *username*@localhost \-p 5555

You might be prompted for a password for the SSH session\. When you are done with the SSH session, type **exit** to close the session\.

## Closing the tunnel<a name="close-tunnel"></a>

1. Open the [AWS IoT console](https://console.aws.amazon.com/iot/)\.

1.  Choose the tunnel and from **Actions**, choose **Close**\. Closing the tunnel causes both local proxy instances to close\.