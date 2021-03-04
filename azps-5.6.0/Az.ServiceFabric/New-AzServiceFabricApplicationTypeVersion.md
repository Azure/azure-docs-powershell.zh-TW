---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: d13e2e4473c390a27be4741de703818bda769efa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903765"
---
# <span data-ttu-id="1275d-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1275d-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="1275d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1275d-102">SYNOPSIS</span></span>
<span data-ttu-id="1275d-103">在指定的資源群組和群組下建立新應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="1275d-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="1275d-104">語法</span><span class="sxs-lookup"><span data-stu-id="1275d-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1275d-105">描述</span><span class="sxs-lookup"><span data-stu-id="1275d-105">DESCRIPTION</span></span>
<span data-ttu-id="1275d-106">此 Cmdlet 會使用 -PackageUrl 中指定的套件來建立新的應用程式類型版本，這應該可透過 REST 端點讓 Azure Resource Manager 在部署期間使用，並包含封裝及壓縮副檔名 .sfpkg 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1275d-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="1275d-107">如果應用程式類型不存在，此命令會建立應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="1275d-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="1275d-108">例子</span><span class="sxs-lookup"><span data-stu-id="1275d-108">EXAMPLES</span></span>

### <span data-ttu-id="1275d-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="1275d-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="1275d-110">此範例將在類型為 "testAppType" 下建立應用程式類型版本 "v1"。</span><span class="sxs-lookup"><span data-stu-id="1275d-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="1275d-111">套件中包含的應用程式清單版本應該與 -Version 中指定的版本相同。</span><span class="sxs-lookup"><span data-stu-id="1275d-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="1275d-112">參數</span><span class="sxs-lookup"><span data-stu-id="1275d-112">PARAMETERS</span></span>

### <span data-ttu-id="1275d-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1275d-113">-ClusterName</span></span>
<span data-ttu-id="1275d-114">指定組名。</span><span class="sxs-lookup"><span data-stu-id="1275d-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1275d-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="1275d-115">-DefaultParameter</span></span>
<span data-ttu-id="1275d-116">將應用程式參數的預設值指定為按鍵/值組。</span><span class="sxs-lookup"><span data-stu-id="1275d-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="1275d-117">這些參數必須存在於應用程式清單中。</span><span class="sxs-lookup"><span data-stu-id="1275d-117">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1275d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1275d-118">-DefaultProfile</span></span>
<span data-ttu-id="1275d-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1275d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1275d-120">-強制</span><span class="sxs-lookup"><span data-stu-id="1275d-120">-Force</span></span>
<span data-ttu-id="1275d-121">繼續但不提示</span><span class="sxs-lookup"><span data-stu-id="1275d-121">Continue without prompts</span></span>

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

### <span data-ttu-id="1275d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1275d-122">-Name</span></span>
<span data-ttu-id="1275d-123">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="1275d-123">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1275d-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="1275d-124">-PackageUrl</span></span>
<span data-ttu-id="1275d-125">指定應用程式套件 sfpkg 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="1275d-125">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1275d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1275d-126">-ResourceGroupName</span></span>
<span data-ttu-id="1275d-127">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1275d-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1275d-128">-版本</span><span class="sxs-lookup"><span data-stu-id="1275d-128">-Version</span></span>
<span data-ttu-id="1275d-129">指定應用程式類型版本</span><span class="sxs-lookup"><span data-stu-id="1275d-129">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeVersion

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1275d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="1275d-130">-Confirm</span></span>
<span data-ttu-id="1275d-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1275d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1275d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1275d-132">-WhatIf</span></span>
<span data-ttu-id="1275d-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1275d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1275d-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1275d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1275d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1275d-135">CommonParameters</span></span>
<span data-ttu-id="1275d-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1275d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1275d-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1275d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1275d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="1275d-138">INPUTS</span></span>

### <span data-ttu-id="1275d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1275d-139">System.String</span></span>

### <span data-ttu-id="1275d-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1275d-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1275d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="1275d-141">OUTPUTS</span></span>

### <span data-ttu-id="1275d-142">Microsoft.Azure.Commands.ServiceFabric.models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="1275d-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="1275d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="1275d-143">NOTES</span></span>

## <span data-ttu-id="1275d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="1275d-144">RELATED LINKS</span></span>
