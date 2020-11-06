---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442507"
---
# <span data-ttu-id="60366-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="60366-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="60366-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60366-102">SYNOPSIS</span></span>
<span data-ttu-id="60366-103">在服務拓朴中的服務下建立新的服務單元。</span><span class="sxs-lookup"><span data-stu-id="60366-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="60366-104">句法</span><span class="sxs-lookup"><span data-stu-id="60366-104">SYNTAX</span></span>

### <span data-ttu-id="60366-105">ByTopologyAndServiceNames (預設) </span><span class="sxs-lookup"><span data-stu-id="60366-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60366-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="60366-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60366-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="60366-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60366-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="60366-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60366-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="60366-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60366-110">說明</span><span class="sxs-lookup"><span data-stu-id="60366-110">DESCRIPTION</span></span>
<span data-ttu-id="60366-111">**新的-AzureRmDeploymentManagerServiceUnit** Cmdlet 會在服務拓朴中的服務下建立服務，並傳回代表該服務單元的物件。</span><span class="sxs-lookup"><span data-stu-id="60366-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="60366-112">依其名稱、服務名稱、服務拓撲結構，以及資源組名稱來指定服務單位。</span><span class="sxs-lookup"><span data-stu-id="60366-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="60366-113">這個 Cmdlet 會傳回 ServiceUnit 物件。</span><span class="sxs-lookup"><span data-stu-id="60366-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="60366-114">您可以在本機修改這個物件，然後使用 Set-AzureRmDeploymentManagerService Cmdlet 將變更套用至服務。</span><span class="sxs-lookup"><span data-stu-id="60366-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="60366-115">示例</span><span class="sxs-lookup"><span data-stu-id="60366-115">EXAMPLES</span></span>

### <span data-ttu-id="60366-116">範例1</span><span class="sxs-lookup"><span data-stu-id="60366-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="60366-117">這個 Cmdlet 會在 ContosoResourceGroup 中的 [拓撲 ContosoServiceTopology 的服務 ContosoService2] 下，于 [位置] 中央，建立一個新的服務單元，並將 name ContosoService2Storage 在中。</span><span class="sxs-lookup"><span data-stu-id="60366-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="60366-118">範本和參數檔案會定義為 [服務拓撲 ContosoServiceTopology] 中所參照之專案來源位置的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="60366-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="60366-119">此範本中定義的資源將會部署到目標資源群組 service2ResourceGroup，並將部署模式設為 [遞增]。</span><span class="sxs-lookup"><span data-stu-id="60366-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="60366-120">範例2</span><span class="sxs-lookup"><span data-stu-id="60366-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="60366-121">這個 Cmdlet 會在 ContosoResourceGroup 中的 [拓撲 ContosoServiceTopology 的服務 ContosoService2] 下，于 [位置] 中央，建立一個新的服務單元，並將 name ContosoService2Storage 在中。</span><span class="sxs-lookup"><span data-stu-id="60366-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="60366-122">範本和參數參照是以 SAS Uri 的形式提供，因為服務拓撲 ContosoServiceTopology1 中未提供專案來源資源 Id。</span><span class="sxs-lookup"><span data-stu-id="60366-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="60366-123">此範本中定義的資源將會部署到目標資源群組 service2ResourceGroup，並將部署模式設定為 [完成]。</span><span class="sxs-lookup"><span data-stu-id="60366-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="60366-124">參數</span><span class="sxs-lookup"><span data-stu-id="60366-124">PARAMETERS</span></span>

