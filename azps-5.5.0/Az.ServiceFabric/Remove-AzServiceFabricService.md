---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138338"
---
# <span data-ttu-id="c3498-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="c3498-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="c3498-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3498-102">SYNOPSIS</span></span>
<span data-ttu-id="c3498-103">從群集中移除服務。</span><span class="sxs-lookup"><span data-stu-id="c3498-103">Remove a service from the cluster.</span></span> <span data-ttu-id="c3498-104">僅支援 ARM 部署服務。</span><span class="sxs-lookup"><span data-stu-id="c3498-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="c3498-105">句法</span><span class="sxs-lookup"><span data-stu-id="c3498-105">SYNTAX</span></span>

### <span data-ttu-id="c3498-106">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="c3498-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c3498-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c3498-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3498-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3498-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3498-109">說明</span><span class="sxs-lookup"><span data-stu-id="c3498-109">DESCRIPTION</span></span>
<span data-ttu-id="c3498-110">這個 Cmdlet 會移除群集的服務形式。</span><span class="sxs-lookup"><span data-stu-id="c3498-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="c3498-111">示例</span><span class="sxs-lookup"><span data-stu-id="c3498-111">EXAMPLES</span></span>

### <span data-ttu-id="c3498-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c3498-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="c3498-113">這個範例會移除服務「testApp ~ testService1」。</span><span class="sxs-lookup"><span data-stu-id="c3498-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="c3498-114">參數</span><span class="sxs-lookup"><span data-stu-id="c3498-114">PARAMETERS</span></span>

### <span data-ttu-id="c3498-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c3498-115">-ApplicationName</span></span>
<span data-ttu-id="c3498-116">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3498-116">Specify the name of the application.</span></span>

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

### <span data-ttu-id="c3498-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c3498-117">-ClusterName</span></span>
<span data-ttu-id="c3498-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3498-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c3498-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3498-119">-DefaultProfile</span></span>
<span data-ttu-id="c3498-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3498-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3498-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c3498-121">-Force</span></span>
<span data-ttu-id="c3498-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="c3498-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="c3498-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3498-123">-InputObject</span></span>
<span data-ttu-id="c3498-124">服務資源。</span><span class="sxs-lookup"><span data-stu-id="c3498-124">The service resource.</span></span>

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

### <span data-ttu-id="c3498-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3498-125">-Name</span></span>
<span data-ttu-id="c3498-126">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3498-126">Specify the name of the service.</span></span>

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

### <span data-ttu-id="c3498-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3498-127">-PassThru</span></span>
<span data-ttu-id="c3498-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="c3498-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c3498-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3498-129">-ResourceGroupName</span></span>
<span data-ttu-id="c3498-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3498-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c3498-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3498-131">-ResourceId</span></span>
<span data-ttu-id="c3498-132">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="c3498-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="c3498-133">-確認</span><span class="sxs-lookup"><span data-stu-id="c3498-133">-Confirm</span></span>
<span data-ttu-id="c3498-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3498-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3498-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3498-135">-WhatIf</span></span>
<span data-ttu-id="c3498-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3498-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3498-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3498-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3498-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3498-138">CommonParameters</span></span>
<span data-ttu-id="c3498-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3498-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3498-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3498-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3498-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c3498-141">INPUTS</span></span>

### <span data-ttu-id="c3498-142">System.object</span><span class="sxs-lookup"><span data-stu-id="c3498-142">System.String</span></span>

### <span data-ttu-id="c3498-143">PSService 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="c3498-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="c3498-144">輸出</span><span class="sxs-lookup"><span data-stu-id="c3498-144">OUTPUTS</span></span>

### <span data-ttu-id="c3498-145">System.object</span><span class="sxs-lookup"><span data-stu-id="c3498-145">System.Boolean</span></span>

## <span data-ttu-id="c3498-146">筆記</span><span class="sxs-lookup"><span data-stu-id="c3498-146">NOTES</span></span>

## <span data-ttu-id="c3498-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3498-147">RELATED LINKS</span></span>
