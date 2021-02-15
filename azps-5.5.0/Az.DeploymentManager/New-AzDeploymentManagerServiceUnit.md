---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142679"
---
# <span data-ttu-id="669e3-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="669e3-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="669e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="669e3-102">SYNOPSIS</span></span>
<span data-ttu-id="669e3-103">在指定的服務和服務拓撲結構下建立服務單元。</span><span class="sxs-lookup"><span data-stu-id="669e3-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="669e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="669e3-104">SYNTAX</span></span>

### <span data-ttu-id="669e3-105">ByTopologyAndServiceNames (預設) </span><span class="sxs-lookup"><span data-stu-id="669e3-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="669e3-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="669e3-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669e3-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="669e3-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669e3-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="669e3-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="669e3-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="669e3-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="669e3-110">說明</span><span class="sxs-lookup"><span data-stu-id="669e3-110">DESCRIPTION</span></span>
<span data-ttu-id="669e3-111">**新的-AzDeploymentManagerServiceUnit** Cmdlet 會在服務拓朴中的服務下建立服務，並傳回代表該服務單元的物件。</span><span class="sxs-lookup"><span data-stu-id="669e3-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="669e3-112">依其名稱、服務名稱、服務拓撲結構，以及資源組名稱來指定服務單位。</span><span class="sxs-lookup"><span data-stu-id="669e3-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="669e3-113">這個 Cmdlet 會傳回 ServiceUnit 物件。</span><span class="sxs-lookup"><span data-stu-id="669e3-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="669e3-114">您可以在本機修改這個物件，然後使用 Set-AzDeploymentManagerService Cmdlet 將變更套用至服務。</span><span class="sxs-lookup"><span data-stu-id="669e3-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="669e3-115">示例</span><span class="sxs-lookup"><span data-stu-id="669e3-115">EXAMPLES</span></span>

### <span data-ttu-id="669e3-116">範例1</span><span class="sxs-lookup"><span data-stu-id="669e3-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="669e3-117">這個 Cmdlet 會在 ContosoResourceGroup 中的 [拓撲 ContosoServiceTopology 的服務 ContosoService2] 下，于 [位置] 中央，建立一個新的服務單元，並將 name ContosoService2Storage 在中。</span><span class="sxs-lookup"><span data-stu-id="669e3-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="669e3-118">範本和參數檔案會定義為 [服務拓撲 ContosoServiceTopology] 中所參照之專案來源位置的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="669e3-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="669e3-119">此範本中定義的資源將會部署到目標資源群組 service2ResourceGroup，並將部署模式設為 [遞增]。</span><span class="sxs-lookup"><span data-stu-id="669e3-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="669e3-120">範例2</span><span class="sxs-lookup"><span data-stu-id="669e3-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="669e3-121">這個 Cmdlet 會在 ContosoResourceGroup 中的 [拓撲 ContosoServiceTopology 的服務 ContosoService2] 下，于 [位置] 中央，建立一個新的服務單元，並將 name ContosoService2Storage 在中。</span><span class="sxs-lookup"><span data-stu-id="669e3-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="669e3-122">範本和參數參照是以 SAS Uri 的形式提供，因為服務拓撲 ContosoServiceTopology1 中未提供專案來源資源 Id。</span><span class="sxs-lookup"><span data-stu-id="669e3-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="669e3-123">此範本中定義的資源將會部署到目標資源群組 service2ResourceGroup，並將部署模式設定為 [完成]。</span><span class="sxs-lookup"><span data-stu-id="669e3-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="669e3-124">參數</span><span class="sxs-lookup"><span data-stu-id="669e3-124">PARAMETERS</span></span>

