---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 992cd2a381e9eda89b9388ec1ed37f74a76e9adf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915809"
---
# <span data-ttu-id="27ef3-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="27ef3-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="27ef3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="27ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="27ef3-103">從組群移除服務。</span><span class="sxs-lookup"><span data-stu-id="27ef3-103">Remove a service from the cluster.</span></span> <span data-ttu-id="27ef3-104">僅支援 ARM 部署的服務。</span><span class="sxs-lookup"><span data-stu-id="27ef3-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="27ef3-105">語法</span><span class="sxs-lookup"><span data-stu-id="27ef3-105">SYNTAX</span></span>

### <span data-ttu-id="27ef3-106">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="27ef3-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27ef3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="27ef3-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27ef3-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="27ef3-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27ef3-109">描述</span><span class="sxs-lookup"><span data-stu-id="27ef3-109">DESCRIPTION</span></span>
<span data-ttu-id="27ef3-110">此 Cmdlet 會移除該群中的服務。</span><span class="sxs-lookup"><span data-stu-id="27ef3-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="27ef3-111">例子</span><span class="sxs-lookup"><span data-stu-id="27ef3-111">EXAMPLES</span></span>

### <span data-ttu-id="27ef3-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="27ef3-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="27ef3-113">此範例會移除服務"testApp~testService1"。</span><span class="sxs-lookup"><span data-stu-id="27ef3-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="27ef3-114">參數</span><span class="sxs-lookup"><span data-stu-id="27ef3-114">PARAMETERS</span></span>

### <span data-ttu-id="27ef3-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="27ef3-115">-ApplicationName</span></span>
<span data-ttu-id="27ef3-116">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="27ef3-116">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef3-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="27ef3-117">-ClusterName</span></span>
<span data-ttu-id="27ef3-118">指定組名。</span><span class="sxs-lookup"><span data-stu-id="27ef3-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="27ef3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ef3-119">-DefaultProfile</span></span>
<span data-ttu-id="27ef3-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="27ef3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27ef3-121">-強制</span><span class="sxs-lookup"><span data-stu-id="27ef3-121">-Force</span></span>
<span data-ttu-id="27ef3-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="27ef3-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="27ef3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27ef3-123">-InputObject</span></span>
<span data-ttu-id="27ef3-124">服務資源。</span><span class="sxs-lookup"><span data-stu-id="27ef3-124">The service resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27ef3-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="27ef3-125">-Name</span></span>
<span data-ttu-id="27ef3-126">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="27ef3-126">Specify the name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ServiceName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ef3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27ef3-127">-PassThru</span></span>
<span data-ttu-id="27ef3-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="27ef3-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="27ef3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ef3-129">-ResourceGroupName</span></span>
<span data-ttu-id="27ef3-130">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27ef3-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="27ef3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27ef3-131">-ResourceId</span></span>
<span data-ttu-id="27ef3-132">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="27ef3-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="27ef3-133">-確認</span><span class="sxs-lookup"><span data-stu-id="27ef3-133">-Confirm</span></span>
<span data-ttu-id="27ef3-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="27ef3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ef3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ef3-135">-WhatIf</span></span>
<span data-ttu-id="27ef3-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="27ef3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27ef3-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="27ef3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ef3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ef3-138">CommonParameters</span></span>
<span data-ttu-id="27ef3-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="27ef3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ef3-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27ef3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ef3-141">輸入</span><span class="sxs-lookup"><span data-stu-id="27ef3-141">INPUTS</span></span>

### <span data-ttu-id="27ef3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="27ef3-142">System.String</span></span>

### <span data-ttu-id="27ef3-143">Microsoft.Azure.Commands.ServiceFabric.models.PSService</span><span class="sxs-lookup"><span data-stu-id="27ef3-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="27ef3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="27ef3-144">OUTPUTS</span></span>

### <span data-ttu-id="27ef3-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="27ef3-145">System.Boolean</span></span>

## <span data-ttu-id="27ef3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="27ef3-146">NOTES</span></span>

## <span data-ttu-id="27ef3-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="27ef3-147">RELATED LINKS</span></span>
