---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 217666284a2245b79864bb6561a1f85143c1ae80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915845"
---
# <span data-ttu-id="a97af-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a97af-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="a97af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a97af-102">SYNOPSIS</span></span>
<span data-ttu-id="a97af-103">從組集中移除服務結構的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="a97af-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="a97af-104">僅支援 ARM 部署的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="a97af-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="a97af-105">語法</span><span class="sxs-lookup"><span data-stu-id="a97af-105">SYNTAX</span></span>

### <span data-ttu-id="a97af-106">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="a97af-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a97af-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a97af-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a97af-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a97af-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a97af-109">描述</span><span class="sxs-lookup"><span data-stu-id="a97af-109">DESCRIPTION</span></span>
<span data-ttu-id="a97af-110">此 Cmdlet 會從該組組移除 Service 結構的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="a97af-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="a97af-111">執行此命令之前，必須先移除此資源下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="a97af-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="a97af-112">例子</span><span class="sxs-lookup"><span data-stu-id="a97af-112">EXAMPLES</span></span>

### <span data-ttu-id="a97af-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="a97af-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="a97af-114">此範例會移除 "testAppType" 類型下的版本 "v1"。</span><span class="sxs-lookup"><span data-stu-id="a97af-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="a97af-115">此資源下有任何應用程式，該命令會引發例外。</span><span class="sxs-lookup"><span data-stu-id="a97af-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="a97af-116">參數</span><span class="sxs-lookup"><span data-stu-id="a97af-116">PARAMETERS</span></span>

### <span data-ttu-id="a97af-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a97af-117">-ClusterName</span></span>
<span data-ttu-id="a97af-118">指定組名。</span><span class="sxs-lookup"><span data-stu-id="a97af-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a97af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97af-119">-DefaultProfile</span></span>
<span data-ttu-id="a97af-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a97af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a97af-121">-強制</span><span class="sxs-lookup"><span data-stu-id="a97af-121">-Force</span></span>
<span data-ttu-id="a97af-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="a97af-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="a97af-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a97af-123">-InputObject</span></span>
<span data-ttu-id="a97af-124">應用程式類型版本資源。</span><span class="sxs-lookup"><span data-stu-id="a97af-124">The application type version resource.</span></span>

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

### <span data-ttu-id="a97af-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a97af-125">-Name</span></span>
<span data-ttu-id="a97af-126">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="a97af-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="a97af-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a97af-127">-PassThru</span></span>
<span data-ttu-id="a97af-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a97af-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a97af-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97af-129">-ResourceGroupName</span></span>
<span data-ttu-id="a97af-130">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a97af-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a97af-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a97af-131">-ResourceId</span></span>
<span data-ttu-id="a97af-132">應用程式類型版本的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="a97af-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="a97af-133">-版本</span><span class="sxs-lookup"><span data-stu-id="a97af-133">-Version</span></span>
<span data-ttu-id="a97af-134">指定應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="a97af-134">Specify the application type version.</span></span>

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

### <span data-ttu-id="a97af-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a97af-135">-Confirm</span></span>
<span data-ttu-id="a97af-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a97af-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a97af-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a97af-137">-WhatIf</span></span>
<span data-ttu-id="a97af-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a97af-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a97af-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a97af-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a97af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97af-140">CommonParameters</span></span>
<span data-ttu-id="a97af-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a97af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97af-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a97af-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97af-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a97af-143">INPUTS</span></span>

### <span data-ttu-id="a97af-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a97af-144">System.String</span></span>

### <span data-ttu-id="a97af-145">Microsoft.Azure.Commands.ServiceFabric.models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="a97af-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="a97af-146">輸出</span><span class="sxs-lookup"><span data-stu-id="a97af-146">OUTPUTS</span></span>

### <span data-ttu-id="a97af-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a97af-147">System.Boolean</span></span>

## <span data-ttu-id="a97af-148">筆記</span><span class="sxs-lookup"><span data-stu-id="a97af-148">NOTES</span></span>

## <span data-ttu-id="a97af-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="a97af-149">RELATED LINKS</span></span>
