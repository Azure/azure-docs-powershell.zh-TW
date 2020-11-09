---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286223"
---
# <span data-ttu-id="d4b46-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d4b46-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="d4b46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4b46-102">SYNOPSIS</span></span>
<span data-ttu-id="d4b46-103">[取得 IoT 中心安全性] (的裝置安全性群組) </span><span class="sxs-lookup"><span data-stu-id="d4b46-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="d4b46-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4b46-104">SYNTAX</span></span>

### <span data-ttu-id="d4b46-105">ResourceIdScope (預設) </span><span class="sxs-lookup"><span data-stu-id="d4b46-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4b46-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="d4b46-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4b46-107">說明</span><span class="sxs-lookup"><span data-stu-id="d4b46-107">DESCRIPTION</span></span>
<span data-ttu-id="d4b46-108">Get-AzDeviceSecurityGroup Cmdlet 會傳回在 iot 安全解決方案中定義的裝置安全性群組</span><span class="sxs-lookup"><span data-stu-id="d4b46-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="d4b46-109">示例</span><span class="sxs-lookup"><span data-stu-id="d4b46-109">EXAMPLES</span></span>

### <span data-ttu-id="d4b46-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d4b46-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="d4b46-111">在具有 reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 的 IoT 中樞中取得裝置安全性群組 "MySecurityGroup"</span><span class="sxs-lookup"><span data-stu-id="d4b46-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="d4b46-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d4b46-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="d4b46-113">取得使用 reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 的 IoT 中樞中的裝置安全性群組清單</span><span class="sxs-lookup"><span data-stu-id="d4b46-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="d4b46-114">參數</span><span class="sxs-lookup"><span data-stu-id="d4b46-114">PARAMETERS</span></span>

### <span data-ttu-id="d4b46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4b46-115">-DefaultProfile</span></span>
<span data-ttu-id="d4b46-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4b46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b46-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="d4b46-117">-HubResourceId</span></span>
<span data-ttu-id="d4b46-118">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4b46-118">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b46-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4b46-119">-Name</span></span>
<span data-ttu-id="d4b46-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="d4b46-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4b46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4b46-121">CommonParameters</span></span>
<span data-ttu-id="d4b46-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4b46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4b46-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4b46-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4b46-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d4b46-124">INPUTS</span></span>

### <span data-ttu-id="d4b46-125">所有</span><span class="sxs-lookup"><span data-stu-id="d4b46-125">None</span></span>

## <span data-ttu-id="d4b46-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d4b46-126">OUTPUTS</span></span>

### <span data-ttu-id="d4b46-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d4b46-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="d4b46-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d4b46-128">NOTES</span></span>

## <span data-ttu-id="d4b46-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4b46-129">RELATED LINKS</span></span>
