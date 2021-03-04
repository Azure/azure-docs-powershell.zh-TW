---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 869512fb91e86d90381bbcba9e492198b9a51005
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909966"
---
# <span data-ttu-id="fc566-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="fc566-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="fc566-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc566-102">SYNOPSIS</span></span>
<span data-ttu-id="fc566-103">為裝置安全性群組建立新閾值自訂警示規則 (IoT 安全性) </span><span class="sxs-lookup"><span data-stu-id="fc566-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="fc566-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc566-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc566-105">描述</span><span class="sxs-lookup"><span data-stu-id="fc566-105">DESCRIPTION</span></span>
<span data-ttu-id="fc566-106">Cmdlet New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject為 IoT 安全性解決方案中的裝置安全性群組建立新的閾值自訂警示規則清單。</span><span class="sxs-lookup"><span data-stu-id="fc566-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="fc566-107">例子</span><span class="sxs-lookup"><span data-stu-id="fc566-107">EXAMPLES</span></span>

### <span data-ttu-id="fc566-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fc566-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="fc566-109">從類型 "SomeRuleType" 建立新閾值自訂警示規則，且狀態已啟用 ant 值的最小和最大閾值</span><span class="sxs-lookup"><span data-stu-id="fc566-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="fc566-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc566-110">PARAMETERS</span></span>

### <span data-ttu-id="fc566-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc566-111">-DefaultProfile</span></span>
<span data-ttu-id="fc566-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc566-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc566-113">-已啟用</span><span class="sxs-lookup"><span data-stu-id="fc566-113">-Enabled</span></span>
<span data-ttu-id="fc566-114">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="fc566-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="fc566-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="fc566-115">-MaxThreshold</span></span>
<span data-ttu-id="fc566-116">最大閥值。</span><span class="sxs-lookup"><span data-stu-id="fc566-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="fc566-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="fc566-117">-MinThreshold</span></span>
<span data-ttu-id="fc566-118">最低閾值。</span><span class="sxs-lookup"><span data-stu-id="fc566-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="fc566-119">-類型</span><span class="sxs-lookup"><span data-stu-id="fc566-119">-Type</span></span>
<span data-ttu-id="fc566-120">規則類型。</span><span class="sxs-lookup"><span data-stu-id="fc566-120">Rule type.</span></span>

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

### <span data-ttu-id="fc566-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc566-121">CommonParameters</span></span>
<span data-ttu-id="fc566-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc566-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc566-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc566-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc566-124">輸入</span><span class="sxs-lookup"><span data-stu-id="fc566-124">INPUTS</span></span>

### <span data-ttu-id="fc566-125">沒有</span><span class="sxs-lookup"><span data-stu-id="fc566-125">None</span></span>

## <span data-ttu-id="fc566-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fc566-126">OUTPUTS</span></span>

### <span data-ttu-id="fc566-127">Microsoft.Azure.Commands.security.models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="fc566-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="fc566-128">筆記</span><span class="sxs-lookup"><span data-stu-id="fc566-128">NOTES</span></span>

## <span data-ttu-id="fc566-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc566-129">RELATED LINKS</span></span>
