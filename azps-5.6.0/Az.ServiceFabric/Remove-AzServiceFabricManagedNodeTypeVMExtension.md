---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: 410509f59cc34dd139761a3e4ddb5de9907ef720
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915818"
---
# <span data-ttu-id="22928-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="22928-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="22928-102">簡介</span><span class="sxs-lookup"><span data-stu-id="22928-102">SYNOPSIS</span></span>
<span data-ttu-id="22928-103">從節點類型移除 vm 副檔名。</span><span class="sxs-lookup"><span data-stu-id="22928-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="22928-104">語法</span><span class="sxs-lookup"><span data-stu-id="22928-104">SYNTAX</span></span>

### <span data-ttu-id="22928-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="22928-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22928-106">ByName</span><span class="sxs-lookup"><span data-stu-id="22928-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22928-107">描述</span><span class="sxs-lookup"><span data-stu-id="22928-107">DESCRIPTION</span></span>
<span data-ttu-id="22928-108">根據名稱從節點類型移除 vm 副檔名。</span><span class="sxs-lookup"><span data-stu-id="22928-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="22928-109">使用 [Get-AzServiceFabricManagedNodeType，](./Get-AzServiceFabricManagedNodeType.md) 並查看 VmExtensions 屬性，以查看節點類型的目前擴充功能。</span><span class="sxs-lookup"><span data-stu-id="22928-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="22928-110">例子</span><span class="sxs-lookup"><span data-stu-id="22928-110">EXAMPLES</span></span>

### <span data-ttu-id="22928-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="22928-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="22928-112">根據名稱從節點類型移除副檔名。</span><span class="sxs-lookup"><span data-stu-id="22928-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="22928-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="22928-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="22928-114">使用管線從節點類型移除延伸模組。</span><span class="sxs-lookup"><span data-stu-id="22928-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="22928-115">參數</span><span class="sxs-lookup"><span data-stu-id="22928-115">PARAMETERS</span></span>

### <span data-ttu-id="22928-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22928-116">-AsJob</span></span>
<span data-ttu-id="22928-117">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="22928-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="22928-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="22928-118">-ClusterName</span></span>
<span data-ttu-id="22928-119">指定組名。</span><span class="sxs-lookup"><span data-stu-id="22928-119">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22928-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22928-120">-DefaultProfile</span></span>
<span data-ttu-id="22928-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="22928-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22928-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22928-122">-InputObject</span></span>
<span data-ttu-id="22928-123">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="22928-123">Node type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22928-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="22928-124">-Name</span></span>
<span data-ttu-id="22928-125">副檔名。</span><span class="sxs-lookup"><span data-stu-id="22928-125">extension name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22928-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="22928-126">-NodeTypeName</span></span>
<span data-ttu-id="22928-127">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="22928-127">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22928-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22928-128">-PassThru</span></span>
<span data-ttu-id="22928-129">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="22928-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="22928-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22928-130">-ResourceGroupName</span></span>
<span data-ttu-id="22928-131">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22928-131">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22928-132">-確認</span><span class="sxs-lookup"><span data-stu-id="22928-132">-Confirm</span></span>
<span data-ttu-id="22928-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="22928-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22928-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22928-134">-WhatIf</span></span>
<span data-ttu-id="22928-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22928-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22928-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22928-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22928-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22928-137">CommonParameters</span></span>
<span data-ttu-id="22928-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="22928-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22928-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22928-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22928-140">輸入</span><span class="sxs-lookup"><span data-stu-id="22928-140">INPUTS</span></span>

### <span data-ttu-id="22928-141">System.String</span><span class="sxs-lookup"><span data-stu-id="22928-141">System.String</span></span>

## <span data-ttu-id="22928-142">輸出</span><span class="sxs-lookup"><span data-stu-id="22928-142">OUTPUTS</span></span>

### <span data-ttu-id="22928-143">Microsoft.Azure.Commands.ServiceFabric.models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="22928-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="22928-144">筆記</span><span class="sxs-lookup"><span data-stu-id="22928-144">NOTES</span></span>

## <span data-ttu-id="22928-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="22928-145">RELATED LINKS</span></span>
