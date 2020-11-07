---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 69bbcbbd508a5bf32163b91378aab62dbdcb3a64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957668"
---
# <span data-ttu-id="91f5e-101">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="91f5e-101">New-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="91f5e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="91f5e-103">在指定的資源群組和群集底下建立新的應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="91f5e-103">Create new application type version under the specified resource group and cluster.</span></span>

## <span data-ttu-id="91f5e-104">句法</span><span class="sxs-lookup"><span data-stu-id="91f5e-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> [-Version] <String> -PackageUrl <String> [-DefaultParameter <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91f5e-105">說明</span><span class="sxs-lookup"><span data-stu-id="91f5e-105">DESCRIPTION</span></span>
<span data-ttu-id="91f5e-106">這個 Cmdlet 會使用在-PackageUrl 中指定的套件來建立新的應用程式類型版本，這應該可透過 Azure 資源管理員的 REST 端點存取，以在部署期間進行，並包含使用副檔名 sfpkg 封裝和 zipped 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="91f5e-106">This cmdlet creates a new application type version using the package specified in -PackageUrl, this should be accessible through a REST endpoint for Azure Resource Manager to consume during deployment and contained The application packaged and zipped with the extension .sfpkg.</span></span> <span data-ttu-id="91f5e-107">如果應用程式類型尚不存在，此命令會建立它。</span><span class="sxs-lookup"><span data-stu-id="91f5e-107">This command will create the application type if it doesn't exist already.</span></span>

## <span data-ttu-id="91f5e-108">示例</span><span class="sxs-lookup"><span data-stu-id="91f5e-108">EXAMPLES</span></span>

### <span data-ttu-id="91f5e-109">範例1</span><span class="sxs-lookup"><span data-stu-id="91f5e-109">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> $packageUrl = "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg"
PS C:\> New-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -PackageUrl $packageUrl -Verbose
```

<span data-ttu-id="91f5e-110">這個範例會在輸入 "testAppType" 下建立應用程式類型版本 "v1"。</span><span class="sxs-lookup"><span data-stu-id="91f5e-110">This example will create an application type version "v1" under type "testAppType".</span></span> <span data-ttu-id="91f5e-111">套件中包含的應用程式資訊清單版本應該與版本中所指定的版本相同。</span><span class="sxs-lookup"><span data-stu-id="91f5e-111">The version in the application manifest contained in the package should have the same version as the one specified in -Version.</span></span>

## <span data-ttu-id="91f5e-112">參數</span><span class="sxs-lookup"><span data-stu-id="91f5e-112">PARAMETERS</span></span>

### <span data-ttu-id="91f5e-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="91f5e-113">-ClusterName</span></span>
<span data-ttu-id="91f5e-114">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="91f5e-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="91f5e-115">-DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="91f5e-115">-DefaultParameter</span></span>
<span data-ttu-id="91f5e-116">指定應用程式參數的預設值做為鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="91f5e-116">Specify the default values of the application parameters as key/value pairs.</span></span>
<span data-ttu-id="91f5e-117">這些參數必須存在於應用程式資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="91f5e-117">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="91f5e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f5e-118">-DefaultProfile</span></span>
<span data-ttu-id="91f5e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91f5e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f5e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="91f5e-120">-Force</span></span>
<span data-ttu-id="91f5e-121">繼續但不提示</span><span class="sxs-lookup"><span data-stu-id="91f5e-121">Continue without prompts</span></span>

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

### <span data-ttu-id="91f5e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="91f5e-122">-Name</span></span>
<span data-ttu-id="91f5e-123">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="91f5e-123">Specify the name of the application type</span></span>

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

### <span data-ttu-id="91f5e-124">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="91f5e-124">-PackageUrl</span></span>
<span data-ttu-id="91f5e-125">指定應用程式套件 sfpkg 檔案的 url</span><span class="sxs-lookup"><span data-stu-id="91f5e-125">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="91f5e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f5e-126">-ResourceGroupName</span></span>
<span data-ttu-id="91f5e-127">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91f5e-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="91f5e-128">-版本</span><span class="sxs-lookup"><span data-stu-id="91f5e-128">-Version</span></span>
<span data-ttu-id="91f5e-129">指定應用程式類型版本</span><span class="sxs-lookup"><span data-stu-id="91f5e-129">Specify the application type version</span></span>

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

### <span data-ttu-id="91f5e-130">-確認</span><span class="sxs-lookup"><span data-stu-id="91f5e-130">-Confirm</span></span>
<span data-ttu-id="91f5e-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91f5e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f5e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f5e-132">-WhatIf</span></span>
<span data-ttu-id="91f5e-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91f5e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f5e-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91f5e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f5e-135">CommonParameters</span></span>
<span data-ttu-id="91f5e-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91f5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f5e-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91f5e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f5e-138">輸入</span><span class="sxs-lookup"><span data-stu-id="91f5e-138">INPUTS</span></span>

### <span data-ttu-id="91f5e-139">System.object</span><span class="sxs-lookup"><span data-stu-id="91f5e-139">System.String</span></span>

### <span data-ttu-id="91f5e-140">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="91f5e-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="91f5e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="91f5e-141">OUTPUTS</span></span>

### <span data-ttu-id="91f5e-142">PSApplicationTypeVersion 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="91f5e-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="91f5e-143">筆記</span><span class="sxs-lookup"><span data-stu-id="91f5e-143">NOTES</span></span>

## <span data-ttu-id="91f5e-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="91f5e-144">RELATED LINKS</span></span>
