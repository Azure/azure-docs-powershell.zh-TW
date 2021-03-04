---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 0a573f8fa293d2c3e4c84eced54c88eb77032970
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915734"
---
# <span data-ttu-id="cfedc-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfedc-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="cfedc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cfedc-102">SYNOPSIS</span></span>
<span data-ttu-id="cfedc-103">移除裝置的邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cfedc-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="cfedc-104">語法</span><span class="sxs-lookup"><span data-stu-id="cfedc-104">SYNTAX</span></span>

### <span data-ttu-id="cfedc-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cfedc-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfedc-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfedc-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfedc-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cfedc-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfedc-108">描述</span><span class="sxs-lookup"><span data-stu-id="cfedc-108">DESCRIPTION</span></span>
<span data-ttu-id="cfedc-109">**Remove-AzStackEdgeStorageAccount** Cmdlet 會移除堆疊 Edge 裝置的相關 Edge 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cfedc-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="cfedc-110">您可以指定要移除的 Edge 儲存空間帳戶名稱，做為 Cmdlet 中的參數。</span><span class="sxs-lookup"><span data-stu-id="cfedc-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="cfedc-111">例子</span><span class="sxs-lookup"><span data-stu-id="cfedc-111">EXAMPLES</span></span>

### <span data-ttu-id="cfedc-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="cfedc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="cfedc-113">參數</span><span class="sxs-lookup"><span data-stu-id="cfedc-113">PARAMETERS</span></span>

### <span data-ttu-id="cfedc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfedc-114">-AsJob</span></span>
<span data-ttu-id="cfedc-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cfedc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfedc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfedc-116">-DefaultProfile</span></span>
<span data-ttu-id="cfedc-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cfedc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfedc-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="cfedc-118">-DeviceName</span></span>
<span data-ttu-id="cfedc-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="cfedc-119">Device Name</span></span>

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

### <span data-ttu-id="cfedc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfedc-120">-InputObject</span></span>
<span data-ttu-id="cfedc-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="cfedc-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfedc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cfedc-122">-Name</span></span>
<span data-ttu-id="cfedc-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="cfedc-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfedc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cfedc-124">-PassThru</span></span>
<span data-ttu-id="cfedc-125">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="cfedc-125">returns true if successful</span></span>

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

### <span data-ttu-id="cfedc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfedc-126">-ResourceGroupName</span></span>
<span data-ttu-id="cfedc-127">資源組名</span><span class="sxs-lookup"><span data-stu-id="cfedc-127">Resource Group Name</span></span>

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

### <span data-ttu-id="cfedc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfedc-128">-ResourceId</span></span>
<span data-ttu-id="cfedc-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfedc-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfedc-130">-確認</span><span class="sxs-lookup"><span data-stu-id="cfedc-130">-Confirm</span></span>
<span data-ttu-id="cfedc-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cfedc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfedc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfedc-132">-WhatIf</span></span>
<span data-ttu-id="cfedc-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cfedc-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfedc-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cfedc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfedc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfedc-135">CommonParameters</span></span>
<span data-ttu-id="cfedc-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cfedc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfedc-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cfedc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfedc-138">輸入</span><span class="sxs-lookup"><span data-stu-id="cfedc-138">INPUTS</span></span>

### <span data-ttu-id="cfedc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="cfedc-139">System.String</span></span>

### <span data-ttu-id="cfedc-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfedc-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="cfedc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="cfedc-141">OUTPUTS</span></span>

### <span data-ttu-id="cfedc-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cfedc-142">System.Boolean</span></span>

## <span data-ttu-id="cfedc-143">筆記</span><span class="sxs-lookup"><span data-stu-id="cfedc-143">NOTES</span></span>

## <span data-ttu-id="cfedc-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="cfedc-144">RELATED LINKS</span></span>
