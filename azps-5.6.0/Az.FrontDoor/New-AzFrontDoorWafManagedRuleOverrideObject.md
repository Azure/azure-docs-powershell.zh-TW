---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: ee4193fff69e8b46362ac75019cc76178001c2e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906634"
---
# <span data-ttu-id="4e72d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="4e72d-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="4e72d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e72d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e72d-103">建立受管理規則重寫物件</span><span class="sxs-lookup"><span data-stu-id="4e72d-103">Create managed rule override object</span></span>

## <span data-ttu-id="4e72d-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e72d-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e72d-105">描述</span><span class="sxs-lookup"><span data-stu-id="4e72d-105">DESCRIPTION</span></span>
<span data-ttu-id="4e72d-106">為受管理的 WAF 規則群組建立 PSAzureManagedRuleOverride 物件以覆蓋物件建立。</span><span class="sxs-lookup"><span data-stu-id="4e72d-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="4e72d-107">例子</span><span class="sxs-lookup"><span data-stu-id="4e72d-107">EXAMPLES</span></span>

### <span data-ttu-id="4e72d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4e72d-108">Example 1</span></span>
<span data-ttu-id="4e72d-109">建立規則 942250 的受管理規則 (物件，該物件位於 SQLI 群組) 。</span><span class="sxs-lookup"><span data-stu-id="4e72d-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="4e72d-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e72d-110">PARAMETERS</span></span>

### <span data-ttu-id="4e72d-111">-動作</span><span class="sxs-lookup"><span data-stu-id="4e72d-111">-Action</span></span>
<span data-ttu-id="4e72d-112">重寫動作</span><span class="sxs-lookup"><span data-stu-id="4e72d-112">Override Action</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e72d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e72d-113">-DefaultProfile</span></span>
<span data-ttu-id="4e72d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e72d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e72d-115">-已停用</span><span class="sxs-lookup"><span data-stu-id="4e72d-115">-Disabled</span></span>
<span data-ttu-id="4e72d-116">已停用狀態</span><span class="sxs-lookup"><span data-stu-id="4e72d-116">Disabled state</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e72d-117">-排除</span><span class="sxs-lookup"><span data-stu-id="4e72d-117">-Exclusion</span></span>
<span data-ttu-id="4e72d-118">排除</span><span class="sxs-lookup"><span data-stu-id="4e72d-118">Exclusion</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRuleExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e72d-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="4e72d-119">-RuleId</span></span>
<span data-ttu-id="4e72d-120">規則識別碼</span><span class="sxs-lookup"><span data-stu-id="4e72d-120">Rule ID</span></span>

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

### <span data-ttu-id="4e72d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e72d-121">CommonParameters</span></span>
<span data-ttu-id="4e72d-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e72d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e72d-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e72d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e72d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4e72d-124">INPUTS</span></span>

### <span data-ttu-id="4e72d-125">沒有</span><span class="sxs-lookup"><span data-stu-id="4e72d-125">None</span></span>

## <span data-ttu-id="4e72d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4e72d-126">OUTPUTS</span></span>

### <span data-ttu-id="4e72d-127">Microsoft.Azure.Commands.FrontDoor.models.PSAzureManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4e72d-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="4e72d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4e72d-128">NOTES</span></span>

## <span data-ttu-id="4e72d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e72d-129">RELATED LINKS</span></span>

[<span data-ttu-id="4e72d-130">New-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="4e72d-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)