### <span data-ttu-id="669e3-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="669e3-125">-AsJob</span></span>
<span data-ttu-id="669e3-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="669e3-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="669e3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="669e3-127">-DefaultProfile</span></span>
<span data-ttu-id="669e3-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="669e3-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="669e3-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="669e3-129">-DeploymentMode</span></span>
<span data-ttu-id="669e3-130">部署服務單元中的資源時要使用的部署模式。</span><span class="sxs-lookup"><span data-stu-id="669e3-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="669e3-131">-位置</span><span class="sxs-lookup"><span data-stu-id="669e3-131">-Location</span></span>
<span data-ttu-id="669e3-132">服務單元資源的位置。</span><span class="sxs-lookup"><span data-stu-id="669e3-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="669e3-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="669e3-133">-Name</span></span>
<span data-ttu-id="669e3-134">服務單元的名稱。</span><span class="sxs-lookup"><span data-stu-id="669e3-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="669e3-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="669e3-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="669e3-136">相對於專案源的參數檔路徑。</span><span class="sxs-lookup"><span data-stu-id="669e3-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="669e3-137">需要在 ServiceTopology 中參照 ArtifactSource。</span><span class="sxs-lookup"><span data-stu-id="669e3-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="669e3-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="669e3-138">-ParametersUri</span></span>
<span data-ttu-id="669e3-139">參數檔的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="669e3-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="669e3-140">如果在 ServiceTopology 中參照了 ArtifactSourceId，請使用 ParametersArtifactSourceRelativePath 指定相對路徑。</span><span class="sxs-lookup"><span data-stu-id="669e3-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="669e3-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="669e3-141">-ResourceGroupName</span></span>
<span data-ttu-id="669e3-142">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="669e3-142">The resource group.</span></span>

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

### <span data-ttu-id="669e3-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="669e3-143">-ServiceName</span></span>
<span data-ttu-id="669e3-144">此服務單元所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="669e3-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="669e3-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="669e3-145">-ServiceObject</span></span>
<span data-ttu-id="669e3-146">應該在其中建立服務單元的服務物件。</span><span class="sxs-lookup"><span data-stu-id="669e3-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="669e3-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="669e3-147">-ServiceResourceId</span></span>
<span data-ttu-id="669e3-148">在其中建立服務單元的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="669e3-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="669e3-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="669e3-149">-ServiceTopologyName</span></span>
<span data-ttu-id="669e3-150">此服務單元所屬的服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="669e3-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="669e3-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="669e3-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="669e3-152">應該在其中建立服務單元的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="669e3-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="669e3-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="669e3-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="669e3-154">在其中建立服務單元的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="669e3-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="669e3-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="669e3-155">-Tag</span></span>
<span data-ttu-id="669e3-156">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="669e3-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="669e3-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="669e3-157">-TargetResourceGroup</span></span>
<span data-ttu-id="669e3-158">決定要將服務單元下的資源部署到哪個位置。</span><span class="sxs-lookup"><span data-stu-id="669e3-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="669e3-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="669e3-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="669e3-160">相對於專案來源的範本檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="669e3-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="669e3-161">需要在 ServiceTopology 中參照 ArtifactSource。</span><span class="sxs-lookup"><span data-stu-id="669e3-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="669e3-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="669e3-162">-TemplateUri</span></span>
<span data-ttu-id="669e3-163">範本檔案的 SAS Uri。</span><span class="sxs-lookup"><span data-stu-id="669e3-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="669e3-164">如果在 ServiceTopology 中參照了 ArtifactSourceId，請使用 TemplateArtifactSourceRelativePath 指定相對路徑。</span><span class="sxs-lookup"><span data-stu-id="669e3-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="669e3-165">-確認</span><span class="sxs-lookup"><span data-stu-id="669e3-165">-Confirm</span></span>
<span data-ttu-id="669e3-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="669e3-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="669e3-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="669e3-167">-WhatIf</span></span>
<span data-ttu-id="669e3-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="669e3-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="669e3-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="669e3-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="669e3-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669e3-170">CommonParameters</span></span>
<span data-ttu-id="669e3-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="669e3-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669e3-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="669e3-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669e3-173">輸入</span><span class="sxs-lookup"><span data-stu-id="669e3-173">INPUTS</span></span>

### <span data-ttu-id="669e3-174">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="669e3-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="669e3-175">輸出</span><span class="sxs-lookup"><span data-stu-id="669e3-175">OUTPUTS</span></span>

### <span data-ttu-id="669e3-176">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="669e3-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="669e3-177">筆記</span><span class="sxs-lookup"><span data-stu-id="669e3-177">NOTES</span></span>

## <span data-ttu-id="669e3-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="669e3-178">RELATED LINKS</span></span>
