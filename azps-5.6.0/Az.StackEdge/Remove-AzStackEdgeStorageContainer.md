---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 6a07031c376e406be1d957a33475af799b229b8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915729"
---
# <span data-ttu-id="ec66a-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec66a-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="ec66a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec66a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec66a-103">移除裝置上 Edge 儲存空間帳戶的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="ec66a-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="ec66a-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec66a-104">SYNTAX</span></span>

### <span data-ttu-id="ec66a-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ec66a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec66a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec66a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec66a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec66a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec66a-108">描述</span><span class="sxs-lookup"><span data-stu-id="ec66a-108">DESCRIPTION</span></span>
<span data-ttu-id="ec66a-109">**Remove-AzStackEdgeStorageContainer Cmdlet** 會移除堆疊 Edge 裝置上 Edge 儲存空間帳戶的相關儲存容器。</span><span class="sxs-lookup"><span data-stu-id="ec66a-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="ec66a-110">您可以指定要移除的儲存容器名稱做為參數。</span><span class="sxs-lookup"><span data-stu-id="ec66a-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="ec66a-111">例子</span><span class="sxs-lookup"><span data-stu-id="ec66a-111">EXAMPLES</span></span>

### <span data-ttu-id="ec66a-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="ec66a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="ec66a-113">參數</span><span class="sxs-lookup"><span data-stu-id="ec66a-113">PARAMETERS</span></span>

### <span data-ttu-id="ec66a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec66a-114">-AsJob</span></span>
<span data-ttu-id="ec66a-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec66a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec66a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec66a-116">-DefaultProfile</span></span>
<span data-ttu-id="ec66a-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec66a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec66a-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ec66a-118">-DeviceName</span></span>
<span data-ttu-id="ec66a-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="ec66a-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec66a-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ec66a-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="ec66a-121">提供現有的 EdgeStorageAccount名稱</span><span class="sxs-lookup"><span data-stu-id="ec66a-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec66a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec66a-122">-InputObject</span></span>
<span data-ttu-id="ec66a-123">輸入物件</span><span class="sxs-lookup"><span data-stu-id="ec66a-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec66a-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec66a-124">-Name</span></span>
<span data-ttu-id="ec66a-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ec66a-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec66a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec66a-126">-PassThru</span></span>
<span data-ttu-id="ec66a-127">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="ec66a-127">returns true if successful</span></span>

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

### <span data-ttu-id="ec66a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec66a-128">-ResourceGroupName</span></span>
<span data-ttu-id="ec66a-129">資源組名</span><span class="sxs-lookup"><span data-stu-id="ec66a-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec66a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec66a-130">-ResourceId</span></span>
<span data-ttu-id="ec66a-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec66a-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec66a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ec66a-132">-Confirm</span></span>
<span data-ttu-id="ec66a-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ec66a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec66a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec66a-134">-WhatIf</span></span>
<span data-ttu-id="ec66a-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec66a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec66a-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec66a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec66a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec66a-137">CommonParameters</span></span>
<span data-ttu-id="ec66a-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec66a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec66a-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec66a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec66a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ec66a-140">INPUTS</span></span>

### <span data-ttu-id="ec66a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ec66a-141">System.String</span></span>

### <span data-ttu-id="ec66a-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ec66a-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="ec66a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ec66a-143">OUTPUTS</span></span>

### <span data-ttu-id="ec66a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ec66a-144">System.Boolean</span></span>

## <span data-ttu-id="ec66a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ec66a-145">NOTES</span></span>

## <span data-ttu-id="ec66a-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec66a-146">RELATED LINKS</span></span>
