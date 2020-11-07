---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966017"
---
# <span data-ttu-id="81e2b-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="81e2b-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="81e2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="81e2b-103">移除裝置上 Edge 儲存空間帳戶的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="81e2b-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="81e2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="81e2b-104">SYNTAX</span></span>

### <span data-ttu-id="81e2b-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="81e2b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e2b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e2b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81e2b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81e2b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81e2b-108">說明</span><span class="sxs-lookup"><span data-stu-id="81e2b-108">DESCRIPTION</span></span>
<span data-ttu-id="81e2b-109">**AzDataBoxEdgeStorageContainer** Cmdlet 會移除資料盒 edge 裝置上 Edge 儲存空間帳戶的關聯儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="81e2b-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="81e2b-110">您可以指定要移除的儲存空間容器名稱作為參數。</span><span class="sxs-lookup"><span data-stu-id="81e2b-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="81e2b-111">示例</span><span class="sxs-lookup"><span data-stu-id="81e2b-111">EXAMPLES</span></span>

### <span data-ttu-id="81e2b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="81e2b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="81e2b-113">參數</span><span class="sxs-lookup"><span data-stu-id="81e2b-113">PARAMETERS</span></span>

### <span data-ttu-id="81e2b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81e2b-114">-AsJob</span></span>
<span data-ttu-id="81e2b-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="81e2b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81e2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e2b-116">-DefaultProfile</span></span>
<span data-ttu-id="81e2b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81e2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81e2b-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="81e2b-118">-DeviceName</span></span>
<span data-ttu-id="81e2b-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="81e2b-119">Device Name</span></span>

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

### <span data-ttu-id="81e2b-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="81e2b-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="81e2b-121">提供現有 EdgeStorageAccount 的名稱</span><span class="sxs-lookup"><span data-stu-id="81e2b-121">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="81e2b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81e2b-122">-InputObject</span></span>
<span data-ttu-id="81e2b-123">輸入物件</span><span class="sxs-lookup"><span data-stu-id="81e2b-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81e2b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="81e2b-124">-Name</span></span>
<span data-ttu-id="81e2b-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="81e2b-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81e2b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81e2b-126">-PassThru</span></span>
<span data-ttu-id="81e2b-127">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="81e2b-127">returns true if successful</span></span>

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

### <span data-ttu-id="81e2b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e2b-128">-ResourceGroupName</span></span>
<span data-ttu-id="81e2b-129">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="81e2b-129">Resource Group Name</span></span>

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

### <span data-ttu-id="81e2b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e2b-130">-ResourceId</span></span>
<span data-ttu-id="81e2b-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="81e2b-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="81e2b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="81e2b-132">-Confirm</span></span>
<span data-ttu-id="81e2b-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81e2b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e2b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e2b-134">-WhatIf</span></span>
<span data-ttu-id="81e2b-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81e2b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81e2b-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81e2b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e2b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e2b-137">CommonParameters</span></span>
<span data-ttu-id="81e2b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81e2b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e2b-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81e2b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e2b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="81e2b-140">INPUTS</span></span>

### <span data-ttu-id="81e2b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="81e2b-141">System.String</span></span>

### <span data-ttu-id="81e2b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="81e2b-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="81e2b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="81e2b-143">OUTPUTS</span></span>

### <span data-ttu-id="81e2b-144">System.object</span><span class="sxs-lookup"><span data-stu-id="81e2b-144">System.Boolean</span></span>

## <span data-ttu-id="81e2b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="81e2b-145">NOTES</span></span>

## <span data-ttu-id="81e2b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="81e2b-146">RELATED LINKS</span></span>
