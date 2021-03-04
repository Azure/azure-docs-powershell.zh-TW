---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject.md
ms.openlocfilehash: 0b915176858c0641ca3076ea10022ae193718807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908741"
---
# <span data-ttu-id="4807a-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span><span class="sxs-lookup"><span data-stu-id="4807a-101">New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject</span></span>

## <span data-ttu-id="4807a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4807a-102">SYNOPSIS</span></span>
<span data-ttu-id="4807a-103">為裝置安全性群組建立新的拒絕清單自訂提醒規則 (IoT 安全性) </span><span class="sxs-lookup"><span data-stu-id="4807a-103">Create new deny list custom alert rule for device security group (IoT Security)</span></span>

## <span data-ttu-id="4807a-104">語法</span><span class="sxs-lookup"><span data-stu-id="4807a-104">SYNTAX</span></span>

```
New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled <Boolean> -Type <String>
 -DenylistValue <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4807a-105">描述</span><span class="sxs-lookup"><span data-stu-id="4807a-105">DESCRIPTION</span></span>
<span data-ttu-id="4807a-106">Cmdlet New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject在 IoT 安全性解決方案中為裝置安全性群組建立一份拒絕自訂通知規則的新清單。</span><span class="sxs-lookup"><span data-stu-id="4807a-106">The New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject cmdlet creates a new list of denyed custom alert rules for device security group in IoT security solution.</span></span>

## <span data-ttu-id="4807a-107">例子</span><span class="sxs-lookup"><span data-stu-id="4807a-107">EXAMPLES</span></span>

### <span data-ttu-id="4807a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4807a-108">Example 1</span></span>
```powershell
PS C:\> New-AzDeviceSecurityGroupDenylistCustomAlertRuleObject -Enabled $false -Type "SomeRuleType" -DenylistValue @()

RuleType: "SomeRuleType"
DisplayName: "Display name for some rule type"
Description: "Description for some rule type"
IsEnabled: false
ValueType: "String"
DenylistValues: []
```

<span data-ttu-id="4807a-109">使用 rull 類型 "SomeRuleType" 建立新拒絕清單自訂提醒規則，且狀態設定為可取消</span><span class="sxs-lookup"><span data-stu-id="4807a-109">Create new deny list custom alert rule with rull type "SomeRuleType" and status set to desable</span></span>

## <span data-ttu-id="4807a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4807a-110">PARAMETERS</span></span>

### <span data-ttu-id="4807a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4807a-111">-DefaultProfile</span></span>
<span data-ttu-id="4807a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4807a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4807a-113">-DenylistValue</span><span class="sxs-lookup"><span data-stu-id="4807a-113">-DenylistValue</span></span>
<span data-ttu-id="4807a-114">拒絕清單值。</span><span class="sxs-lookup"><span data-stu-id="4807a-114">Deny list values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4807a-115">-已啟用</span><span class="sxs-lookup"><span data-stu-id="4807a-115">-Enabled</span></span>
<span data-ttu-id="4807a-116">已啟用規則。</span><span class="sxs-lookup"><span data-stu-id="4807a-116">Is rule enabled.</span></span>

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

### <span data-ttu-id="4807a-117">-類型</span><span class="sxs-lookup"><span data-stu-id="4807a-117">-Type</span></span>
<span data-ttu-id="4807a-118">規則類型。</span><span class="sxs-lookup"><span data-stu-id="4807a-118">Rule type.</span></span>

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

### <span data-ttu-id="4807a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4807a-119">CommonParameters</span></span>
<span data-ttu-id="4807a-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4807a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4807a-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4807a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4807a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4807a-122">INPUTS</span></span>

### <span data-ttu-id="4807a-123">沒有</span><span class="sxs-lookup"><span data-stu-id="4807a-123">None</span></span>

## <span data-ttu-id="4807a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4807a-124">OUTPUTS</span></span>

### <span data-ttu-id="4807a-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span><span class="sxs-lookup"><span data-stu-id="4807a-125">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule</span></span>

## <span data-ttu-id="4807a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4807a-126">NOTES</span></span>

## <span data-ttu-id="4807a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4807a-127">RELATED LINKS</span></span>
