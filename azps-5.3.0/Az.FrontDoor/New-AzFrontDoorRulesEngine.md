---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 9f01a17bfe9e3e499e2bac2953f1cccc2af56c41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438411"
---
# <span data-ttu-id="cf54f-101">New-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="cf54f-101">New-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="cf54f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf54f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf54f-103">針對指定的前門建立新的規則引擎配置。</span><span class="sxs-lookup"><span data-stu-id="cf54f-103">Create a new rules engine configuration for a specified front door.</span></span> 

## <span data-ttu-id="cf54f-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf54f-104">SYNTAX</span></span>

```
New-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 [-Rule <PSRulesEngineRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf54f-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf54f-105">DESCRIPTION</span></span>
<span data-ttu-id="cf54f-106">針對指定的前門建立新的規則引擎配置。</span><span class="sxs-lookup"><span data-stu-id="cf54f-106">Create a new rules engine configuration for a specified front door.</span></span> 

<span data-ttu-id="cf54f-107">使用 Cmdlet "New-AzFrontDoorRulesEngineRule" 來構造規則引擎規則，以傳遞到此 Cmdlet 的 "-Rules" 參數。</span><span class="sxs-lookup"><span data-stu-id="cf54f-107">Use cmdlet "New-AzFrontDoorRulesEngineRule" to construct rules engine rules to pass into the "-Rules" parameter of this cmdlet.</span></span>

## <span data-ttu-id="cf54f-108">示例</span><span class="sxs-lookup"><span data-stu-id="cf54f-108">EXAMPLES</span></span>

### <span data-ttu-id="cf54f-109">範例1</span><span class="sxs-lookup"><span data-stu-id="cf54f-109">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name myRulesEngine -Rule $rulesEngineRule1

Name          RulesEngineRules
----          ----------------
myRulesEngine {rules1}
```

<span data-ttu-id="cf54f-110">針對指定的前門建立新的規則引擎配置。</span><span class="sxs-lookup"><span data-stu-id="cf54f-110">Create a new rules engine configuration for specified front door.</span></span>

## <span data-ttu-id="cf54f-111">參數</span><span class="sxs-lookup"><span data-stu-id="cf54f-111">PARAMETERS</span></span>

### <span data-ttu-id="cf54f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf54f-112">-DefaultProfile</span></span>
<span data-ttu-id="cf54f-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf54f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf54f-114">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="cf54f-114">-FrontDoorName</span></span>
<span data-ttu-id="cf54f-115">前門名稱。</span><span class="sxs-lookup"><span data-stu-id="cf54f-115">Front Door name.</span></span>

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

### <span data-ttu-id="cf54f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf54f-116">-Name</span></span>
<span data-ttu-id="cf54f-117">規則引擎名稱。</span><span class="sxs-lookup"><span data-stu-id="cf54f-117">Rules engine name.</span></span>

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

### <span data-ttu-id="cf54f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf54f-118">-ResourceGroupName</span></span>
<span data-ttu-id="cf54f-119">在其中建立前蓋的資源群組名稱。</span><span class="sxs-lookup"><span data-stu-id="cf54f-119">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="cf54f-120">-規則</span><span class="sxs-lookup"><span data-stu-id="cf54f-120">-Rule</span></span>
<span data-ttu-id="cf54f-121">定義特定規則引擎配置的規則清單。</span><span class="sxs-lookup"><span data-stu-id="cf54f-121">A list of rules that define a particular Rules Engine Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngineRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf54f-122">-確認</span><span class="sxs-lookup"><span data-stu-id="cf54f-122">-Confirm</span></span>
<span data-ttu-id="cf54f-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf54f-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf54f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf54f-124">-WhatIf</span></span>
<span data-ttu-id="cf54f-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf54f-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf54f-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf54f-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf54f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf54f-127">CommonParameters</span></span>
<span data-ttu-id="cf54f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf54f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf54f-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf54f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf54f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cf54f-130">INPUTS</span></span>

### <span data-ttu-id="cf54f-131">所有</span><span class="sxs-lookup"><span data-stu-id="cf54f-131">None</span></span>

## <span data-ttu-id="cf54f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cf54f-132">OUTPUTS</span></span>

### <span data-ttu-id="cf54f-133">PSRulesEngine 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="cf54f-133">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="cf54f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cf54f-134">NOTES</span></span>

## <span data-ttu-id="cf54f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf54f-135">RELATED LINKS</span></span>
