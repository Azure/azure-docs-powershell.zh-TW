---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133563"
---
# <span data-ttu-id="61ebc-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="61ebc-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="61ebc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="61ebc-103">從群集中移除應用程式類型版本的服務結構。</span><span class="sxs-lookup"><span data-stu-id="61ebc-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="61ebc-104">僅支援 ARM 已部署的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="61ebc-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="61ebc-105">句法</span><span class="sxs-lookup"><span data-stu-id="61ebc-105">SYNTAX</span></span>

### <span data-ttu-id="61ebc-106">ByResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="61ebc-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ebc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="61ebc-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61ebc-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="61ebc-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61ebc-109">說明</span><span class="sxs-lookup"><span data-stu-id="61ebc-109">DESCRIPTION</span></span>
<span data-ttu-id="61ebc-110">這個 Cmdlet 會從群集中移除應用程式類型版本的服務結構。</span><span class="sxs-lookup"><span data-stu-id="61ebc-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="61ebc-111">執行此命令之前，必須先移除此資源底下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="61ebc-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="61ebc-112">示例</span><span class="sxs-lookup"><span data-stu-id="61ebc-112">EXAMPLES</span></span>

### <span data-ttu-id="61ebc-113">範例1</span><span class="sxs-lookup"><span data-stu-id="61ebc-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="61ebc-114">這個範例會移除類型 "testAppType" 下的版本 "v1"。</span><span class="sxs-lookup"><span data-stu-id="61ebc-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="61ebc-115">此資源下有任何應用程式，命令會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="61ebc-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="61ebc-116">參數</span><span class="sxs-lookup"><span data-stu-id="61ebc-116">PARAMETERS</span></span>

### <span data-ttu-id="61ebc-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="61ebc-117">-ClusterName</span></span>
<span data-ttu-id="61ebc-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="61ebc-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="61ebc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61ebc-119">-DefaultProfile</span></span>
<span data-ttu-id="61ebc-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61ebc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61ebc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="61ebc-121">-Force</span></span>
<span data-ttu-id="61ebc-122">移除而不提示。</span><span class="sxs-lookup"><span data-stu-id="61ebc-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="61ebc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61ebc-123">-InputObject</span></span>
<span data-ttu-id="61ebc-124">應用程式類型版本資源。</span><span class="sxs-lookup"><span data-stu-id="61ebc-124">The application type version resource.</span></span>

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

### <span data-ttu-id="61ebc-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="61ebc-125">-Name</span></span>
<span data-ttu-id="61ebc-126">指定應用程式類型的名稱。</span><span class="sxs-lookup"><span data-stu-id="61ebc-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="61ebc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61ebc-127">-PassThru</span></span>
<span data-ttu-id="61ebc-128">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="61ebc-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="61ebc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61ebc-129">-ResourceGroupName</span></span>
<span data-ttu-id="61ebc-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61ebc-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="61ebc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61ebc-131">-ResourceId</span></span>
<span data-ttu-id="61ebc-132">應用程式類型版本的 Arm ResourceId。</span><span class="sxs-lookup"><span data-stu-id="61ebc-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="61ebc-133">-版本</span><span class="sxs-lookup"><span data-stu-id="61ebc-133">-Version</span></span>
<span data-ttu-id="61ebc-134">指定應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="61ebc-134">Specify the application type version.</span></span>

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

### <span data-ttu-id="61ebc-135">-確認</span><span class="sxs-lookup"><span data-stu-id="61ebc-135">-Confirm</span></span>
<span data-ttu-id="61ebc-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61ebc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61ebc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61ebc-137">-WhatIf</span></span>
<span data-ttu-id="61ebc-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61ebc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61ebc-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61ebc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61ebc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61ebc-140">CommonParameters</span></span>
<span data-ttu-id="61ebc-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61ebc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61ebc-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="61ebc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61ebc-143">輸入</span><span class="sxs-lookup"><span data-stu-id="61ebc-143">INPUTS</span></span>

### <span data-ttu-id="61ebc-144">System.object</span><span class="sxs-lookup"><span data-stu-id="61ebc-144">System.String</span></span>

### <span data-ttu-id="61ebc-145">PSApplicationTypeVersion 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="61ebc-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="61ebc-146">輸出</span><span class="sxs-lookup"><span data-stu-id="61ebc-146">OUTPUTS</span></span>

### <span data-ttu-id="61ebc-147">System.object</span><span class="sxs-lookup"><span data-stu-id="61ebc-147">System.Boolean</span></span>

## <span data-ttu-id="61ebc-148">筆記</span><span class="sxs-lookup"><span data-stu-id="61ebc-148">NOTES</span></span>

## <span data-ttu-id="61ebc-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="61ebc-149">RELATED LINKS</span></span>
