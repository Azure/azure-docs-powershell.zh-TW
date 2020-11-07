---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623415"
---
# <span data-ttu-id="1afff-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="1afff-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="1afff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1afff-102">SYNOPSIS</span></span>
<span data-ttu-id="1afff-103">移除前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="1afff-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1afff-104">句法</span><span class="sxs-lookup"><span data-stu-id="1afff-104">SYNTAX</span></span>

### <span data-ttu-id="1afff-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1afff-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afff-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afff-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1afff-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1afff-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1afff-108">說明</span><span class="sxs-lookup"><span data-stu-id="1afff-108">DESCRIPTION</span></span>
<span data-ttu-id="1afff-109">**AzureRmFrontDoor** Cmdlet 會在目前的訂閱底下移除前門負載平衡器</span><span class="sxs-lookup"><span data-stu-id="1afff-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="1afff-110">示例</span><span class="sxs-lookup"><span data-stu-id="1afff-110">EXAMPLES</span></span>

### <span data-ttu-id="1afff-111">範例1：在目前的訂閱下，移除資源群組 "rg1" 中的 [frontdoor1]。</span><span class="sxs-lookup"><span data-stu-id="1afff-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="1afff-112">在目前訂閱下的資源群組 "rg1" 中，移除 [frontdoor1]。</span><span class="sxs-lookup"><span data-stu-id="1afff-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="1afff-113">範例2：在目前的訂閱下，移除資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="1afff-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="1afff-114">在目前的訂閱下，移除資源群組 "rg1" 中的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="1afff-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="1afff-115">範例3：移除目前訂閱下的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="1afff-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="1afff-116">移除目前訂閱下的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="1afff-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="1afff-117">範例4：在目前的訂閱下，移除名稱為 "frontdoor1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="1afff-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="1afff-118">在目前的訂閱底下，移除名稱為 "frontdoor1" 的所有 FrontDoors。</span><span class="sxs-lookup"><span data-stu-id="1afff-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="1afff-119">參數</span><span class="sxs-lookup"><span data-stu-id="1afff-119">PARAMETERS</span></span>

### <span data-ttu-id="1afff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1afff-120">-DefaultProfile</span></span>
<span data-ttu-id="1afff-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1afff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1afff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1afff-122">-InputObject</span></span>
<span data-ttu-id="1afff-123">要刪除的前蓋物件。</span><span class="sxs-lookup"><span data-stu-id="1afff-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="1afff-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="1afff-124">-Name</span></span>
<span data-ttu-id="1afff-125">要刪除之前門的名稱。</span><span class="sxs-lookup"><span data-stu-id="1afff-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="1afff-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1afff-126">-PassThru</span></span>
<span data-ttu-id="1afff-127">如果指定) ，則傳回物件 (。</span><span class="sxs-lookup"><span data-stu-id="1afff-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="1afff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1afff-128">-ResourceGroupName</span></span>
<span data-ttu-id="1afff-129">前門所屬的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1afff-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="1afff-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1afff-130">-ResourceId</span></span>
<span data-ttu-id="1afff-131">要刪除之前門的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1afff-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1afff-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1afff-132">-Confirm</span></span>
<span data-ttu-id="1afff-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1afff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1afff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1afff-134">-WhatIf</span></span>
<span data-ttu-id="1afff-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1afff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1afff-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1afff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1afff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1afff-137">CommonParameters</span></span>
<span data-ttu-id="1afff-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1afff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1afff-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1afff-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1afff-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1afff-140">INPUTS</span></span>

### <span data-ttu-id="1afff-141">PSFrontDoor 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="1afff-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="1afff-142">System.object</span><span class="sxs-lookup"><span data-stu-id="1afff-142">System.String</span></span>

### <span data-ttu-id="1afff-143">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="1afff-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1afff-144">輸出</span><span class="sxs-lookup"><span data-stu-id="1afff-144">OUTPUTS</span></span>

### <span data-ttu-id="1afff-145">System.object</span><span class="sxs-lookup"><span data-stu-id="1afff-145">System.Boolean</span></span>

## <span data-ttu-id="1afff-146">筆記</span><span class="sxs-lookup"><span data-stu-id="1afff-146">NOTES</span></span>

## <span data-ttu-id="1afff-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="1afff-147">RELATED LINKS</span></span>

<span data-ttu-id="1afff-148">[新-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
[AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="1afff-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
