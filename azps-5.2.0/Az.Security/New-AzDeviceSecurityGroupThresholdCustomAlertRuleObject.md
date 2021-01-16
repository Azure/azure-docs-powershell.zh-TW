---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject.md
ms.openlocfilehash: 848882438cfe41a8c736bfcde780aa0421f73a68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277687"
---
# <span data-ttu-id="73f13-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="73f13-101">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject</span></span>

## <span data-ttu-id="73f13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73f13-102">SYNOPSIS</span></span>
<span data-ttu-id="73f13-103">為裝置安全性群組 (IoT 安全性) 建立新的閾值自訂警示規則</span><span class="sxs-lookup"><span data-stu-id="73f13-103">Create new threshold custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="73f13-104">句法</span><span class="sxs-lookup"><span data-stu-id="73f13-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold <Int32> -MaxThreshold <Int32>
 -Enabled <Boolean> -Type <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73f13-105">說明</span><span class="sxs-lookup"><span data-stu-id="73f13-105">DESCRIPTION</span></span>
<span data-ttu-id="73f13-106">New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject Cmdlet 會針對 IoT security 解決方案中的 device security 群組建立新的閾值自訂警報規則清單。</span><span class="sxs-lookup"><span data-stu-id="73f13-106">The New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject cmdlet creates a new list of threshold custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="73f13-107">示例</span><span class="sxs-lookup"><span data-stu-id="73f13-107">EXAMPLES</span></span>

### <span data-ttu-id="73f13-108">範例1</span><span class="sxs-lookup"><span data-stu-id="73f13-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupThresholdCustomAlertRuleObject -MinThreshold 0 -MaxThreshold 10 -Enabled $true -Type "SomeRuleType"

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
MinThreshold: 0
MaxThreshold: 10
```

<span data-ttu-id="73f13-109">從類型 "SomeRuleType" 建立新的閾值自訂警示規則，並啟用狀態為 [最小] 和 [最大閾值] 的 ant 值</span><span class="sxs-lookup"><span data-stu-id="73f13-109">Create new threshold custom alert rule from type "SomeRuleType" with status enabled ant values for minimum and maximum threshold</span></span>

## <span data-ttu-id="73f13-110">參數</span><span class="sxs-lookup"><span data-stu-id="73f13-110">PARAMETERS</span></span>

### <span data-ttu-id="73f13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f13-111">-DefaultProfile</span></span>
<span data-ttu-id="73f13-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73f13-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f13-113">-啟用</span><span class="sxs-lookup"><span data-stu-id="73f13-113">-Enabled</span></span>
<span data-ttu-id="73f13-114">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="73f13-114">Is rule enabled.</span></span>

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

### <span data-ttu-id="73f13-115">-MaxThreshold</span><span class="sxs-lookup"><span data-stu-id="73f13-115">-MaxThreshold</span></span>
<span data-ttu-id="73f13-116">最大閾值。</span><span class="sxs-lookup"><span data-stu-id="73f13-116">Maximum threshold.</span></span>

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

### <span data-ttu-id="73f13-117">-MinThreshold</span><span class="sxs-lookup"><span data-stu-id="73f13-117">-MinThreshold</span></span>
<span data-ttu-id="73f13-118">[最小值]。</span><span class="sxs-lookup"><span data-stu-id="73f13-118">Minimum threshold.</span></span>

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

### <span data-ttu-id="73f13-119">-類型</span><span class="sxs-lookup"><span data-stu-id="73f13-119">-Type</span></span>
<span data-ttu-id="73f13-120">規則類型。</span><span class="sxs-lookup"><span data-stu-id="73f13-120">Rule type.</span></span>

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

### <span data-ttu-id="73f13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f13-121">CommonParameters</span></span>
<span data-ttu-id="73f13-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73f13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f13-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="73f13-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f13-124">輸入</span><span class="sxs-lookup"><span data-stu-id="73f13-124">INPUTS</span></span>

### <span data-ttu-id="73f13-125">所有</span><span class="sxs-lookup"><span data-stu-id="73f13-125">None</span></span>

## <span data-ttu-id="73f13-126">輸出</span><span class="sxs-lookup"><span data-stu-id="73f13-126">OUTPUTS</span></span>

### <span data-ttu-id="73f13-127">PSThresholdCustomAlertRule 中的 DeviceSecurityGroups （Security..。</span><span class="sxs-lookup"><span data-stu-id="73f13-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule</span></span>

## <span data-ttu-id="73f13-128">筆記</span><span class="sxs-lookup"><span data-stu-id="73f13-128">NOTES</span></span>

## <span data-ttu-id="73f13-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="73f13-129">RELATED LINKS</span></span>
