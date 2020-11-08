---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128258"
---
# <span data-ttu-id="e8e28-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8e28-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="e8e28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8e28-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e28-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-103">Creates a data factory.</span></span>

## <span data-ttu-id="e8e28-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8e28-104">SYNTAX</span></span>

### <span data-ttu-id="e8e28-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="e8e28-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e28-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e28-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e28-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e8e28-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e28-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e8e28-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e28-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e8e28-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8e28-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e8e28-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e28-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8e28-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e28-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="e8e28-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8e28-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="e8e28-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8e28-114">說明</span><span class="sxs-lookup"><span data-stu-id="e8e28-114">DESCRIPTION</span></span>
<span data-ttu-id="e8e28-115">**AzDataFactoryV2** Cmdlet 會建立具有指定資源群組名稱和位置的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="e8e28-116">依下列循序執行這些作業：--建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="e8e28-117">--建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="e8e28-117">-- Create linked services.</span></span>
<span data-ttu-id="e8e28-118">--建立資料集。</span><span class="sxs-lookup"><span data-stu-id="e8e28-118">-- Create datasets.</span></span>
<span data-ttu-id="e8e28-119">--建立管線。</span><span class="sxs-lookup"><span data-stu-id="e8e28-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="e8e28-120">示例</span><span class="sxs-lookup"><span data-stu-id="e8e28-120">EXAMPLES</span></span>

### <span data-ttu-id="e8e28-121">範例1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="e8e28-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="e8e28-122">範例2：使用現有的工廠物件，建立含存放庫配置詳細資料的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="e8e28-123">這個命令會在 EastUS 位置的資源群組中，使用 Azure DevOps 來源控制設定來建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="e8e28-124">範例3：使用新的工廠物件建立含 GitHub 存放庫配置詳細資料的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="e8e28-125">這個命令會在使用 GitHub 來源控制設定的 EastUS 位置中，在名為 [ADF] 的資源群組中建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="e8e28-126">參數</span><span class="sxs-lookup"><span data-stu-id="e8e28-126">PARAMETERS</span></span>

### <span data-ttu-id="e8e28-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e8e28-127">-AccountName</span></span>
<span data-ttu-id="e8e28-128">存放庫配置的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e28-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="e8e28-129">-CollaborationBranch</span></span>
<span data-ttu-id="e8e28-130">存放庫配置的共同作業分支。</span><span class="sxs-lookup"><span data-stu-id="e8e28-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e28-131">-DefaultProfile</span></span>
<span data-ttu-id="e8e28-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8e28-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8e28-133">-Force</span><span class="sxs-lookup"><span data-stu-id="e8e28-133">-Force</span></span>
<span data-ttu-id="e8e28-134">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8e28-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e8e28-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="e8e28-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="e8e28-136">包含資料工廠之全域參數的字典。</span><span class="sxs-lookup"><span data-stu-id="e8e28-136">The dictionary containing the global parameters of the data factory.</span></span>

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

### <span data-ttu-id="e8e28-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="e8e28-137">-HostName</span></span>
<span data-ttu-id="e8e28-138">GitHub 存放庫配置的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e28-138">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8e28-139">-InputObject</span></span>
<span data-ttu-id="e8e28-140">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="e8e28-140">The data factory object.</span></span>

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

### <span data-ttu-id="e8e28-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="e8e28-141">-LastCommitId</span></span>
<span data-ttu-id="e8e28-142">[存放庫] 設定的最後一個 commit id。</span><span class="sxs-lookup"><span data-stu-id="e8e28-142">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-143">-位置</span><span class="sxs-lookup"><span data-stu-id="e8e28-143">-Location</span></span>
<span data-ttu-id="e8e28-144">此區域會建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="e8e28-144">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="e8e28-145">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8e28-145">-Name</span></span>
<span data-ttu-id="e8e28-146">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e28-146">The data factory name.</span></span>

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

### <span data-ttu-id="e8e28-147">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="e8e28-147">-ProjectName</span></span>
<span data-ttu-id="e8e28-148">用於存放庫設定的 Microsoft project name Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="e8e28-148">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="e8e28-149">-RepositoryName</span></span>
<span data-ttu-id="e8e28-150">存放庫配置的儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e28-150">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e28-151">-ResourceGroupName</span></span>
<span data-ttu-id="e8e28-152">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8e28-152">The resource group name.</span></span>

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

### <span data-ttu-id="e8e28-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e28-153">-ResourceId</span></span>
<span data-ttu-id="e8e28-154">V2 資料工廠的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8e28-154">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="e8e28-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="e8e28-155">-RootFolder</span></span>
<span data-ttu-id="e8e28-156">存放庫配置的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="e8e28-156">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8e28-157">-Tag</span></span>
<span data-ttu-id="e8e28-158">資料工廠的標籤。</span><span class="sxs-lookup"><span data-stu-id="e8e28-158">The tags of the data factory.</span></span>

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

### <span data-ttu-id="e8e28-159">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e8e28-159">-TenantId</span></span>
<span data-ttu-id="e8e28-160">Azure DevOps 存放庫配置的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8e28-160">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="e8e28-161">-確認</span><span class="sxs-lookup"><span data-stu-id="e8e28-161">-Confirm</span></span>
<span data-ttu-id="e8e28-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8e28-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8e28-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8e28-163">-WhatIf</span></span>
<span data-ttu-id="e8e28-164">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8e28-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e8e28-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e28-165">CommonParameters</span></span>
<span data-ttu-id="e8e28-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8e28-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e28-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8e28-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e28-168">輸入</span><span class="sxs-lookup"><span data-stu-id="e8e28-168">INPUTS</span></span>

### <span data-ttu-id="e8e28-169">System.object</span><span class="sxs-lookup"><span data-stu-id="e8e28-169">System.String</span></span>

### <span data-ttu-id="e8e28-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8e28-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="e8e28-171">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8e28-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e8e28-172">輸出</span><span class="sxs-lookup"><span data-stu-id="e8e28-172">OUTPUTS</span></span>

### <span data-ttu-id="e8e28-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e8e28-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="e8e28-174">筆記</span><span class="sxs-lookup"><span data-stu-id="e8e28-174">NOTES</span></span>
<span data-ttu-id="e8e28-175">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="e8e28-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e8e28-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8e28-176">RELATED LINKS</span></span>

[<span data-ttu-id="e8e28-177">AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8e28-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="e8e28-178">移除-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e8e28-178">Remove-AzDataFactoryV2</span></span>]()
