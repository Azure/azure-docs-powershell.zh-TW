---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 1475296638cec105713eaa390bcce6552e5502ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970170"
---
# <span data-ttu-id="6e2b6-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="6e2b6-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="6e2b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e2b6-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2b6-103">從群集中移除服務。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-103">Remove a service from the cluster.</span></span>

## <span data-ttu-id="6e2b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e2b6-104">SYNTAX</span></span>

### <span data-ttu-id="6e2b6-105">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="6e2b6-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e2b6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e2b6-106">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2b6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e2b6-107">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e2b6-108">說明</span><span class="sxs-lookup"><span data-stu-id="6e2b6-108">DESCRIPTION</span></span>
<span data-ttu-id="6e2b6-109">這個 Cmdlet 會移除群集的服務形式。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-109">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="6e2b6-110">示例</span><span class="sxs-lookup"><span data-stu-id="6e2b6-110">EXAMPLES</span></span>

### <span data-ttu-id="6e2b6-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6e2b6-111">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="6e2b6-112">這個範例會移除服務「testApp ~ testService1」。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-112">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="6e2b6-113">參數</span><span class="sxs-lookup"><span data-stu-id="6e2b6-113">PARAMETERS</span></span>

### <span data-ttu-id="6e2b6-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="6e2b6-114">-ApplicationName</span></span>
<span data-ttu-id="6e2b6-115">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-115">Specify the name of the application.</span></span>

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

### <span data-ttu-id="6e2b6-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6e2b6-116">-ClusterName</span></span>
<span data-ttu-id="6e2b6-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6e2b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2b6-118">-DefaultProfile</span></span>
<span data-ttu-id="6e2b6-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e2b6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6e2b6-120">-Force</span></span>
<span data-ttu-id="6e2b6-121">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="6e2b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e2b6-122">-InputObject</span></span>
<span data-ttu-id="6e2b6-123">服務資源。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-123">The service resource.</span></span>

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

### <span data-ttu-id="6e2b6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e2b6-124">-Name</span></span>
<span data-ttu-id="6e2b6-125">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-125">Specify the name of the service.</span></span>

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

### <span data-ttu-id="6e2b6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e2b6-126">-PassThru</span></span>
<span data-ttu-id="6e2b6-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="6e2b6-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6e2b6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2b6-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e2b6-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="6e2b6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e2b6-130">-ResourceId</span></span>
<span data-ttu-id="6e2b6-131">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-131">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="6e2b6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6e2b6-132">-Confirm</span></span>
<span data-ttu-id="6e2b6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e2b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e2b6-134">-WhatIf</span></span>
<span data-ttu-id="6e2b6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e2b6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e2b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2b6-137">CommonParameters</span></span>
<span data-ttu-id="6e2b6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2b6-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2b6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6e2b6-140">INPUTS</span></span>

### <span data-ttu-id="6e2b6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="6e2b6-141">System.String</span></span>

### <span data-ttu-id="6e2b6-142">PSService 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="6e2b6-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="6e2b6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6e2b6-143">OUTPUTS</span></span>

### <span data-ttu-id="6e2b6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="6e2b6-144">System.Boolean</span></span>

## <span data-ttu-id="6e2b6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6e2b6-145">NOTES</span></span>

## <span data-ttu-id="6e2b6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e2b6-146">RELATED LINKS</span></span>