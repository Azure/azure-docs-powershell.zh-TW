---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 52fae225184b83675f21af941fa125576252ffbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917645"
---
# <span data-ttu-id="38e7c-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="38e7c-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="38e7c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="38e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="38e7c-103">取得裝置安全性群組 (IoT Hub 安全性) </span><span class="sxs-lookup"><span data-stu-id="38e7c-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="38e7c-104">語法</span><span class="sxs-lookup"><span data-stu-id="38e7c-104">SYNTAX</span></span>

### <span data-ttu-id="38e7c-105">ResourceIdScope (預設) </span><span class="sxs-lookup"><span data-stu-id="38e7c-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38e7c-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="38e7c-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38e7c-107">描述</span><span class="sxs-lookup"><span data-stu-id="38e7c-107">DESCRIPTION</span></span>
<span data-ttu-id="38e7c-108">Cmdlet Get-AzDeviceSecurityGroup iot 安全性解決方案中定義的裝置安全性群組</span><span class="sxs-lookup"><span data-stu-id="38e7c-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="38e7c-109">例子</span><span class="sxs-lookup"><span data-stu-id="38e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="38e7c-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="38e7c-110">Example 1</span></span>
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

<span data-ttu-id="38e7c-111">使用 Reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 在 IoT Hub 中取得裝置安全性群組 "MySecurityGroup"</span><span class="sxs-lookup"><span data-stu-id="38e7c-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="38e7c-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="38e7c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="38e7c-113">使用 Reasource Id "/subscriptions/XXXXXXXX-XXXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 取得 IoT Hub 中的裝置安全性群組清單</span><span class="sxs-lookup"><span data-stu-id="38e7c-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="38e7c-114">參數</span><span class="sxs-lookup"><span data-stu-id="38e7c-114">PARAMETERS</span></span>

### <span data-ttu-id="38e7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e7c-115">-DefaultProfile</span></span>
<span data-ttu-id="38e7c-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="38e7c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38e7c-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="38e7c-117">-HubResourceId</span></span>
<span data-ttu-id="38e7c-118">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="38e7c-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="38e7c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="38e7c-119">-Name</span></span>
<span data-ttu-id="38e7c-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="38e7c-120">Resource name.</span></span>

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

### <span data-ttu-id="38e7c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e7c-121">CommonParameters</span></span>
<span data-ttu-id="38e7c-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="38e7c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e7c-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38e7c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e7c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="38e7c-124">INPUTS</span></span>

### <span data-ttu-id="38e7c-125">沒有</span><span class="sxs-lookup"><span data-stu-id="38e7c-125">None</span></span>

## <span data-ttu-id="38e7c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="38e7c-126">OUTPUTS</span></span>

### <span data-ttu-id="38e7c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="38e7c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="38e7c-128">筆記</span><span class="sxs-lookup"><span data-stu-id="38e7c-128">NOTES</span></span>

## <span data-ttu-id="38e7c-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="38e7c-129">RELATED LINKS</span></span>
