---
title : "Kết nối ESP32 với IoT Core"
weight : 2 
chapter : false
pre : " <b> 5.2. </b> "
---

#### Quyền IAM
Thêm chính sách quyền IAM sau vào tài khoản người dùng của bạn để triển khai và dọn dẹp workshop.
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "cloudformation:*",
                "cloudwatch:*",
                "ec2:AcceptTransitGatewayPeeringAttachment",
                "ec2:AcceptTransitGatewayVpcAttachment",
                "ec2:AllocateAddress",
                "ec2:AssociateAddress",
                "ec2:AssociateIamInstanceProfile",
                "ec2:AssociateRouteTable",
                "ec2:AssociateSubnetCidrBlock",
                "ec2:AssociateTransitGatewayRouteTable",
                "ec2:AssociateVpcCidrBlock",
                "ec2:AttachInternetGateway",
                "ec2:AttachNetworkInterface",
                "ec2:AttachVolume",
                "ec2:AttachVpnGateway",
                "ec2:AuthorizeSecurityGroupEgress",
                "ec2:AuthorizeSecurityGroupIngress",
                "ec2:CreateClientVpnEndpoint",
                "ec2:CreateClientVpnRoute",
                "ec2:CreateCustomerGateway",
                "ec2:CreateDhcpOptions",
                "ec2:CreateFlowLogs",
                "ec2:CreateInternetGateway",
                "ec2:CreateLaunchTemplate",
                "ec2:CreateNetworkAcl",
                "ec2:CreateNetworkInterface",
                "ec2:CreateNetworkInterfacePermission",
                "ec2:CreateRoute",
                "ec2:CreateRouteTable",
                "ec2:CreateSecurityGroup",
                "ec2:CreateSubnet",
                "ec2:CreateSubnetCidrReservation",
                "ec2:CreateTags",
                "ec2:CreateTransitGateway",
                "ec2:CreateTransitGatewayPeeringAttachment",
                "ec2:CreateTransitGatewayPrefixListReference",
                "ec2:CreateTransitGatewayRoute",
                "ec2:CreateTransitGatewayRouteTable",
                "ec2:CreateTransitGatewayVpcAttachment",
                "ec2:CreateVpc",
                "ec2:CreateVpcEndpoint",
                "ec2:CreateVpcEndpointConnectionNotification",
                "ec2:CreateVpcEndpointServiceConfiguration",
                "ec2:CreateVpnConnection",
                "ec2:CreateVpnConnectionRoute",
                "ec2:CreateVpnGateway",
                "ec2:DeleteCustomerGateway",
                "ec2:DeleteFlowLogs",
                "ec2:DeleteInternetGateway",
                "ec2:DeleteNetworkInterface",
                "ec2:DeleteNetworkInterfacePermission",
                "ec2:DeleteRoute",
                "ec2:DeleteRouteTable",
                "ec2:DeleteSecurityGroup",
                "ec2:DeleteSubnet",
                "ec2:DeleteSubnetCidrReservation",
                "ec2:DeleteTags",
                "ec2:DeleteTransitGateway",
                "ec2:DeleteTransitGatewayPeeringAttachment",
                "ec2:DeleteTransitGatewayPrefixListReference",
                "ec2:DeleteTransitGatewayRoute",
                "ec2:DeleteTransitGatewayRouteTable",
                "ec2:DeleteTransitGatewayVpcAttachment",
                "ec2:DeleteVpc",
                "ec2:DeleteVpcEndpoints",
                "ec2:DeleteVpcEndpointServiceConfigurations",
                "ec2:DeleteVpnConnection",
                "ec2:DeleteVpnConnectionRoute",
                "ec2:Describe*",
                "ec2:DetachInternetGateway",
                "ec2:DisassociateAddress",
                "ec2:DisassociateRouteTable",
                "ec2:GetLaunchTemplateData",
                "ec2:GetTransitGatewayAttachmentPropagations",
                "ec2:ModifyInstanceAttribute",
                "ec2:ModifySecurityGroupRules",
                "ec2:ModifyTransitGatewayVpcAttachment",
                "ec2:ModifyVpcAttribute",
                "ec2:ModifyVpcEndpoint",
                "ec2:ReleaseAddress",
                "ec2:ReplaceRoute",
                "ec2:RevokeSecurityGroupEgress",
                "ec2:RevokeSecurityGroupIngress",
                "ec2:RunInstances",
                "ec2:StartInstances",
                "ec2:StopInstances",
                "ec2:UpdateSecurityGroupRuleDescriptionsEgress",
                "ec2:UpdateSecurityGroupRuleDescriptionsIngress",
                "iam:AddRoleToInstanceProfile",
                "iam:AttachRolePolicy",
                "iam:CreateInstanceProfile",
                "iam:CreatePolicy",
                "iam:CreateRole",
                "iam:DeleteInstanceProfile",
                "iam:DeletePolicy",
                "iam:DeleteRole",
                "iam:DeleteRolePolicy",
                "iam:DetachRolePolicy",
                "iam:GetInstanceProfile",
                "iam:GetPolicy",
                "iam:GetRole",
                "iam:GetRolePolicy",
                "iam:ListPolicyVersions",
                "iam:ListRoles",
                "iam:PassRole",
                "iam:PutRolePolicy",
                "iam:RemoveRoleFromInstanceProfile",
                "lambda:CreateFunction",
                "lambda:DeleteFunction",
                "lambda:DeleteLayerVersion",
                "lambda:GetFunction",
                "lambda:GetLayerVersion",
                "lambda:InvokeFunction",
                "lambda:PublishLayerVersion",
                "logs:CreateLogGroup",
                "logs:DeleteLogGroup",
                "logs:DescribeLogGroups",
                "logs:PutRetentionPolicy",
                "route53:ChangeTagsForResource",
                "route53:CreateHealthCheck",
                "route53:CreateHostedZone",
                "route53:CreateTrafficPolicy",
                "route53:DeleteHostedZone",
                "route53:DisassociateVPCFromHostedZone",
                "route53:GetHostedZone",
                "route53:ListHostedZones",
                "route53domains:ListDomains",
                "route53domains:ListOperations",
                "route53domains:ListTagsForDomain",
                "route53resolver:AssociateResolverEndpointIpAddress",
                "route53resolver:AssociateResolverRule",
                "route53resolver:CreateResolverEndpoint",
                "route53resolver:CreateResolverRule",
                "route53resolver:DeleteResolverEndpoint",
                "route53resolver:DeleteResolverRule",
                "route53resolver:DisassociateResolverEndpointIpAddress",
                "route53resolver:DisassociateResolverRule",
                "route53resolver:GetResolverEndpoint",
                "route53resolver:GetResolverRule",
                "route53resolver:ListResolverEndpointIpAddresses",
                "route53resolver:ListResolverEndpoints",
                "route53resolver:ListResolverRuleAssociations",
                "route53resolver:ListResolverRules",
                "route53resolver:ListTagsForResource",
                "route53resolver:UpdateResolverEndpoint",
                "route53resolver:UpdateResolverRule",
                "s3:AbortMultipartUpload",
                "s3:CreateBucket",
                "s3:DeleteBucket",
                "s3:DeleteObject",
                "s3:GetAccountPublicAccessBlock",
                "s3:GetBucketAcl",
                "s3:GetBucketOwnershipControls",
                "s3:GetBucketPolicy",
                "s3:GetBucketPolicyStatus",
                "s3:GetBucketPublicAccessBlock",
                "s3:GetObject",
                "s3:GetObjectVersion",
                "s3:GetBucketVersioning",
                "s3:ListAccessPoints",
                "s3:ListAccessPointsForObjectLambda",
                "s3:ListAllMyBuckets",
                "s3:ListBucket",
                "s3:ListBucketMultipartUploads",
                "s3:ListBucketVersions",
                "s3:ListJobs",
                "s3:ListMultipartUploadParts",
                "s3:ListMultiRegionAccessPoints",
                "s3:ListStorageLensConfigurations",
                "s3:PutAccountPublicAccessBlock",
                "s3:PutBucketAcl",
                "s3:PutBucketPolicy",
                "s3:PutBucketPublicAccessBlock",
                "s3:PutObject",
                "secretsmanager:CreateSecret",
                "secretsmanager:DeleteSecret",
                "secretsmanager:DescribeSecret",
                "secretsmanager:GetSecretValue",
                "secretsmanager:ListSecrets",
                "secretsmanager:ListSecretVersionIds",
                "secretsmanager:PutResourcePolicy",
                "secretsmanager:TagResource",
                "secretsmanager:UpdateSecret",
                "sns:ListTopics",
                "ssm:DescribeInstanceProperties",
                "ssm:DescribeSessions",
                "ssm:GetConnectionStatus",
                "ssm:GetParameters",
                "ssm:ListAssociations",
                "ssm:ResumeSession",
                "ssm:StartSession",
                "ssm:TerminateSession"
            ],
            "Resource": "*"
        }
    ]
}

