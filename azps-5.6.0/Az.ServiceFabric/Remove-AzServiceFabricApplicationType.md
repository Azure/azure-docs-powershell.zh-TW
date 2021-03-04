---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: dbd2e29a3136576ecf5596c4a401d689fd0631a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915849"
---
# <span data-ttu-id="3b636-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="3b636-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="3b636-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3b636-102">SYNOPSIS</span></span>
<span data-ttu-id="3b636-103">從組群移除服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="3b636-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="3b636-104">這會移除此資源下的所有類型版本。</span><span class="sxs-lookup"><span data-stu-id="3b636-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="3b636-105">僅支援 ARM 部署的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="3b636-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="3b636-106">語法</span><span class="sxs-lookup"><span data-stu-id="3b636-106">SYNTAX</span></span>

### <span data-ttu-id="3b636-107">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="3b636-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b636-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b636-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b636-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3b636-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b636-110">描述</span><span class="sxs-lookup"><span data-stu-id="3b636-110">DESCRIPTION</span></span>
<span data-ttu-id="3b636-111">此 Cmdlet 會移除該組集中的應用程式類型，並移除此資源下的所有類型版本，但應先移除其下的所有應用程式，再執行此命令。</span><span class="sxs-lookup"><span data-stu-id="3b636-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="3b636-112">例子</span><span class="sxs-lookup"><span data-stu-id="3b636-112">EXAMPLES</span></span>

### <span data-ttu-id="3b636-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="3b636-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="3b636-114">此範例會移除應用程式類型 "testAppType" 及其下的所有版本。</span><span class="sxs-lookup"><span data-stu-id="3b636-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="3b636-115">如果有使用此類型建立的任何應用程式，該命令會引發例外。</span><span class="sxs-lookup"><span data-stu-id="3b636-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="3b636-116">參數</span><span class="sxs-lookup"><span data-stu-id="3b636-116">PARAMETERS</span></span>

### <span data-ttu-id="3b636-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3b636-117">-ClusterName</span></span>
<span data-ttu-id="3b636-118">指定組名。</span><span class="sxs-lookup"><span data-stu-id="3b636-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b636-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b636-119">-DefaultProfile</span></span>
<span data-ttu-id="3b636-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b636-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b636-121">-強制</span><span class="sxs-lookup"><span data-stu-id="3b636-121">-Force</span></span>
<span data-ttu-id="3b636-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="3b636-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="3b636-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b636-123">-InputObject</span></span>
<span data-ttu-id="3b636-124">應用程式類型資源。</span><span class="sxs-lookup"><span data-stu-id="3b636-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b636-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b636-125">-Name</span></span>
<span data-ttu-id="3b636-126">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b636-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b636-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b636-127">-PassThru</span></span>
<span data-ttu-id="3b636-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3b636-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3b636-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b636-129">-ResourceGroupName</span></span>
<span data-ttu-id="3b636-130">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b636-130">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b636-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b636-131">-ResourceId</span></span>
<span data-ttu-id="3b636-132">應用程式類型的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="3b636-132">Arm ResourceId of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b636-133">-確認</span><span class="sxs-lookup"><span data-stu-id="3b636-133">-Confirm</span></span>
<span data-ttu-id="3b636-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3b636-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b636-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b636-135">-WhatIf</span></span>
<span data-ttu-id="3b636-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b636-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b636-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b636-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b636-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b636-138">CommonParameters</span></span>
<span data-ttu-id="3b636-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3b636-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b636-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b636-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b636-141">輸入</span><span class="sxs-lookup"><span data-stu-id="3b636-141">INPUTS</span></span>

### <span data-ttu-id="3b636-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3b636-142">System.String</span></span>

### <span data-ttu-id="3b636-143">Microsoft.Azure.Commands.ServiceFabric.models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="3b636-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="3b636-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3b636-144">OUTPUTS</span></span>

### <span data-ttu-id="3b636-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b636-145">System.Boolean</span></span>

## <span data-ttu-id="3b636-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3b636-146">NOTES</span></span>

## <span data-ttu-id="3b636-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b636-147">RELATED LINKS</span></span>