### <span data-ttu-id="60366-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60366-125">-AsJob</span></span>
<span data-ttu-id="60366-126">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="60366-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60366-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60366-127">-DefaultProfile</span></span>
<span data-ttu-id="60366-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60366-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60366-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="60366-129">-DeploymentMode</span></span>
<span data-ttu-id="60366-130">部署服務單元中的資源時要使用的部署模式。</span><span class="sxs-lookup"><span data-stu-id="60366-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="60366-131">-位置</span><span class="sxs-lookup"><span data-stu-id="60366-131">-Location</span></span>
<span data-ttu-id="60366-132">服務單元資源的位置。</span><span class="sxs-lookup"><span data-stu-id="60366-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="60366-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="60366-133">-Name</span></span>
<span data-ttu-id="60366-134">服務單元的名稱。</span><span class="sxs-lookup"><span data-stu-id="60366-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="60366-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="60366-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="60366-136">部署服務單元中的資源時要使用的部署模式。</span><span class="sxs-lookup"><span data-stu-id="60366-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="60366-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="60366-137">-ParametersUri</span></span>
<span data-ttu-id="60366-138">部署服務單元中的資源時要使用的部署模式。</span><span class="sxs-lookup"><span data-stu-id="60366-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="60366-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60366-139">-ResourceGroupName</span></span>
<span data-ttu-id="60366-140">[資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="60366-140">The resource group.</span></span>

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

### <span data-ttu-id="60366-141">-服務</span><span class="sxs-lookup"><span data-stu-id="60366-141">-Service</span></span>
<span data-ttu-id="60366-142">應該在其中建立服務單元的服務物件。</span><span class="sxs-lookup"><span data-stu-id="60366-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="60366-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="60366-143">-ServiceName</span></span>
<span data-ttu-id="60366-144">此服務單元所屬的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="60366-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="60366-145">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="60366-145">-ServiceResourceId</span></span>
<span data-ttu-id="60366-146">在其中建立服務單元的服務資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60366-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="60366-147">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="60366-147">-ServiceTopology</span></span>
<span data-ttu-id="60366-148">應該在其中建立服務單元的服務拓撲物件。</span><span class="sxs-lookup"><span data-stu-id="60366-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="60366-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="60366-149">-ServiceTopologyName</span></span>
<span data-ttu-id="60366-150">此服務單元所屬的服務拓撲的名稱。</span><span class="sxs-lookup"><span data-stu-id="60366-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="60366-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="60366-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="60366-152">在其中建立服務單元的服務拓撲資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60366-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="60366-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="60366-153">-Tag</span></span>
<span data-ttu-id="60366-154">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="60366-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="60366-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="60366-155">-TargetResourceGroup</span></span>
<span data-ttu-id="60366-156">決定要將服務單元下的資源部署到哪個位置。</span><span class="sxs-lookup"><span data-stu-id="60366-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="60366-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="60366-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="60366-158">部署服務單元中的資源時要使用的部署模式。</span><span class="sxs-lookup"><span data-stu-id="60366-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="60366-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="60366-159">-TemplateUri</span></span>
<span data-ttu-id="60366-160">部署服務單元中的資源時要使用的部署模式。</span><span class="sxs-lookup"><span data-stu-id="60366-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="60366-161">-確認</span><span class="sxs-lookup"><span data-stu-id="60366-161">-Confirm</span></span>
<span data-ttu-id="60366-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60366-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60366-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60366-163">-WhatIf</span></span>
<span data-ttu-id="60366-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60366-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60366-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60366-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60366-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60366-166">CommonParameters</span></span>
<span data-ttu-id="60366-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60366-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60366-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60366-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60366-169">輸入</span><span class="sxs-lookup"><span data-stu-id="60366-169">INPUTS</span></span>

### <span data-ttu-id="60366-170">所有</span><span class="sxs-lookup"><span data-stu-id="60366-170">None</span></span>

## <span data-ttu-id="60366-171">輸出</span><span class="sxs-lookup"><span data-stu-id="60366-171">OUTPUTS</span></span>

### <span data-ttu-id="60366-172">PSServiceUnitResource 中的 DeploymentManager。</span><span class="sxs-lookup"><span data-stu-id="60366-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="60366-173">筆記</span><span class="sxs-lookup"><span data-stu-id="60366-173">NOTES</span></span>

## <span data-ttu-id="60366-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="60366-174">RELATED LINKS</span></span>

[<span data-ttu-id="60366-175">AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="60366-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="60366-176">移除-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="60366-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="60366-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="60366-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)