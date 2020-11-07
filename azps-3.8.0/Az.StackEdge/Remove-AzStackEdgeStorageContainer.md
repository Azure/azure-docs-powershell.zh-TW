---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageContainer.md
ms.openlocfilehash: c1e76da1fc01ea1698c56e40fd3bd46f6378ea07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959847"
---
# <span data-ttu-id="14b3c-101">Remove-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="14b3c-101">Remove-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="14b3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="14b3c-103">移除裝置上 Edge 儲存空間帳戶的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="14b3c-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="14b3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="14b3c-104">SYNTAX</span></span>

### <span data-ttu-id="14b3c-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14b3c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b3c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b3c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14b3c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14b3c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageContainer -InputObject <PSStackEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14b3c-108">說明</span><span class="sxs-lookup"><span data-stu-id="14b3c-108">DESCRIPTION</span></span>
<span data-ttu-id="14b3c-109">**AzStackEdgeStorageContainer** Cmdlet 會移除堆疊 edge 裝置上 Edge 儲存空間帳戶的關聯儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="14b3c-109">The **Remove-AzStackEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="14b3c-110">您可以指定要移除的儲存空間容器名稱作為參數。</span><span class="sxs-lookup"><span data-stu-id="14b3c-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="14b3c-111">示例</span><span class="sxs-lookup"><span data-stu-id="14b3c-111">EXAMPLES</span></span>

### <span data-ttu-id="14b3c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="14b3c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="14b3c-113">參數</span><span class="sxs-lookup"><span data-stu-id="14b3c-113">PARAMETERS</span></span>

### <span data-ttu-id="14b3c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14b3c-114">-AsJob</span></span>
<span data-ttu-id="14b3c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="14b3c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14b3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b3c-116">-DefaultProfile</span></span>
<span data-ttu-id="14b3c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14b3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b3c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="14b3c-118">-DeviceName</span></span>
<span data-ttu-id="14b3c-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="14b3c-119">Device Name</span></span>

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

### <span data-ttu-id="14b3c-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="14b3c-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="14b3c-121">提供現有 EdgeStorageAccount 的名稱</span><span class="sxs-lookup"><span data-stu-id="14b3c-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="14b3c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14b3c-122">-InputObject</span></span>
<span data-ttu-id="14b3c-123">輸入物件</span><span class="sxs-lookup"><span data-stu-id="14b3c-123">Input Object</span></span>

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

### <span data-ttu-id="14b3c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="14b3c-124">-Name</span></span>
<span data-ttu-id="14b3c-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="14b3c-125">Resource Name</span></span>

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

### <span data-ttu-id="14b3c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14b3c-126">-PassThru</span></span>
<span data-ttu-id="14b3c-127">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="14b3c-127">returns true if successful</span></span>

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

### <span data-ttu-id="14b3c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14b3c-128">-ResourceGroupName</span></span>
<span data-ttu-id="14b3c-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="14b3c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="14b3c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14b3c-130">-ResourceId</span></span>
<span data-ttu-id="14b3c-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="14b3c-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="14b3c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="14b3c-132">-Confirm</span></span>
<span data-ttu-id="14b3c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="14b3c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14b3c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14b3c-134">-WhatIf</span></span>
<span data-ttu-id="14b3c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14b3c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14b3c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14b3c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14b3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b3c-137">CommonParameters</span></span>
<span data-ttu-id="14b3c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14b3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b3c-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14b3c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b3c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="14b3c-140">INPUTS</span></span>

### <span data-ttu-id="14b3c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="14b3c-141">System.String</span></span>

### <span data-ttu-id="14b3c-142">PSStackEdgeStorageContainer （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="14b3c-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="14b3c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="14b3c-143">OUTPUTS</span></span>

### <span data-ttu-id="14b3c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="14b3c-144">System.Boolean</span></span>

## <span data-ttu-id="14b3c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="14b3c-145">NOTES</span></span>

## <span data-ttu-id="14b3c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="14b3c-146">RELATED LINKS</span></span>
