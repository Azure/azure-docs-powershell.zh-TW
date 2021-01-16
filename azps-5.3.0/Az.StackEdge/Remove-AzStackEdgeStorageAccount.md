---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286120"
---
# <span data-ttu-id="43dc9-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="43dc9-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="43dc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="43dc9-103">移除裝置的邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="43dc9-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="43dc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="43dc9-104">SYNTAX</span></span>

### <span data-ttu-id="43dc9-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="43dc9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43dc9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43dc9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43dc9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43dc9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43dc9-108">說明</span><span class="sxs-lookup"><span data-stu-id="43dc9-108">DESCRIPTION</span></span>
<span data-ttu-id="43dc9-109">**AzStackEdgeStorageAccount** Cmdlet 會移除堆疊邊緣裝置的關聯邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="43dc9-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="43dc9-110">您可以指定要移除為 Cmdlet 中的參數的 Edge 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="43dc9-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="43dc9-111">示例</span><span class="sxs-lookup"><span data-stu-id="43dc9-111">EXAMPLES</span></span>

### <span data-ttu-id="43dc9-112">範例1</span><span class="sxs-lookup"><span data-stu-id="43dc9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="43dc9-113">參數</span><span class="sxs-lookup"><span data-stu-id="43dc9-113">PARAMETERS</span></span>

### <span data-ttu-id="43dc9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43dc9-114">-AsJob</span></span>
<span data-ttu-id="43dc9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="43dc9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43dc9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43dc9-116">-DefaultProfile</span></span>
<span data-ttu-id="43dc9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43dc9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43dc9-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="43dc9-118">-DeviceName</span></span>
<span data-ttu-id="43dc9-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="43dc9-119">Device Name</span></span>

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

### <span data-ttu-id="43dc9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43dc9-120">-InputObject</span></span>
<span data-ttu-id="43dc9-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="43dc9-121">Input Object</span></span>

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

### <span data-ttu-id="43dc9-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="43dc9-122">-Name</span></span>
<span data-ttu-id="43dc9-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="43dc9-123">Resource Name</span></span>

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

### <span data-ttu-id="43dc9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43dc9-124">-PassThru</span></span>
<span data-ttu-id="43dc9-125">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="43dc9-125">returns true if successful</span></span>

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

### <span data-ttu-id="43dc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43dc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="43dc9-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="43dc9-127">Resource Group Name</span></span>

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

### <span data-ttu-id="43dc9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43dc9-128">-ResourceId</span></span>
<span data-ttu-id="43dc9-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="43dc9-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="43dc9-130">-確認</span><span class="sxs-lookup"><span data-stu-id="43dc9-130">-Confirm</span></span>
<span data-ttu-id="43dc9-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43dc9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43dc9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43dc9-132">-WhatIf</span></span>
<span data-ttu-id="43dc9-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43dc9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43dc9-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43dc9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43dc9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43dc9-135">CommonParameters</span></span>
<span data-ttu-id="43dc9-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43dc9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43dc9-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43dc9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43dc9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="43dc9-138">INPUTS</span></span>

### <span data-ttu-id="43dc9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="43dc9-139">System.String</span></span>

### <span data-ttu-id="43dc9-140">PSStackEdgeStorageAccount （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="43dc9-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="43dc9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="43dc9-141">OUTPUTS</span></span>

### <span data-ttu-id="43dc9-142">System.object</span><span class="sxs-lookup"><span data-stu-id="43dc9-142">System.Boolean</span></span>

## <span data-ttu-id="43dc9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="43dc9-143">NOTES</span></span>

## <span data-ttu-id="43dc9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="43dc9-144">RELATED LINKS</span></span>
