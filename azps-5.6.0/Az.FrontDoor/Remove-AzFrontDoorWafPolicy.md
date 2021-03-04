---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 707f3157cead45d501cdfdaf357222cdaceac826
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917729"
---
# <span data-ttu-id="74399-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="74399-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="74399-102">簡介</span><span class="sxs-lookup"><span data-stu-id="74399-102">SYNOPSIS</span></span>
<span data-ttu-id="74399-103">移除 WAF 政策</span><span class="sxs-lookup"><span data-stu-id="74399-103">Remove WAF policy</span></span>

## <span data-ttu-id="74399-104">語法</span><span class="sxs-lookup"><span data-stu-id="74399-104">SYNTAX</span></span>

### <span data-ttu-id="74399-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74399-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74399-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="74399-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74399-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="74399-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74399-108">描述</span><span class="sxs-lookup"><span data-stu-id="74399-108">DESCRIPTION</span></span>
<span data-ttu-id="74399-109">**Remove-AzFrontDoorWafPolicy** Cmdlet 會移除目前訂閱下的 WAF 策略</span><span class="sxs-lookup"><span data-stu-id="74399-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="74399-110">例子</span><span class="sxs-lookup"><span data-stu-id="74399-110">EXAMPLES</span></span>

### <span data-ttu-id="74399-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="74399-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="74399-112">在 $policyName 移除稱為 $resourceGroupName 的 WAF $resourceGroupName。</span><span class="sxs-lookup"><span data-stu-id="74399-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="74399-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="74399-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="74399-114">移除所有 WAF $resourceGroupName。</span><span class="sxs-lookup"><span data-stu-id="74399-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="74399-115">參數</span><span class="sxs-lookup"><span data-stu-id="74399-115">PARAMETERS</span></span>

### <span data-ttu-id="74399-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74399-116">-DefaultProfile</span></span>
<span data-ttu-id="74399-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="74399-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74399-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74399-118">-InputObject</span></span>
<span data-ttu-id="74399-119">要刪除的 WAF 策略物件。</span><span class="sxs-lookup"><span data-stu-id="74399-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74399-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="74399-120">-Name</span></span>
<span data-ttu-id="74399-121">要刪除的 WAF 策略名稱。</span><span class="sxs-lookup"><span data-stu-id="74399-121">The name of the WAF policy to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74399-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74399-122">-PassThru</span></span>
<span data-ttu-id="74399-123">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="74399-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="74399-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74399-124">-ResourceGroupName</span></span>
<span data-ttu-id="74399-125">WAF 策略所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="74399-125">The resource group to which the WAF policy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74399-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74399-126">-ResourceId</span></span>
<span data-ttu-id="74399-127">要刪除的 WAF 策略資源識別碼</span><span class="sxs-lookup"><span data-stu-id="74399-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74399-128">-確認</span><span class="sxs-lookup"><span data-stu-id="74399-128">-Confirm</span></span>
<span data-ttu-id="74399-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="74399-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74399-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74399-130">-WhatIf</span></span>
<span data-ttu-id="74399-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74399-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74399-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74399-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74399-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74399-133">CommonParameters</span></span>
<span data-ttu-id="74399-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="74399-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74399-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74399-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74399-136">輸入</span><span class="sxs-lookup"><span data-stu-id="74399-136">INPUTS</span></span>

### <span data-ttu-id="74399-137">Microsoft.Azure.Commands.FrontDoor.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="74399-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="74399-138">System.String</span><span class="sxs-lookup"><span data-stu-id="74399-138">System.String</span></span>

## <span data-ttu-id="74399-139">輸出</span><span class="sxs-lookup"><span data-stu-id="74399-139">OUTPUTS</span></span>

### <span data-ttu-id="74399-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="74399-140">System.Boolean</span></span>

## <span data-ttu-id="74399-141">筆記</span><span class="sxs-lookup"><span data-stu-id="74399-141">NOTES</span></span>

## <span data-ttu-id="74399-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="74399-142">RELATED LINKS</span></span>

<span data-ttu-id="74399-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="74399-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
