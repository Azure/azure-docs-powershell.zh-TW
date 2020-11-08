---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: f653a71ed00cce72a926259b1f1cfeed026c0624
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137641"
---
# <span data-ttu-id="d5de6-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="d5de6-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="d5de6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5de6-102">SYNOPSIS</span></span>
<span data-ttu-id="d5de6-103">針對裝置安全性群組 (IoT Security) 建立新的時間範圍規則</span><span class="sxs-lookup"><span data-stu-id="d5de6-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="d5de6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5de6-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5de6-105">說明</span><span class="sxs-lookup"><span data-stu-id="d5de6-105">DESCRIPTION</span></span>
<span data-ttu-id="d5de6-106">New-AzDeviceSecurityGroupTimeWindowRuleObject Cmdlet 會針對 IoT security 方案中的 device security 群組，建立一個新的時間視窗警報規則清單。</span><span class="sxs-lookup"><span data-stu-id="d5de6-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="d5de6-107">示例</span><span class="sxs-lookup"><span data-stu-id="d5de6-107">EXAMPLES</span></span>

### <span data-ttu-id="d5de6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d5de6-108">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize $TimeWindowSize -MinThreshold 0 -MaxThreshold 30 -Enabled $true -Type "ActiveConnectionsNotInAllowedRange"

RuleType: "ActiveConnectionsNotInAllowedRange"
DisplayName: "Number of active connections is not in allowed range"
Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 30
TimeWindowSize: "PT5M"
```

<span data-ttu-id="d5de6-109">從 "ActiveConnectionsNotInAllowedRange" 類型建立新的時間範圍規則</span><span class="sxs-lookup"><span data-stu-id="d5de6-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="d5de6-110">參數</span><span class="sxs-lookup"><span data-stu-id="d5de6-110">PARAMETERS</span></span>

### <span data-ttu-id="d5de6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5de6-111">-DefaultProfile</span></span>
<span data-ttu-id="d5de6-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5de6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5de6-113">-啟用</span><span class="sxs-lookup"><span data-stu-id="d5de6-113">-Enabled</span></span>
<span data-ttu-id="d5de6-114">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="d5de6-114">Is rule enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5de6-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="d5de6-115">-MaxThreshold</span></span>
<span data-ttu-id="d5de6-116">最大閾值。</span><span class="sxs-lookup"><span data-stu-id="d5de6-116">Maximum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5de6-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="d5de6-117">-MinThreshold</span></span>
<span data-ttu-id="d5de6-118">[最小值]。</span><span class="sxs-lookup"><span data-stu-id="d5de6-118">Minimum threshold.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5de6-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="d5de6-119">-TimeWindowSize</span></span>
<span data-ttu-id="d5de6-120">時間視窗大小。</span><span class="sxs-lookup"><span data-stu-id="d5de6-120">Time window size.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5de6-121">-類型</span><span class="sxs-lookup"><span data-stu-id="d5de6-121">-Type</span></span>
<span data-ttu-id="d5de6-122">規則類型。</span><span class="sxs-lookup"><span data-stu-id="d5de6-122">Rule type.</span></span>

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

### <span data-ttu-id="d5de6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5de6-123">CommonParameters</span></span>
<span data-ttu-id="d5de6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5de6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5de6-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d5de6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5de6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="d5de6-126">INPUTS</span></span>

### <span data-ttu-id="d5de6-127">所有</span><span class="sxs-lookup"><span data-stu-id="d5de6-127">None</span></span>

## <span data-ttu-id="d5de6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d5de6-128">OUTPUTS</span></span>

### <span data-ttu-id="d5de6-129">PSTimeWindowCustomAlertRule 中的 DeviceSecurityGroups （Security..。</span><span class="sxs-lookup"><span data-stu-id="d5de6-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="d5de6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="d5de6-130">NOTES</span></span>

## <span data-ttu-id="d5de6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5de6-131">RELATED LINKS</span></span>
