---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 8dc06a9ce860dfb6e01c79674dd414eedb51df17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129257"
---
# <span data-ttu-id="a939b-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="a939b-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="a939b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a939b-102">SYNOPSIS</span></span>
<span data-ttu-id="a939b-103">從群集中移除應用程式。</span><span class="sxs-lookup"><span data-stu-id="a939b-103">Remove an application from the cluster.</span></span> <span data-ttu-id="a939b-104">這將會移除應用程式下的所有服務。</span><span class="sxs-lookup"><span data-stu-id="a939b-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="a939b-105">句法</span><span class="sxs-lookup"><span data-stu-id="a939b-105">SYNTAX</span></span>

### <span data-ttu-id="a939b-106">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="a939b-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a939b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a939b-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a939b-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a939b-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a939b-109">說明</span><span class="sxs-lookup"><span data-stu-id="a939b-109">DESCRIPTION</span></span>
<span data-ttu-id="a939b-110">這個 Cmdlet 會移除群集中的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a939b-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="a939b-111">這將會移除應用程式資源底下的所有服務（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a939b-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="a939b-112">示例</span><span class="sxs-lookup"><span data-stu-id="a939b-112">EXAMPLES</span></span>

### <span data-ttu-id="a939b-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a939b-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="a939b-114">這個範例會移除 [testRG] 和 [群集] testCluster "資源群組] 下的應用程式" testApp "。</span><span class="sxs-lookup"><span data-stu-id="a939b-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="a939b-115">參數</span><span class="sxs-lookup"><span data-stu-id="a939b-115">PARAMETERS</span></span>

### <span data-ttu-id="a939b-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a939b-116">-ClusterName</span></span>
<span data-ttu-id="a939b-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a939b-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a939b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a939b-118">-DefaultProfile</span></span>
<span data-ttu-id="a939b-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a939b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a939b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a939b-120">-Force</span></span>
<span data-ttu-id="a939b-121">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="a939b-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="a939b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a939b-122">-InputObject</span></span>
<span data-ttu-id="a939b-123">應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="a939b-123">The application resource.</span></span>

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

### <span data-ttu-id="a939b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="a939b-124">-Name</span></span>
<span data-ttu-id="a939b-125">指定應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a939b-125">Specify the name of the application.</span></span>

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

### <span data-ttu-id="a939b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a939b-126">-PassThru</span></span>
<span data-ttu-id="a939b-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="a939b-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a939b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a939b-128">-ResourceGroupName</span></span>
<span data-ttu-id="a939b-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a939b-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a939b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a939b-130">-ResourceId</span></span>
<span data-ttu-id="a939b-131">應用程式的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a939b-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="a939b-132">-確認</span><span class="sxs-lookup"><span data-stu-id="a939b-132">-Confirm</span></span>
<span data-ttu-id="a939b-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a939b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a939b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a939b-134">-WhatIf</span></span>
<span data-ttu-id="a939b-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a939b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a939b-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a939b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a939b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a939b-137">CommonParameters</span></span>
<span data-ttu-id="a939b-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a939b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a939b-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a939b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a939b-140">輸入</span><span class="sxs-lookup"><span data-stu-id="a939b-140">INPUTS</span></span>

### <span data-ttu-id="a939b-141">System.object</span><span class="sxs-lookup"><span data-stu-id="a939b-141">System.String</span></span>

### <span data-ttu-id="a939b-142">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a939b-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="a939b-143">輸出</span><span class="sxs-lookup"><span data-stu-id="a939b-143">OUTPUTS</span></span>

### <span data-ttu-id="a939b-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a939b-144">System.Boolean</span></span>

## <span data-ttu-id="a939b-145">筆記</span><span class="sxs-lookup"><span data-stu-id="a939b-145">NOTES</span></span>

## <span data-ttu-id="a939b-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a939b-146">RELATED LINKS</span></span>
