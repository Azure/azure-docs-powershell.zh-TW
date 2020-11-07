---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulegroupoverrideobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRuleGroupOverrideObject.md
ms.openlocfilehash: 6175b99f5da139344c351189db5fbc5a13a137c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787785"
---
# <span data-ttu-id="ff302-101">New-AzFrontDoorRuleGroupOverrideObject</span><span class="sxs-lookup"><span data-stu-id="ff302-101">New-AzFrontDoorRuleGroupOverrideObject</span></span>

## <span data-ttu-id="ff302-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff302-102">SYNOPSIS</span></span>
<span data-ttu-id="ff302-103">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="ff302-103">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="ff302-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff302-104">SYNTAX</span></span>

```
New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName <String>
 [-ManagedRuleOverride <PSAzureManagedRuleOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff302-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff302-105">DESCRIPTION</span></span>
<span data-ttu-id="ff302-106">建立 WAF 原則建立的 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="ff302-106">Create RuleGroupOverride Object for WAF policy creation</span></span>

## <span data-ttu-id="ff302-107">示例</span><span class="sxs-lookup"><span data-stu-id="ff302-107">EXAMPLES</span></span>

### <span data-ttu-id="ff302-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ff302-108">Example 1</span></span>
```powershell
PS C:\> $ruleOverride1 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942250" -Action Log -EnabledState Enabled
PS C:\> $ruleOverride2 = New-AzFrontDoorManagedRuleOverrideObject -RuleId "942251" -Action Log -EnabledState Enabled

PS C:\> New-AzFrontDoorRuleGroupOverrideObject -RuleGroupName SQLI -ManagedRuleOverride $ruleOverride1,$ruleOverride2

RuleGroupName ManagedRuleOverrides
------------- --------------------
SQLI          {942250, 942251}
```

<span data-ttu-id="ff302-109">建立 RuleGroupOverride 物件</span><span class="sxs-lookup"><span data-stu-id="ff302-109">Create a RuleGroupOverride Object</span></span>

## <span data-ttu-id="ff302-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff302-110">PARAMETERS</span></span>

### <span data-ttu-id="ff302-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff302-111">-DefaultProfile</span></span>
<span data-ttu-id="ff302-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff302-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff302-113">-ManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="ff302-113">-ManagedRuleOverride</span></span>
<span data-ttu-id="ff302-114">規則覆寫清單</span><span class="sxs-lookup"><span data-stu-id="ff302-114">Rule override list</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff302-115">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="ff302-115">-RuleGroupName</span></span>
<span data-ttu-id="ff302-116">這些覆蓋適用的規則組名</span><span class="sxs-lookup"><span data-stu-id="ff302-116">Rule Group Name for which these overrides apply</span></span>

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

### <span data-ttu-id="ff302-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff302-117">CommonParameters</span></span>
<span data-ttu-id="ff302-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff302-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff302-119">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ff302-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff302-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ff302-120">INPUTS</span></span>

### <span data-ttu-id="ff302-121">所有</span><span class="sxs-lookup"><span data-stu-id="ff302-121">None</span></span>

## <span data-ttu-id="ff302-122">輸出</span><span class="sxs-lookup"><span data-stu-id="ff302-122">OUTPUTS</span></span>

### <span data-ttu-id="ff302-123">PSAzureRuleGroupOverride 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="ff302-123">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride</span></span>

## <span data-ttu-id="ff302-124">筆記</span><span class="sxs-lookup"><span data-stu-id="ff302-124">NOTES</span></span>

## <span data-ttu-id="ff302-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff302-125">RELATED LINKS</span></span>

[<span data-ttu-id="ff302-126">新-AzFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ff302-126">New-AzFrontDoorManagedRuleObject</span></span>](./New-AzFrontDoorManagedRuleObject.md)
