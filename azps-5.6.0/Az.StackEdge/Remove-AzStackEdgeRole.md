---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeRole.md
ms.openlocfilehash: d34893ef00fd0e7fb799c2bc0569e818f78a4185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915742"
---
# <span data-ttu-id="aa495-101">Remove-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="aa495-101">Remove-AzStackEdgeRole</span></span>

## <span data-ttu-id="aa495-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aa495-102">SYNOPSIS</span></span>
<span data-ttu-id="aa495-103">移除裝置的相關 IoT 角色。</span><span class="sxs-lookup"><span data-stu-id="aa495-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="aa495-104">語法</span><span class="sxs-lookup"><span data-stu-id="aa495-104">SYNTAX</span></span>

### <span data-ttu-id="aa495-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="aa495-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa495-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa495-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa495-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa495-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeRole -InputObject <PSStackEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa495-108">描述</span><span class="sxs-lookup"><span data-stu-id="aa495-108">DESCRIPTION</span></span>
<span data-ttu-id="aa495-109">**Remove-AzStackEdgeRole** Cmdlet 會移除堆疊 Edge 裝置的相關 IoT 角色。</span><span class="sxs-lookup"><span data-stu-id="aa495-109">The **Remove-AzStackEdgeRole** cmdlet removes the associated IoT role for a Stack Edge device.</span></span>

## <span data-ttu-id="aa495-110">例子</span><span class="sxs-lookup"><span data-stu-id="aa495-110">EXAMPLES</span></span>

### <span data-ttu-id="aa495-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="aa495-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="aa495-112">參數</span><span class="sxs-lookup"><span data-stu-id="aa495-112">PARAMETERS</span></span>

### <span data-ttu-id="aa495-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa495-113">-AsJob</span></span>
<span data-ttu-id="aa495-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="aa495-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa495-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa495-115">-DefaultProfile</span></span>
<span data-ttu-id="aa495-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa495-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa495-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="aa495-117">-DeviceName</span></span>
<span data-ttu-id="aa495-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="aa495-118">Device Name</span></span>

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

### <span data-ttu-id="aa495-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa495-119">-InputObject</span></span>
<span data-ttu-id="aa495-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="aa495-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa495-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa495-121">-Name</span></span>
<span data-ttu-id="aa495-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="aa495-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa495-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa495-123">-PassThru</span></span>
<span data-ttu-id="aa495-124">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="aa495-124">returns true if successful</span></span>

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

### <span data-ttu-id="aa495-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa495-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa495-126">資源組名</span><span class="sxs-lookup"><span data-stu-id="aa495-126">Resource Group Name</span></span>

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

### <span data-ttu-id="aa495-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa495-127">-ResourceId</span></span>
<span data-ttu-id="aa495-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa495-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="aa495-129">-確認</span><span class="sxs-lookup"><span data-stu-id="aa495-129">-Confirm</span></span>
<span data-ttu-id="aa495-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aa495-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa495-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa495-131">-WhatIf</span></span>
<span data-ttu-id="aa495-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa495-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa495-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa495-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa495-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa495-134">CommonParameters</span></span>
<span data-ttu-id="aa495-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aa495-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa495-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa495-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa495-137">輸入</span><span class="sxs-lookup"><span data-stu-id="aa495-137">INPUTS</span></span>

### <span data-ttu-id="aa495-138">System.String</span><span class="sxs-lookup"><span data-stu-id="aa495-138">System.String</span></span>

### <span data-ttu-id="aa495-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="aa495-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="aa495-140">輸出</span><span class="sxs-lookup"><span data-stu-id="aa495-140">OUTPUTS</span></span>

### <span data-ttu-id="aa495-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="aa495-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="aa495-142">筆記</span><span class="sxs-lookup"><span data-stu-id="aa495-142">NOTES</span></span>

## <span data-ttu-id="aa495-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa495-143">RELATED LINKS</span></span>