```

#### Kết nối ESP32 bằng IoT Core

Trong lab này, chúng ta sử dụng **Singapore ap-southeast-1**.

Để chuẩn bị môi trường workshop, tạo **IoT Core Template** (nhấp link): [PrivateLinkWorkshop ](https://ap-southeast-1.console.aws.amazon.com/iot/home?region=ap-southeast-1#/thing/ESP32_01). Chấp nhận tất cả giá trị mặc định khi triển khai template.

![create stack](/images/5-Workshop/5.2-Prerequisite/CreateThings1.jpeg)

+ Chọn **IoT Core template**
+ Chọn **Create Things**

![create stack](/images/5-Workshop/5.2-Prerequisite/CreateThings2.jpeg)

+ Chọn **Create single thing**
+ Chọn **Next**

![complete](/images/5-Workshop/5.2-Prerequisite/CreateThings3.jpeg)

+ Đặt tên **thing**
+ Chọn **Next**

![vpcs](/images/5-Workshop/5.2-Prerequisite/CreateThings4.jpeg)

+ Chọn **Recommended Option**
+ Chọn **Next**
![EC2](/images/5-Workshop/5.2-Prerequisite/CreateThings5.jpeg)
+ Chọn **Create Policy**
+ Chọn **Next**

![EC2](/images/5-Workshop/5.2-Prerequisite/CreateThings6.jpeg)
+ Đặt tên **Policy**
+ Chọn **Add Four New Statements**
![EC2](/images/5-Workshop/5.2-Prerequisite/Code.jpg)
+ Dựa trên **Code** để điền **Resource Name**
![EC2](/images/5-Workshop/5.2-Prerequisite/CreateThings7.jpeg)

+ Chọn **Policy Action** như hình
+ Điền **Policy Resource** với thông tin của bạn
+ Chọn **Create**

![EC2](/images/5-Workshop/5.2-Prerequisite/CreateThings8.jpeg)

+ Chọn **Create Policy**

![EC2](/images/5-Workshop/5.2-Prerequisite/CreateThings9.jpeg)
+ Chọn **ESP32_POLICY**
+ Chọn **Create thing**

#### Mã IoT
Thêm đoạn code sau để kết nối ESP32.
```

