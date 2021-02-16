---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130751"
---
# <span data-ttu-id="684b4-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="684b4-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="684b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="684b4-102">SYNOPSIS</span></span>
<span data-ttu-id="684b4-103">從群集中移除服務結構應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="684b4-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="684b4-104">這會移除此資源下的所有類型版本。</span><span class="sxs-lookup"><span data-stu-id="684b4-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="684b4-105">僅支援 ARM 已部署的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="684b4-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="684b4-106">句法</span><span class="sxs-lookup"><span data-stu-id="684b4-106">SYNTAX</span></span>

### <span data-ttu-id="684b4-107">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="684b4-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="684b4-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="684b4-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="684b4-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="684b4-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="684b4-110">說明</span><span class="sxs-lookup"><span data-stu-id="684b4-110">DESCRIPTION</span></span>
<span data-ttu-id="684b4-111">這個 Cmdlet 會從群集中移除應用程式類型，並移除此資源下的所有類型版本，但在執行此命令前，必須移除所有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="684b4-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="684b4-112">示例</span><span class="sxs-lookup"><span data-stu-id="684b4-112">EXAMPLES</span></span>

### <span data-ttu-id="684b4-113">範例1</span><span class="sxs-lookup"><span data-stu-id="684b4-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="684b4-114">這個範例會移除應用程式類型 "testAppType" 以及它底下的所有版本。</span><span class="sxs-lookup"><span data-stu-id="684b4-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="684b4-115">如果有使用此類型建立的任何應用程式，命令就會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="684b4-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="684b4-116">參數</span><span class="sxs-lookup"><span data-stu-id="684b4-116">PARAMETERS</span></span>

### <span data-ttu-id="684b4-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="684b4-117">-ClusterName</span></span>
<span data-ttu-id="684b4-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="684b4-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="684b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684b4-119">-DefaultProfile</span></span>
<span data-ttu-id="684b4-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="684b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="684b4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="684b4-121">-Force</span></span>
<span data-ttu-id="684b4-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="684b4-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="684b4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="684b4-123">-InputObject</span></span>
<span data-ttu-id="684b4-124">[應用程式類型] 資源。</span><span class="sxs-lookup"><span data-stu-id="684b4-124">The application type resource.</span></span>

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

### <span data-ttu-id="684b4-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="684b4-125">-Name</span></span>
<span data-ttu-id="684b4-126">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="684b4-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="684b4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="684b4-127">-PassThru</span></span>
<span data-ttu-id="684b4-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="684b4-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="684b4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684b4-129">-ResourceGroupName</span></span>
<span data-ttu-id="684b4-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="684b4-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="684b4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="684b4-131">-ResourceId</span></span>
<span data-ttu-id="684b4-132">應用程式類型的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="684b4-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="684b4-133">-確認</span><span class="sxs-lookup"><span data-stu-id="684b4-133">-Confirm</span></span>
<span data-ttu-id="684b4-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="684b4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684b4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684b4-135">-WhatIf</span></span>
<span data-ttu-id="684b4-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="684b4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684b4-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="684b4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684b4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684b4-138">CommonParameters</span></span>
<span data-ttu-id="684b4-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="684b4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684b4-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="684b4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684b4-141">輸入</span><span class="sxs-lookup"><span data-stu-id="684b4-141">INPUTS</span></span>

### <span data-ttu-id="684b4-142">System.object</span><span class="sxs-lookup"><span data-stu-id="684b4-142">System.String</span></span>

### <span data-ttu-id="684b4-143">PSApplicationType 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="684b4-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="684b4-144">輸出</span><span class="sxs-lookup"><span data-stu-id="684b4-144">OUTPUTS</span></span>

### <span data-ttu-id="684b4-145">System.object</span><span class="sxs-lookup"><span data-stu-id="684b4-145">System.Boolean</span></span>

## <span data-ttu-id="684b4-146">筆記</span><span class="sxs-lookup"><span data-stu-id="684b4-146">NOTES</span></span>

## <span data-ttu-id="684b4-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="684b4-147">RELATED LINKS</span></span>
