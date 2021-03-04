---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupTimeWindowRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupTimeWindowRuleObject.md
ms.openlocfilehash: fb068adcf7a7775106714dce9d91d23ae5e2c240
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909962"
---
# <span data-ttu-id="4e18e-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span><span class="sxs-lookup"><span data-stu-id="4e18e-101">New-AzDeviceSecurityGroupTimeWindowRuleObject</span></span>

## <span data-ttu-id="4e18e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e18e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e18e-103">為裝置安全性群組建立新時間視窗規則 (IoT 安全性) </span><span class="sxs-lookup"><span data-stu-id="4e18e-103">Create new time window rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="4e18e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e18e-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupTimeWindowRuleObject -TimeWindowSize <TimeSpan> -MinThreshold <Int32>
 -MaxThreshold <Int32> -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e18e-105">描述</span><span class="sxs-lookup"><span data-stu-id="4e18e-105">DESCRIPTION</span></span>
<span data-ttu-id="4e18e-106">此New-AzDeviceSecurityGroupTimeWindowRuleObject Cmdlet 會針對 IoT 安全性解決方案中的裝置安全性群組，建立一份新的時間視窗警示規則清單。</span><span class="sxs-lookup"><span data-stu-id="4e18e-106">The New-AzDeviceSecurityGroupTimeWindowRuleObject cmdlet creates a new list of time window alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="4e18e-107">例子</span><span class="sxs-lookup"><span data-stu-id="4e18e-107">EXAMPLES</span></span>

### <span data-ttu-id="4e18e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4e18e-108">Example 1</span></span>
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

<span data-ttu-id="4e18e-109">從「ActiveConnectionsNotInAllowedRange」類型建立新時間視窗規則</span><span class="sxs-lookup"><span data-stu-id="4e18e-109">Create new time window rule from "ActiveConnectionsNotInAllowedRange" type</span></span>

## <span data-ttu-id="4e18e-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e18e-110">PARAMETERS</span></span>

### <span data-ttu-id="4e18e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e18e-111">-DefaultProfile</span></span>
<span data-ttu-id="4e18e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e18e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e18e-113">-已啟用</span><span class="sxs-lookup"><span data-stu-id="4e18e-113">-Enabled</span></span>
<span data-ttu-id="4e18e-114">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="4e18e-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="4e18e-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="4e18e-115">-MaxThreshold</span></span>
<span data-ttu-id="4e18e-116">最大閥值。</span><span class="sxs-lookup"><span data-stu-id="4e18e-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="4e18e-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="4e18e-117">-MinThreshold</span></span>
<span data-ttu-id="4e18e-118">最低閾值。</span><span class="sxs-lookup"><span data-stu-id="4e18e-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="4e18e-119">-TimeWindowSize</span><span class="sxs-lookup"><span data-stu-id="4e18e-119">-TimeWindowSize</span></span>
<span data-ttu-id="4e18e-120">時間視窗大小。</span><span class="sxs-lookup"><span data-stu-id="4e18e-120">Time window size.</span></span>

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

### <span data-ttu-id="4e18e-121">-類型</span><span class="sxs-lookup"><span data-stu-id="4e18e-121">-Type</span></span>
<span data-ttu-id="4e18e-122">規則類型。</span><span class="sxs-lookup"><span data-stu-id="4e18e-122">Rule type.</span></span>

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

### <span data-ttu-id="4e18e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e18e-123">CommonParameters</span></span>
<span data-ttu-id="4e18e-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e18e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e18e-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e18e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e18e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4e18e-126">INPUTS</span></span>

### <span data-ttu-id="4e18e-127">沒有</span><span class="sxs-lookup"><span data-stu-id="4e18e-127">None</span></span>

## <span data-ttu-id="4e18e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4e18e-128">OUTPUTS</span></span>

### <span data-ttu-id="4e18e-129">Microsoft.Azure.Commands.security.models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="4e18e-129">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule</span></span>

## <span data-ttu-id="4e18e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4e18e-130">NOTES</span></span>

## <span data-ttu-id="4e18e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e18e-131">RELATED LINKS</span></span>
