---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafmanagedruleoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafManagedRuleOverrideObject.md
ms.openlocfilehash: 7fc4a16e6668af017e9666999eabe710b40e7d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129516"
---
# <span data-ttu-id="9c527-101">New-AzFrontDoorWafManagedRuleOverrideObject</span><span class="sxs-lookup"><span data-stu-id="9c527-101">New-AzFrontDoorWafManagedRuleOverrideObject</span></span>

## <span data-ttu-id="9c527-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c527-102">SYNOPSIS</span></span>
<span data-ttu-id="9c527-103">建立受管理的規則覆寫物件</span><span class="sxs-lookup"><span data-stu-id="9c527-103">Create managed rule override object</span></span>

## <span data-ttu-id="9c527-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c527-104">SYNTAX</span></span>

```
New-AzFrontDoorWafManagedRuleOverrideObject -RuleId <String> [-Action <String>] [-Disabled]
 [-Exclusion <PSManagedRuleExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c527-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c527-105">DESCRIPTION</span></span>
<span data-ttu-id="9c527-106">為 managed WAF 規則群組建立 PSAzureManagedRuleOverride 物件，以覆寫物件建立。</span><span class="sxs-lookup"><span data-stu-id="9c527-106">Create PSAzureManagedRuleOverride Object for managed WAF rule group override object creation.</span></span>

## <span data-ttu-id="9c527-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c527-107">EXAMPLES</span></span>

### <span data-ttu-id="9c527-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9c527-108">Example 1</span></span>
<span data-ttu-id="9c527-109">針對 SQLI 群組) 中的規則 942250 (建立受管理的規則覆寫物件。</span><span class="sxs-lookup"><span data-stu-id="9c527-109">Create a managed rule override object for rule 942250 (which is in SQLI group).</span></span>

```powershell
PS C:\> New-AzFrontDoorWafManagedRuleOverrideObject -RuleId "942250" -Action Log

RuleId EnabledState Action
------ ------------ ------
942250      Enabled    Log
```

## <span data-ttu-id="9c527-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c527-110">PARAMETERS</span></span>

### <span data-ttu-id="9c527-111">-動作</span><span class="sxs-lookup"><span data-stu-id="9c527-111">-Action</span></span>
<span data-ttu-id="9c527-112">覆寫動作</span><span class="sxs-lookup"><span data-stu-id="9c527-112">Override Action</span></span>

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

### <span data-ttu-id="9c527-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c527-113">-DefaultProfile</span></span>
<span data-ttu-id="9c527-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c527-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c527-115">-已停用</span><span class="sxs-lookup"><span data-stu-id="9c527-115">-Disabled</span></span>
<span data-ttu-id="9c527-116">停用狀態</span><span class="sxs-lookup"><span data-stu-id="9c527-116">Disabled state</span></span>

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

### <span data-ttu-id="9c527-117">-排除</span><span class="sxs-lookup"><span data-stu-id="9c527-117">-Exclusion</span></span>
<span data-ttu-id="9c527-118">他</span><span class="sxs-lookup"><span data-stu-id="9c527-118">Exclusion</span></span>

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

### <span data-ttu-id="9c527-119">-RuleId</span><span class="sxs-lookup"><span data-stu-id="9c527-119">-RuleId</span></span>
<span data-ttu-id="9c527-120">規則識別碼</span><span class="sxs-lookup"><span data-stu-id="9c527-120">Rule ID</span></span>

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

### <span data-ttu-id="9c527-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c527-121">CommonParameters</span></span>
<span data-ttu-id="9c527-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c527-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c527-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9c527-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c527-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9c527-124">INPUTS</span></span>

### <span data-ttu-id="9c527-125">所有</span><span class="sxs-lookup"><span data-stu-id="9c527-125">None</span></span>

## <span data-ttu-id="9c527-126">輸出</span><span class="sxs-lookup"><span data-stu-id="9c527-126">OUTPUTS</span></span>

### <span data-ttu-id="9c527-127">PSAzureManagedRuleOverride 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="9c527-127">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride</span></span>

## <span data-ttu-id="9c527-128">筆記</span><span class="sxs-lookup"><span data-stu-id="9c527-128">NOTES</span></span>

## <span data-ttu-id="9c527-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c527-129">RELATED LINKS</span></span>

[<span data-ttu-id="9c527-130">新-AzFrontDoorWafRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="9c527-130">New-AzFrontDoorWafRuleGroupOverrideObject</span></span>](./New-AzFrontDoorWafRuleGroupOverrideObject.md)