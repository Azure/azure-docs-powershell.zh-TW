---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagednodetypevmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedNodeTypeVMExtension.md
ms.openlocfilehash: dfe88add0571fe460520e7af3b8dece4c4d0bc6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126793"
---
# <span data-ttu-id="5c960-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="5c960-101">Remove-AzServiceFabricManagedNodeTypeVMExtension</span></span>

## <span data-ttu-id="5c960-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c960-102">SYNOPSIS</span></span>
<span data-ttu-id="5c960-103">從節點類型移除 vm 延伸。</span><span class="sxs-lookup"><span data-stu-id="5c960-103">Remove vm extension from the node type.</span></span>

## <span data-ttu-id="5c960-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c960-104">SYNTAX</span></span>

### <span data-ttu-id="5c960-105">ByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="5c960-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-InputObject] <PSManagedNodeType> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c960-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5c960-106">ByName</span></span>
```
Remove-AzServiceFabricManagedNodeTypeVMExtension [-ResourceGroupName] <String> [-ClusterName] <String>
 [-NodeTypeName] <String> -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c960-107">說明</span><span class="sxs-lookup"><span data-stu-id="5c960-107">DESCRIPTION</span></span>
<span data-ttu-id="5c960-108">依名稱從節點類型移除 vm 延伸。</span><span class="sxs-lookup"><span data-stu-id="5c960-108">Remove vm extension from the node type by name.</span></span> <span data-ttu-id="5c960-109">使用 [AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) ，並查看 VmExtensions 屬性，以查看節點類型上的目前延伸。</span><span class="sxs-lookup"><span data-stu-id="5c960-109">Use [Get-AzServiceFabricManagedNodeType](./Get-AzServiceFabricManagedNodeType.md) and look at the VmExtensions property to see the current extension on the node type.</span></span>

## <span data-ttu-id="5c960-110">示例</span><span class="sxs-lookup"><span data-stu-id="5c960-110">EXAMPLES</span></span>

### <span data-ttu-id="5c960-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5c960-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Remove-AzServiceFabricManagedNodeTypeVMExtension -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -Name MyExtensionName
```

<span data-ttu-id="5c960-112">依名稱從節點類型移除延伸。</span><span class="sxs-lookup"><span data-stu-id="5c960-112">Remove extension from node type by name.</span></span>

### <span data-ttu-id="5c960-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5c960-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Remove-AzServiceFabricManagedNodeTypeVMExtension -Name MyExtensionName
```

<span data-ttu-id="5c960-114">使用管道從節點類型移除延伸（依名稱）。</span><span class="sxs-lookup"><span data-stu-id="5c960-114">Remove extension from node type by name, with piping.</span></span>

## <span data-ttu-id="5c960-115">參數</span><span class="sxs-lookup"><span data-stu-id="5c960-115">PARAMETERS</span></span>

### <span data-ttu-id="5c960-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c960-116">-AsJob</span></span>
<span data-ttu-id="5c960-117">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="5c960-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5c960-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5c960-118">-ClusterName</span></span>
<span data-ttu-id="5c960-119">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c960-119">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5c960-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c960-120">-DefaultProfile</span></span>
<span data-ttu-id="5c960-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c960-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c960-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c960-122">-InputObject</span></span>
<span data-ttu-id="5c960-123">節點類型資源</span><span class="sxs-lookup"><span data-stu-id="5c960-123">Node type resource</span></span>

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

### <span data-ttu-id="5c960-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c960-124">-Name</span></span>
<span data-ttu-id="5c960-125">副檔名。</span><span class="sxs-lookup"><span data-stu-id="5c960-125">extension name.</span></span>

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

### <span data-ttu-id="5c960-126">-NodeTypeName</span><span class="sxs-lookup"><span data-stu-id="5c960-126">-NodeTypeName</span></span>
<span data-ttu-id="5c960-127">指定節點類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c960-127">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="5c960-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c960-128">-PassThru</span></span>
<span data-ttu-id="5c960-129">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="5c960-129">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5c960-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c960-130">-ResourceGroupName</span></span>
<span data-ttu-id="5c960-131">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c960-131">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5c960-132">-確認</span><span class="sxs-lookup"><span data-stu-id="5c960-132">-Confirm</span></span>
<span data-ttu-id="5c960-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c960-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c960-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c960-134">-WhatIf</span></span>
<span data-ttu-id="5c960-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c960-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c960-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c960-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c960-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c960-137">CommonParameters</span></span>
<span data-ttu-id="5c960-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c960-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c960-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5c960-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c960-140">輸入</span><span class="sxs-lookup"><span data-stu-id="5c960-140">INPUTS</span></span>

### <span data-ttu-id="5c960-141">System.object</span><span class="sxs-lookup"><span data-stu-id="5c960-141">System.String</span></span>

## <span data-ttu-id="5c960-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5c960-142">OUTPUTS</span></span>

### <span data-ttu-id="5c960-143">PSManagedNodeType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="5c960-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="5c960-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5c960-144">NOTES</span></span>

## <span data-ttu-id="5c960-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c960-145">RELATED LINKS</span></span>
