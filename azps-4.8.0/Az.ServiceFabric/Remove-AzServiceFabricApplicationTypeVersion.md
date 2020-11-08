---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 498dec77dfc2f4ede8ae81aa70b10acfe2ad2954
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971715"
---
# <span data-ttu-id="2d067-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2d067-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="2d067-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d067-102">SYNOPSIS</span></span>
<span data-ttu-id="2d067-103">從群集中移除應用程式類型版本的服務結構。</span><span class="sxs-lookup"><span data-stu-id="2d067-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="2d067-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d067-104">SYNTAX</span></span>

### <span data-ttu-id="2d067-105">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="2d067-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d067-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2d067-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d067-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2d067-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d067-108">說明</span><span class="sxs-lookup"><span data-stu-id="2d067-108">DESCRIPTION</span></span>
<span data-ttu-id="2d067-109">這個 Cmdlet 會從群集中移除應用程式類型版本的服務結構。</span><span class="sxs-lookup"><span data-stu-id="2d067-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="2d067-110">執行此命令之前，必須先移除此資源底下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="2d067-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="2d067-111">示例</span><span class="sxs-lookup"><span data-stu-id="2d067-111">EXAMPLES</span></span>

### <span data-ttu-id="2d067-112">範例1</span><span class="sxs-lookup"><span data-stu-id="2d067-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="2d067-113">這個範例會移除類型 "testAppType" 下的版本 "v1"。</span><span class="sxs-lookup"><span data-stu-id="2d067-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="2d067-114">此資源下有任何應用程式，命令會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2d067-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="2d067-115">參數</span><span class="sxs-lookup"><span data-stu-id="2d067-115">PARAMETERS</span></span>

### <span data-ttu-id="2d067-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2d067-116">-ClusterName</span></span>
<span data-ttu-id="2d067-117">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d067-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2d067-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d067-118">-DefaultProfile</span></span>
<span data-ttu-id="2d067-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d067-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d067-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2d067-120">-Force</span></span>
<span data-ttu-id="2d067-121">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="2d067-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="2d067-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d067-122">-InputObject</span></span>
<span data-ttu-id="2d067-123">應用程式類型版本資源。</span><span class="sxs-lookup"><span data-stu-id="2d067-123">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d067-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d067-124">-Name</span></span>
<span data-ttu-id="2d067-125">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d067-125">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d067-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d067-126">-PassThru</span></span>
<span data-ttu-id="2d067-127">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="2d067-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2d067-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d067-128">-ResourceGroupName</span></span>
<span data-ttu-id="2d067-129">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d067-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2d067-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d067-130">-ResourceId</span></span>
<span data-ttu-id="2d067-131">應用程式類型版本的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="2d067-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="2d067-132">-版本</span><span class="sxs-lookup"><span data-stu-id="2d067-132">-Version</span></span>
<span data-ttu-id="2d067-133">指定應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="2d067-133">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d067-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2d067-134">-Confirm</span></span>
<span data-ttu-id="2d067-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2d067-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d067-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d067-136">-WhatIf</span></span>
<span data-ttu-id="2d067-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d067-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d067-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d067-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d067-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d067-139">CommonParameters</span></span>
<span data-ttu-id="2d067-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d067-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d067-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2d067-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d067-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2d067-142">INPUTS</span></span>

### <span data-ttu-id="2d067-143">System.object</span><span class="sxs-lookup"><span data-stu-id="2d067-143">System.String</span></span>

### <span data-ttu-id="2d067-144">PSApplicationTypeVersion 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="2d067-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="2d067-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2d067-145">OUTPUTS</span></span>

### <span data-ttu-id="2d067-146">System.object</span><span class="sxs-lookup"><span data-stu-id="2d067-146">System.Boolean</span></span>

## <span data-ttu-id="2d067-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2d067-147">NOTES</span></span>

## <span data-ttu-id="2d067-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d067-148">RELATED LINKS</span></span>
