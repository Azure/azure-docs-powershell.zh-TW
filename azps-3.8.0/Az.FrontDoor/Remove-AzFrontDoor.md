---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956651"
---
# <span data-ttu-id="37f03-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="37f03-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="37f03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37f03-102">SYNOPSIS</span></span>
<span data-ttu-id="37f03-103">移除前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="37f03-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="37f03-104">句法</span><span class="sxs-lookup"><span data-stu-id="37f03-104">SYNTAX</span></span>

### <span data-ttu-id="37f03-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="37f03-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37f03-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37f03-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37f03-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37f03-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f03-108">說明</span><span class="sxs-lookup"><span data-stu-id="37f03-108">DESCRIPTION</span></span>
<span data-ttu-id="37f03-109">**AzFrontDoor** Cmdlet 會在目前的訂閱底下移除前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="37f03-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="37f03-110">示例</span><span class="sxs-lookup"><span data-stu-id="37f03-110">EXAMPLES</span></span>

### <span data-ttu-id="37f03-111">範例1：在目前的訂閱下，移除資源群組 "rg1" 中的 [frontdoor1]。</span><span class="sxs-lookup"><span data-stu-id="37f03-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="37f03-112">在目前訂閱下的資源群組 "rg1" 中，移除 [frontdoor1]。</span><span class="sxs-lookup"><span data-stu-id="37f03-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="37f03-113">範例2：在目前的訂閱下，移除資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="37f03-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="37f03-114">在目前的訂閱下，移除資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="37f03-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="37f03-115">範例3：移除目前訂閱下的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="37f03-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="37f03-116">移除目前訂閱下的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="37f03-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="37f03-117">範例4：在目前的訂閱下，移除名稱為 "frontdoor1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="37f03-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="37f03-118">在目前的訂閱底下，移除名稱為 "frontdoor1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="37f03-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="37f03-119">參數</span><span class="sxs-lookup"><span data-stu-id="37f03-119">PARAMETERS</span></span>

### <span data-ttu-id="37f03-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f03-120">-DefaultProfile</span></span>
<span data-ttu-id="37f03-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37f03-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37f03-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37f03-122">-InputObject</span></span>
<span data-ttu-id="37f03-123">要刪除的前蓋物件。</span><span class="sxs-lookup"><span data-stu-id="37f03-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="37f03-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="37f03-124">-Name</span></span>
<span data-ttu-id="37f03-125">要刪除之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="37f03-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="37f03-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37f03-126">-PassThru</span></span>
<span data-ttu-id="37f03-127">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="37f03-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="37f03-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f03-128">-ResourceGroupName</span></span>
<span data-ttu-id="37f03-129">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="37f03-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="37f03-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37f03-130">-ResourceId</span></span>
<span data-ttu-id="37f03-131">要刪除之前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="37f03-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="37f03-132">-確認</span><span class="sxs-lookup"><span data-stu-id="37f03-132">-Confirm</span></span>
<span data-ttu-id="37f03-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37f03-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f03-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f03-134">-WhatIf</span></span>
<span data-ttu-id="37f03-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37f03-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37f03-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37f03-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37f03-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f03-137">CommonParameters</span></span>
<span data-ttu-id="37f03-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37f03-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f03-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37f03-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f03-140">輸入</span><span class="sxs-lookup"><span data-stu-id="37f03-140">INPUTS</span></span>

### <span data-ttu-id="37f03-141">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="37f03-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="37f03-142">System.object</span><span class="sxs-lookup"><span data-stu-id="37f03-142">System.String</span></span>

## <span data-ttu-id="37f03-143">輸出</span><span class="sxs-lookup"><span data-stu-id="37f03-143">OUTPUTS</span></span>

### <span data-ttu-id="37f03-144">System.object</span><span class="sxs-lookup"><span data-stu-id="37f03-144">System.Boolean</span></span>

## <span data-ttu-id="37f03-145">筆記</span><span class="sxs-lookup"><span data-stu-id="37f03-145">NOTES</span></span>

## <span data-ttu-id="37f03-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="37f03-146">RELATED LINKS</span></span>

<span data-ttu-id="37f03-147">[新-AzFrontDoor](./New-AzFrontDoor.md) 
[AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="37f03-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>