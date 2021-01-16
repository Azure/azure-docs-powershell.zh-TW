---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricService.md
ms.openlocfilehash: 2a41a61b67ea77e2927acf5eef7b7d520464978a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281470"
---
# <span data-ttu-id="67194-101">Remove-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="67194-101">Remove-AzServiceFabricService</span></span>

## <span data-ttu-id="67194-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67194-102">SYNOPSIS</span></span>
<span data-ttu-id="67194-103">從群集中移除服務。</span><span class="sxs-lookup"><span data-stu-id="67194-103">Remove a service from the cluster.</span></span> <span data-ttu-id="67194-104">僅支援 ARM 部署服務。</span><span class="sxs-lookup"><span data-stu-id="67194-104">Only supports ARM deployed services.</span></span>

## <span data-ttu-id="67194-105">句法</span><span class="sxs-lookup"><span data-stu-id="67194-105">SYNTAX</span></span>

### <span data-ttu-id="67194-106">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="67194-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricService [-ResourceGroupName] <String> [-ClusterName] <String> [-ApplicationName] <String>
 [-Name] <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67194-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67194-107">ByResourceId</span></span>
```
Remove-AzServiceFabricService -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67194-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67194-108">ByInputObject</span></span>
```
Remove-AzServiceFabricService -InputObject <PSService> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67194-109">說明</span><span class="sxs-lookup"><span data-stu-id="67194-109">DESCRIPTION</span></span>
<span data-ttu-id="67194-110">這個 Cmdlet 會移除群集的服務形式。</span><span class="sxs-lookup"><span data-stu-id="67194-110">This cmdlet removes a service form the cluster.</span></span>

## <span data-ttu-id="67194-111">示例</span><span class="sxs-lookup"><span data-stu-id="67194-111">EXAMPLES</span></span>

### <span data-ttu-id="67194-112">範例1</span><span class="sxs-lookup"><span data-stu-id="67194-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> $serviceName = "testApp~testService1"
PS C:\> Remove-AzServiceFabricService -ResourceGroupName $resourceGroupName -ClusterName $clusterName -ApplicationName $appName -Name $serviceName
```

<span data-ttu-id="67194-113">這個範例會移除服務「testApp ~ testService1」。</span><span class="sxs-lookup"><span data-stu-id="67194-113">This example will remove the service "testApp~testService1".</span></span>

## <span data-ttu-id="67194-114">參數</span><span class="sxs-lookup"><span data-stu-id="67194-114">PARAMETERS</span></span>

### <span data-ttu-id="67194-115">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="67194-115">-ApplicationName</span></span>
<span data-ttu-id="67194-116">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="67194-116">Specify the name of the application.</span></span>

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

### <span data-ttu-id="67194-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="67194-117">-ClusterName</span></span>
<span data-ttu-id="67194-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="67194-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="67194-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67194-119">-DefaultProfile</span></span>
<span data-ttu-id="67194-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67194-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67194-121">-Force</span><span class="sxs-lookup"><span data-stu-id="67194-121">-Force</span></span>
<span data-ttu-id="67194-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="67194-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="67194-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67194-123">-InputObject</span></span>
<span data-ttu-id="67194-124">服務資源。</span><span class="sxs-lookup"><span data-stu-id="67194-124">The service resource.</span></span>

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

### <span data-ttu-id="67194-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="67194-125">-Name</span></span>
<span data-ttu-id="67194-126">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="67194-126">Specify the name of the service.</span></span>

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

### <span data-ttu-id="67194-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67194-127">-PassThru</span></span>
<span data-ttu-id="67194-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="67194-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="67194-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67194-129">-ResourceGroupName</span></span>
<span data-ttu-id="67194-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="67194-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="67194-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67194-131">-ResourceId</span></span>
<span data-ttu-id="67194-132">服務的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="67194-132">Arm ResourceId of the service.</span></span>

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

### <span data-ttu-id="67194-133">-確認</span><span class="sxs-lookup"><span data-stu-id="67194-133">-Confirm</span></span>
<span data-ttu-id="67194-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67194-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67194-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67194-135">-WhatIf</span></span>
<span data-ttu-id="67194-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67194-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67194-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67194-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67194-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67194-138">CommonParameters</span></span>
<span data-ttu-id="67194-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67194-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67194-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="67194-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67194-141">輸入</span><span class="sxs-lookup"><span data-stu-id="67194-141">INPUTS</span></span>

### <span data-ttu-id="67194-142">System.object</span><span class="sxs-lookup"><span data-stu-id="67194-142">System.String</span></span>

### <span data-ttu-id="67194-143">PSService 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="67194-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSService</span></span>

## <span data-ttu-id="67194-144">輸出</span><span class="sxs-lookup"><span data-stu-id="67194-144">OUTPUTS</span></span>

### <span data-ttu-id="67194-145">System.object</span><span class="sxs-lookup"><span data-stu-id="67194-145">System.Boolean</span></span>

## <span data-ttu-id="67194-146">筆記</span><span class="sxs-lookup"><span data-stu-id="67194-146">NOTES</span></span>

## <span data-ttu-id="67194-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="67194-147">RELATED LINKS</span></span>