{
#ifndef AWS_CONFIG_H
#define AWS_CONFIG_H
#include <pgmspace.h>



// Wi-Fi (Connect to your hotspot)
#define WIFI_SSID "ABC"
#define WIFI_PASSWORD "***"

// ================== AWS IoT Core ==================
// ✅ Endpoint trong AWS CLI 
#define AWS_IOT_ENDPOINT ""

// ✅ Thing name trùng với AWS Thing
#define AWS_IOT_CLIENT_ID "ESP32_01"

// ✅ Topics khớp với policy của bạn
#define AWS_IOT_PUBLISH_TOPIC "esp32/pub"
#define AWS_IOT_SUBSCRIBE_TOPIC "esp32/sub"

// Chứng chỉ
static const char AWS_CERT_CA[] PROGMEM = R"EOF(

)EOF";
//Device Certificate
static const char AWS_CERT_CRT[] PROGMEM = R"KEY(

)KEY";

static const char AWS_CERT_PRIVATE[] PROGMEM = R"KEY(

)KEY";

#endif
}
```
![EC2](/images/5-Workshop/5.2-Prerequisite/CreateCert1.jpeg)
+ Chọn **Create Certificate**


![EC2](/images/5-Workshop/5.2-Prerequisite/CreateCert2.jpeg)
+ Chọn **Create**

![EC2](/images/5-Workshop/5.2-Prerequisite/CreateCert3.jpeg)
+ Tải về **4 Certificate (Device, Public Key File, Private Key File, CA1)** 
+ Chọn **Continue**

![EC2](/images/5-Workshop/5.2-Prerequisite/MQTT1.jpeg)
+ Chọn **esp32/pub**
+ Chọn **Subcribe**

![EC2](/images/5-Workshop/5.2-Prerequisite/MQTT2.jpeg)

