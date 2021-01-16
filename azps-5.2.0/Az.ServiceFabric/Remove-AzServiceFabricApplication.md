---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279959"
---
# <span data-ttu-id="ec7d8-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ec7d8-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="ec7d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7d8-103">從群集中移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-103">Remove an application from the cluster.</span></span> <span data-ttu-id="ec7d8-104">這將會移除應用程式下的所有服務。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-104">This will remove all the services under the application.</span></span> <span data-ttu-id="ec7d8-105">僅支援 ARM 部署的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="ec7d8-106">句法</span><span class="sxs-lookup"><span data-stu-id="ec7d8-106">SYNTAX</span></span>

### <span data-ttu-id="ec7d8-107">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="ec7d8-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7d8-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7d8-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec7d8-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ec7d8-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec7d8-110">說明</span><span class="sxs-lookup"><span data-stu-id="ec7d8-110">DESCRIPTION</span></span>
<span data-ttu-id="ec7d8-111">這個 Cmdlet 會移除群集中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="ec7d8-112">這將會移除應用程式資源底下的所有服務（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="ec7d8-113">示例</span><span class="sxs-lookup"><span data-stu-id="ec7d8-113">EXAMPLES</span></span>

### <span data-ttu-id="ec7d8-114">範例1</span><span class="sxs-lookup"><span data-stu-id="ec7d8-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="ec7d8-115">這個範例會移除 [testRG] 和 [群集] testCluster "資源群組] 下的應用程式" testApp "。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="ec7d8-116">參數</span><span class="sxs-lookup"><span data-stu-id="ec7d8-116">PARAMETERS</span></span>

### <span data-ttu-id="ec7d8-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ec7d8-117">-ClusterName</span></span>
<span data-ttu-id="ec7d8-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ec7d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7d8-119">-DefaultProfile</span></span>
<span data-ttu-id="ec7d8-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec7d8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ec7d8-121">-Force</span></span>
<span data-ttu-id="ec7d8-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="ec7d8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec7d8-123">-InputObject</span></span>
<span data-ttu-id="ec7d8-124">應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-124">The application resource.</span></span>

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

### <span data-ttu-id="ec7d8-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec7d8-125">-Name</span></span>
<span data-ttu-id="ec7d8-126">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="ec7d8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec7d8-127">-PassThru</span></span>
<span data-ttu-id="ec7d8-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="ec7d8-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ec7d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec7d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec7d8-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ec7d8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec7d8-131">-ResourceId</span></span>
<span data-ttu-id="ec7d8-132">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="ec7d8-133">-確認</span><span class="sxs-lookup"><span data-stu-id="ec7d8-133">-Confirm</span></span>
<span data-ttu-id="ec7d8-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec7d8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec7d8-135">-WhatIf</span></span>
<span data-ttu-id="ec7d8-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec7d8-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec7d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7d8-138">CommonParameters</span></span>
<span data-ttu-id="ec7d8-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7d8-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7d8-141">輸入</span><span class="sxs-lookup"><span data-stu-id="ec7d8-141">INPUTS</span></span>

### <span data-ttu-id="ec7d8-142">System.object</span><span class="sxs-lookup"><span data-stu-id="ec7d8-142">System.String</span></span>

### <span data-ttu-id="ec7d8-143">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="ec7d8-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="ec7d8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ec7d8-144">OUTPUTS</span></span>

### <span data-ttu-id="ec7d8-145">System.object</span><span class="sxs-lookup"><span data-stu-id="ec7d8-145">System.Boolean</span></span>

## <span data-ttu-id="ec7d8-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ec7d8-146">NOTES</span></span>

## <span data-ttu-id="ec7d8-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec7d8-147">RELATED LINKS</span></span>
