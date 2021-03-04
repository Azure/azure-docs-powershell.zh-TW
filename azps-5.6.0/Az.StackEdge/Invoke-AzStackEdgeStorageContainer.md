---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/invoke-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeStorageContainer.md
ms.openlocfilehash: ce4c80146524f57e48570b9739f78635e3e21b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909425"
---
# <span data-ttu-id="ccb0c-101">Invoke-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ccb0c-101">Invoke-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="ccb0c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ccb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb0c-103">在儲存容器上啟動特定動作</span><span class="sxs-lookup"><span data-stu-id="ccb0c-103">Invokes specific actions on a storage container</span></span>

## <span data-ttu-id="ccb0c-104">語法</span><span class="sxs-lookup"><span data-stu-id="ccb0c-104">SYNTAX</span></span>

### <span data-ttu-id="ccb0c-105">InvokeByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ccb0c-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb0c-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccb0c-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-ResourceId] <String> [-RefreshData] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccb0c-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccb0c-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeStorageContainer [-RefreshData] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeStorageContainer> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccb0c-108">描述</span><span class="sxs-lookup"><span data-stu-id="ccb0c-108">DESCRIPTION</span></span>
<span data-ttu-id="ccb0c-109">**Invoke-AzStackEdgeStorageContainer Cmdlet** 會啟動動作來重新更新 Stack Edge 裝置上儲存容器上的資料。</span><span class="sxs-lookup"><span data-stu-id="ccb0c-109">The **Invoke-AzStackEdgeStorageContainer** cmdlet invokes actions to refresh the data on a storage container on a Stack Edge device.</span></span> 

## <span data-ttu-id="ccb0c-110">例子</span><span class="sxs-lookup"><span data-stu-id="ccb0c-110">EXAMPLES</span></span>

### <span data-ttu-id="ccb0c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ccb0c-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 -PassThru
PS C:\> true
```

### <span data-ttu-id="ccb0c-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="ccb0c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccount1 -Name container1 | Invoke-AzStackEdgeStorageContainer
```

## <span data-ttu-id="ccb0c-113">參數</span><span class="sxs-lookup"><span data-stu-id="ccb0c-113">PARAMETERS</span></span>

### <span data-ttu-id="ccb0c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccb0c-114">-AsJob</span></span>
<span data-ttu-id="ccb0c-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ccb0c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccb0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccb0c-116">-DefaultProfile</span></span>
<span data-ttu-id="ccb0c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ccb0c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccb0c-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ccb0c-118">-DeviceName</span></span>
<span data-ttu-id="ccb0c-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="ccb0c-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb0c-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ccb0c-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="ccb0c-121">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ccb0c-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb0c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccb0c-122">-InputObject</span></span>
<span data-ttu-id="ccb0c-123">提供現有的 EdgeStorageAccount 物件</span><span class="sxs-lookup"><span data-stu-id="ccb0c-123">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeStorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb0c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ccb0c-124">-Name</span></span>
<span data-ttu-id="ccb0c-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="ccb0c-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb0c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ccb0c-126">-PassThru</span></span>
<span data-ttu-id="ccb0c-127">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="ccb0c-127">returns true if successful</span></span>

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

### <span data-ttu-id="ccb0c-128">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="ccb0c-128">-RefreshData</span></span>
<span data-ttu-id="ccb0c-129">使用雲端資料重新組織容器中繼資料</span><span class="sxs-lookup"><span data-stu-id="ccb0c-129">Refresh Container Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="ccb0c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccb0c-130">-ResourceGroupName</span></span>
<span data-ttu-id="ccb0c-131">資源組名</span><span class="sxs-lookup"><span data-stu-id="ccb0c-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb0c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccb0c-132">-ResourceId</span></span>
<span data-ttu-id="ccb0c-133">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccb0c-133">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccb0c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ccb0c-134">-Confirm</span></span>
<span data-ttu-id="ccb0c-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ccb0c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccb0c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccb0c-136">-WhatIf</span></span>
<span data-ttu-id="ccb0c-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ccb0c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccb0c-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccb0c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccb0c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb0c-139">CommonParameters</span></span>
<span data-ttu-id="ccb0c-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ccb0c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb0c-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccb0c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb0c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ccb0c-142">INPUTS</span></span>

### <span data-ttu-id="ccb0c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ccb0c-143">System.String</span></span>

### <span data-ttu-id="ccb0c-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ccb0c-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="ccb0c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="ccb0c-145">OUTPUTS</span></span>

### <span data-ttu-id="ccb0c-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ccb0c-146">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="ccb0c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="ccb0c-147">NOTES</span></span>

## <span data-ttu-id="ccb0c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="ccb0c-148">RELATED LINKS</span></span>
