---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 5004b6b9528eb91a1883805405dba6147d5161a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915850"
---
# <span data-ttu-id="8fc53-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="8fc53-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="8fc53-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8fc53-102">SYNOPSIS</span></span>
<span data-ttu-id="8fc53-103">從組群移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="8fc53-103">Remove an application from the cluster.</span></span> <span data-ttu-id="8fc53-104">這會移除應用程式下的所有服務。</span><span class="sxs-lookup"><span data-stu-id="8fc53-104">This will remove all the services under the application.</span></span> <span data-ttu-id="8fc53-105">僅支援 ARM 部署的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8fc53-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="8fc53-106">語法</span><span class="sxs-lookup"><span data-stu-id="8fc53-106">SYNTAX</span></span>

### <span data-ttu-id="8fc53-107">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="8fc53-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc53-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc53-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fc53-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8fc53-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fc53-110">描述</span><span class="sxs-lookup"><span data-stu-id="8fc53-110">DESCRIPTION</span></span>
<span data-ttu-id="8fc53-111">此 Cmdlet 會移除該組集中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8fc53-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="8fc53-112">這會移除應用程式資源下的所有服務 ，如果有的話。</span><span class="sxs-lookup"><span data-stu-id="8fc53-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="8fc53-113">例子</span><span class="sxs-lookup"><span data-stu-id="8fc53-113">EXAMPLES</span></span>

### <span data-ttu-id="8fc53-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="8fc53-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="8fc53-115">此範例會移除資源群組 "testRG" 和叢集 "testCluster" 下的應用程式 "testApp"。</span><span class="sxs-lookup"><span data-stu-id="8fc53-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="8fc53-116">參數</span><span class="sxs-lookup"><span data-stu-id="8fc53-116">PARAMETERS</span></span>

### <span data-ttu-id="8fc53-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8fc53-117">-ClusterName</span></span>
<span data-ttu-id="8fc53-118">指定組名。</span><span class="sxs-lookup"><span data-stu-id="8fc53-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="8fc53-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fc53-119">-DefaultProfile</span></span>
<span data-ttu-id="8fc53-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8fc53-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fc53-121">-強制</span><span class="sxs-lookup"><span data-stu-id="8fc53-121">-Force</span></span>
<span data-ttu-id="8fc53-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="8fc53-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="8fc53-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fc53-123">-InputObject</span></span>
<span data-ttu-id="8fc53-124">應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="8fc53-124">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fc53-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8fc53-125">-Name</span></span>
<span data-ttu-id="8fc53-126">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fc53-126">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fc53-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fc53-127">-PassThru</span></span>
<span data-ttu-id="8fc53-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8fc53-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8fc53-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fc53-129">-ResourceGroupName</span></span>
<span data-ttu-id="8fc53-130">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8fc53-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="8fc53-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fc53-131">-ResourceId</span></span>
<span data-ttu-id="8fc53-132">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="8fc53-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="8fc53-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8fc53-133">-Confirm</span></span>
<span data-ttu-id="8fc53-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8fc53-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fc53-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fc53-135">-WhatIf</span></span>
<span data-ttu-id="8fc53-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8fc53-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fc53-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8fc53-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fc53-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fc53-138">CommonParameters</span></span>
<span data-ttu-id="8fc53-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8fc53-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fc53-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8fc53-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fc53-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8fc53-141">INPUTS</span></span>

### <span data-ttu-id="8fc53-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8fc53-142">System.String</span></span>

### <span data-ttu-id="8fc53-143">Microsoft.Azure.Commands.ServiceFabric.models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="8fc53-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="8fc53-144">輸出</span><span class="sxs-lookup"><span data-stu-id="8fc53-144">OUTPUTS</span></span>

### <span data-ttu-id="8fc53-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8fc53-145">System.Boolean</span></span>

## <span data-ttu-id="8fc53-146">筆記</span><span class="sxs-lookup"><span data-stu-id="8fc53-146">NOTES</span></span>

## <span data-ttu-id="8fc53-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fc53-147">RELATED LINKS</span></span>
