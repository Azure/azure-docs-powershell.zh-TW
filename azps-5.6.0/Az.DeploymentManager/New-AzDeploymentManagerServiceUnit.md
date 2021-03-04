---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 5c4b418812c6cbe3ee1b5e1f8ee82baa05723f86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904462"
---
# <span data-ttu-id="dd5ae-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="dd5ae-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="dd5ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dd5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5ae-103">在指定的服務與服務拓撲下建立服務單位。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="dd5ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="dd5ae-104">SYNTAX</span></span>

### <span data-ttu-id="dd5ae-105">ByTopserviceAndServiceNames (預設) </span><span class="sxs-lookup"><span data-stu-id="dd5ae-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd5ae-106">ByTopserviceObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="dd5ae-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5ae-107">ByTopserviceResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="dd5ae-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5ae-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="dd5ae-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5ae-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5ae-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd5ae-110">描述</span><span class="sxs-lookup"><span data-stu-id="dd5ae-110">DESCRIPTION</span></span>
<span data-ttu-id="dd5ae-111">**New-AzDeploymentManagerServiceUnit** Cmdlet 會依據服務拓撲的服務建立服務，並返回代表該服務單位的物件。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="dd5ae-112">根據服務單位的名稱、服務名稱、服務拓撲及資源組名來指定服務單位。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="dd5ae-113">Cmdlet 會返回 ServiceUnit 物件。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="dd5ae-114">您可以在本地修改此物件，然後使用 Cmdlet 將變更Set-AzDeploymentManagerService服務。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="dd5ae-115">例子</span><span class="sxs-lookup"><span data-stu-id="dd5ae-115">EXAMPLES</span></span>

### <span data-ttu-id="dd5ae-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="dd5ae-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="dd5ae-117">此 Cmdlet 會建立一個新服務單元，名稱為 ContosoResourceGroup 中的 ContosoResourceGroup，服務 ContosoService2 的拓撲 ContosoServiceTopservice，位於美國中央位置。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="dd5ae-118">範本和參數檔案定義為服務拓撲 ContosoServiceTop用中參照之產品來源位置的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="dd5ae-119">此範本中定義的資源將部署至目標資源群組 Service2ResourceGroup，部署模式設定為增量。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="dd5ae-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="dd5ae-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="dd5ae-121">此 Cmdlet 會建立一個新服務單元，名稱為 ContosoResourceGroup 中的 ContosoResourceGroup，服務 ContosoService2 的拓撲 ContosoServiceTopservice，位於美國中央位置。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="dd5ae-122">服務拓撲 ContosoServiceTop地1 未提供範本和參數參照做為 SAS Uri 的做為產品來源 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="dd5ae-123">此範本中定義的資源將部署至目標資源群組 Service2ResourceGroup，部署模式設定為完成。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="dd5ae-124">參數</span><span class="sxs-lookup"><span data-stu-id="dd5ae-124">PARAMETERS</span></span>

### <span data-ttu-id="dd5ae-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd5ae-125">-AsJob</span></span>
<span data-ttu-id="dd5ae-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd5ae-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd5ae-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5ae-127">-DefaultProfile</span></span>
<span data-ttu-id="dd5ae-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd5ae-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="dd5ae-129">-DeploymentMode</span></span>
<span data-ttu-id="dd5ae-130">在服務單位中部署資源時使用的部署模式。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-131">-位置</span><span class="sxs-lookup"><span data-stu-id="dd5ae-131">-Location</span></span>
<span data-ttu-id="dd5ae-132">服務單位資源的位置。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-132">The location of the service unit resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="dd5ae-133">-Name</span></span>
<span data-ttu-id="dd5ae-134">服務單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="dd5ae-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="dd5ae-136">相對於產品來源的參數檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="dd5ae-137">需要在 ServiceTop能中參照 ArtifactSource。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="dd5ae-138">-ParametersUri</span></span>
<span data-ttu-id="dd5ae-139">參數檔案的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="dd5ae-140">如果在 ServiceTopative 中參照了 ArtifactSourceId，請用 ParametersArtifactSourceRelativePath 指定相對路徑。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5ae-141">-ResourceGroupName</span></span>
<span data-ttu-id="dd5ae-142">資源群組。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-142">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dd5ae-143">-ServiceName</span></span>
<span data-ttu-id="dd5ae-144">這個服務單位的服務名稱是其中一部分。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="dd5ae-145">-ServiceObject</span></span>
<span data-ttu-id="dd5ae-146">應建立服務單位的服務物件。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5ae-147">-ServiceResourceId</span></span>
<span data-ttu-id="dd5ae-148">應建立服務單位的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="dd5ae-149">-ServiceTopologyName</span></span>
<span data-ttu-id="dd5ae-150">這個服務單位的服務拓撲名稱是其中一部分。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-151">-ServiceTopectObject</span><span class="sxs-lookup"><span data-stu-id="dd5ae-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="dd5ae-152">應建立服務單位的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-153">-ServiceTopsourceResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5ae-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="dd5ae-154">應建立服務單位的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-155">-標記</span><span class="sxs-lookup"><span data-stu-id="dd5ae-155">-Tag</span></span>
<span data-ttu-id="dd5ae-156">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="dd5ae-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dd5ae-157">-TargetResourceGroup</span></span>
<span data-ttu-id="dd5ae-158">決定部署服務單位下資源的位置。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-158">Determines the location where resources under the service unit would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="dd5ae-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="dd5ae-160">相對於產品來源的範本檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="dd5ae-161">需要在 ServiceTop能中參照 ArtifactSource。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="dd5ae-162">-TemplateUri</span></span>
<span data-ttu-id="dd5ae-163">範本檔案的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="dd5ae-164">如果在 ServiceTopative 中參照了 ArtifactSourceId，請用 TemplateArtifactSourceRelativePath 指定相對路徑。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5ae-165">-確認</span><span class="sxs-lookup"><span data-stu-id="dd5ae-165">-Confirm</span></span>
<span data-ttu-id="dd5ae-166">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5ae-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5ae-167">-WhatIf</span></span>
<span data-ttu-id="dd5ae-168">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd5ae-169">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd5ae-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5ae-170">CommonParameters</span></span>
<span data-ttu-id="dd5ae-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dd5ae-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5ae-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd5ae-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5ae-173">輸入</span><span class="sxs-lookup"><span data-stu-id="dd5ae-173">INPUTS</span></span>

### <span data-ttu-id="dd5ae-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="dd5ae-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dd5ae-175">輸出</span><span class="sxs-lookup"><span data-stu-id="dd5ae-175">OUTPUTS</span></span>

### <span data-ttu-id="dd5ae-176">Microsoft.Azure.Commands.DeploymentManager.models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="dd5ae-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="dd5ae-177">筆記</span><span class="sxs-lookup"><span data-stu-id="dd5ae-177">NOTES</span></span>

## <span data-ttu-id="dd5ae-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd5ae-178">RELATED LINKS</span></span>
