---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 10759ac90bf1d92243a8d706be3bbb345af4669c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914057"
---
# <span data-ttu-id="cc099-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cc099-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="cc099-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc099-102">SYNOPSIS</span></span>
<span data-ttu-id="cc099-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="cc099-103">Creates a data factory.</span></span>

## <span data-ttu-id="cc099-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc099-104">SYNTAX</span></span>

### <span data-ttu-id="cc099-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="cc099-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc099-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cc099-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc099-107">ByResourceIdFactoryRepoVtsConfig</span><span class="sxs-lookup"><span data-stu-id="cc099-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc099-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="cc099-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc099-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="cc099-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc099-110">ByFactoryNameFactoryRepoVtsConfig</span><span class="sxs-lookup"><span data-stu-id="cc099-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc099-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cc099-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc099-112">ByInputObjectFactoryRepoVtsConfig</span><span class="sxs-lookup"><span data-stu-id="cc099-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc099-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="cc099-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc099-114">描述</span><span class="sxs-lookup"><span data-stu-id="cc099-114">DESCRIPTION</span></span>
<span data-ttu-id="cc099-115">**Set-AzDataFactoryV2** Cmdlet 會使用指定的資源組名和位置來建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="cc099-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="cc099-116">請以下列循序執行這些作業：建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="cc099-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="cc099-117">-- 建立連結服務。</span><span class="sxs-lookup"><span data-stu-id="cc099-117">-- Create linked services.</span></span>
<span data-ttu-id="cc099-118">-- 建立資料集。</span><span class="sxs-lookup"><span data-stu-id="cc099-118">-- Create datasets.</span></span>
<span data-ttu-id="cc099-119">-- 建立管線。</span><span class="sxs-lookup"><span data-stu-id="cc099-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="cc099-120">例子</span><span class="sxs-lookup"><span data-stu-id="cc099-120">EXAMPLES</span></span>

### <span data-ttu-id="cc099-121">範例 1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="cc099-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="cc099-122">範例 2：使用現有的 factory 物件建立具有 repo 組配置詳細資料的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="cc099-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="cc099-123">此命令會使用 Azure DevOps 原始程式碼控制組，在資源群組中建立名為 WikiADF 的資料工廠，名稱為 EastUS 位置中的 ADF。</span><span class="sxs-lookup"><span data-stu-id="cc099-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="cc099-124">範例 3：使用 GitHub repo 組配置詳細資料使用新的 factory 物件建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="cc099-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="cc099-125">此命令在具有 GitHub 原始程式碼管理配置的 EastUS 位置中名為 ADF 的資源群組中，建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="cc099-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="cc099-126">參數</span><span class="sxs-lookup"><span data-stu-id="cc099-126">PARAMETERS</span></span>

### <span data-ttu-id="cc099-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cc099-127">-AccountName</span></span>
<span data-ttu-id="cc099-128">用於 repo 設定檔的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cc099-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="cc099-129">-CollaborationBranch</span></span>
<span data-ttu-id="cc099-130">用於 Repo 配置的共同合作分支。</span><span class="sxs-lookup"><span data-stu-id="cc099-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc099-131">-DefaultProfile</span></span>
<span data-ttu-id="cc099-132">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc099-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc099-133">-強制</span><span class="sxs-lookup"><span data-stu-id="cc099-133">-Force</span></span>
<span data-ttu-id="cc099-134">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="cc099-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cc099-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="cc099-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="cc099-136">包含資料工廠全域參數的字典。</span><span class="sxs-lookup"><span data-stu-id="cc099-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="cc099-137">-HostName</span></span>
<span data-ttu-id="cc099-138">GitHub Repo 配置的主機名稱稱。</span><span class="sxs-lookup"><span data-stu-id="cc099-138">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc099-139">-InputObject</span></span>
<span data-ttu-id="cc099-140">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="cc099-140">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="cc099-141">-LastCommitId</span></span>
<span data-ttu-id="cc099-142">用於 repo 配置的上次提交識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc099-142">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-143">-位置</span><span class="sxs-lookup"><span data-stu-id="cc099-143">-Location</span></span>
<span data-ttu-id="cc099-144">資料工廠是在這個地區建立。</span><span class="sxs-lookup"><span data-stu-id="cc099-144">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc099-145">-Name</span></span>
<span data-ttu-id="cc099-146">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="cc099-146">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-147">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="cc099-147">-ProjectName</span></span>
<span data-ttu-id="cc099-148">專案名稱 Azure DevOps for repo configuration。</span><span class="sxs-lookup"><span data-stu-id="cc099-148">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="cc099-149">-RepositoryName</span></span>
<span data-ttu-id="cc099-150">用於 repo 配置的存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="cc099-150">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc099-151">-ResourceGroupName</span></span>
<span data-ttu-id="cc099-152">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cc099-152">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc099-153">-ResourceId</span></span>
<span data-ttu-id="cc099-154">V2 資料工廠的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc099-154">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="cc099-155">-RootFolder</span></span>
<span data-ttu-id="cc099-156">用於 repo 配置的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="cc099-156">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-157">-標記</span><span class="sxs-lookup"><span data-stu-id="cc099-157">-Tag</span></span>
<span data-ttu-id="cc099-158">資料工廠的標記。</span><span class="sxs-lookup"><span data-stu-id="cc099-158">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-159">-TenantId</span><span class="sxs-lookup"><span data-stu-id="cc099-159">-TenantId</span></span>
<span data-ttu-id="cc099-160">Azure DevOps repo 配置的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc099-160">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc099-161">-確認</span><span class="sxs-lookup"><span data-stu-id="cc099-161">-Confirm</span></span>
<span data-ttu-id="cc099-162">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc099-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc099-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc099-163">-WhatIf</span></span>
<span data-ttu-id="cc099-164">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc099-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="cc099-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc099-165">CommonParameters</span></span>
<span data-ttu-id="cc099-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc099-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc099-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc099-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc099-168">輸入</span><span class="sxs-lookup"><span data-stu-id="cc099-168">INPUTS</span></span>

### <span data-ttu-id="cc099-169">System.String</span><span class="sxs-lookup"><span data-stu-id="cc099-169">System.String</span></span>

### <span data-ttu-id="cc099-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cc099-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="cc099-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cc099-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cc099-172">輸出</span><span class="sxs-lookup"><span data-stu-id="cc099-172">OUTPUTS</span></span>

### <span data-ttu-id="cc099-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cc099-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="cc099-174">筆記</span><span class="sxs-lookup"><span data-stu-id="cc099-174">NOTES</span></span>
<span data-ttu-id="cc099-175">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="cc099-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cc099-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc099-176">RELATED LINKS</span></span>

[<span data-ttu-id="cc099-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cc099-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="cc099-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cc099-178">Remove-AzDataFactoryV2</span></span>]()
