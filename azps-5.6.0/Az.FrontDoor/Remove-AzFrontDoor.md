---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 79307a12fbcf5be02d9ea356f41398f76e292379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917734"
---
# <span data-ttu-id="05351-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="05351-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="05351-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05351-102">SYNOPSIS</span></span>
<span data-ttu-id="05351-103">移除前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="05351-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="05351-104">語法</span><span class="sxs-lookup"><span data-stu-id="05351-104">SYNTAX</span></span>

### <span data-ttu-id="05351-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="05351-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05351-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05351-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05351-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05351-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05351-108">描述</span><span class="sxs-lookup"><span data-stu-id="05351-108">DESCRIPTION</span></span>
<span data-ttu-id="05351-109">**Remove-AzFrontDoor** Cmdlet 會移除目前訂閱下的前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="05351-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="05351-110">例子</span><span class="sxs-lookup"><span data-stu-id="05351-110">EXAMPLES</span></span>

### <span data-ttu-id="05351-111">範例 1：在目前訂閱下移除資源群組 "rg1" 中的"frontdoor1"。</span><span class="sxs-lookup"><span data-stu-id="05351-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="05351-112">移除目前訂閱下資源群組 "rg1" 中的「frontdoor1」。</span><span class="sxs-lookup"><span data-stu-id="05351-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="05351-113">範例 2：移除目前訂閱下資源群組 "rg1" 中所有的 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="05351-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="05351-114">移除目前訂閱下資源群組 "rg1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="05351-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="05351-115">範例 3：移除目前訂閱下的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="05351-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="05351-116">移除目前訂閱下的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="05351-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="05351-117">範例 4：移除目前訂閱下名稱為 "frontdoor1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="05351-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="05351-118">移除目前訂閱下名稱為「frontdoor1」的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="05351-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="05351-119">參數</span><span class="sxs-lookup"><span data-stu-id="05351-119">PARAMETERS</span></span>

### <span data-ttu-id="05351-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05351-120">-DefaultProfile</span></span>
<span data-ttu-id="05351-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05351-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05351-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05351-122">-InputObject</span></span>
<span data-ttu-id="05351-123">要刪除的門物件。</span><span class="sxs-lookup"><span data-stu-id="05351-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05351-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="05351-124">-Name</span></span>
<span data-ttu-id="05351-125">要刪除的門名稱。</span><span class="sxs-lookup"><span data-stu-id="05351-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="05351-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05351-126">-PassThru</span></span>
<span data-ttu-id="05351-127">如果指定 (，則) 。</span><span class="sxs-lookup"><span data-stu-id="05351-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="05351-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05351-128">-ResourceGroupName</span></span>
<span data-ttu-id="05351-129">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="05351-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="05351-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05351-130">-ResourceId</span></span>
<span data-ttu-id="05351-131">要刪除之前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="05351-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="05351-132">-確認</span><span class="sxs-lookup"><span data-stu-id="05351-132">-Confirm</span></span>
<span data-ttu-id="05351-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="05351-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05351-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05351-134">-WhatIf</span></span>
<span data-ttu-id="05351-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05351-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05351-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05351-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05351-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05351-137">CommonParameters</span></span>
<span data-ttu-id="05351-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05351-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05351-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05351-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05351-140">輸入</span><span class="sxs-lookup"><span data-stu-id="05351-140">INPUTS</span></span>

### <span data-ttu-id="05351-141">Microsoft.Azure.Commands.FrontDoor.models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="05351-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="05351-142">System.String</span><span class="sxs-lookup"><span data-stu-id="05351-142">System.String</span></span>

## <span data-ttu-id="05351-143">輸出</span><span class="sxs-lookup"><span data-stu-id="05351-143">OUTPUTS</span></span>

### <span data-ttu-id="05351-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05351-144">System.Boolean</span></span>

## <span data-ttu-id="05351-145">筆記</span><span class="sxs-lookup"><span data-stu-id="05351-145">NOTES</span></span>

## <span data-ttu-id="05351-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="05351-146">RELATED LINKS</span></span>

<span data-ttu-id="05351-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="05351-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>