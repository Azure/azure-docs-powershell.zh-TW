---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612914"
---
# <span data-ttu-id="0b215-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b215-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="0b215-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b215-102">SYNOPSIS</span></span>
<span data-ttu-id="0b215-103">建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="0b215-103">Creates a data factory.</span></span>

## <span data-ttu-id="0b215-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b215-104">SYNTAX</span></span>

### <span data-ttu-id="0b215-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="0b215-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b215-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0b215-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b215-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="0b215-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b215-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="0b215-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b215-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="0b215-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b215-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="0b215-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b215-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0b215-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b215-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="0b215-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b215-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="0b215-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b215-114">說明</span><span class="sxs-lookup"><span data-stu-id="0b215-114">DESCRIPTION</span></span>
<span data-ttu-id="0b215-115">**AzDataFactoryV2** Cmdlet 會建立具有指定資源群組名稱和位置的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="0b215-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="0b215-116">依下列循序執行這些作業：--建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="0b215-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="0b215-117">--建立連結的服務。</span><span class="sxs-lookup"><span data-stu-id="0b215-117">-- Create linked services.</span></span>
<span data-ttu-id="0b215-118">--建立資料集。</span><span class="sxs-lookup"><span data-stu-id="0b215-118">-- Create datasets.</span></span>
<span data-ttu-id="0b215-119">--建立管線。</span><span class="sxs-lookup"><span data-stu-id="0b215-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="0b215-120">示例</span><span class="sxs-lookup"><span data-stu-id="0b215-120">EXAMPLES</span></span>

### <span data-ttu-id="0b215-121">範例1：建立資料工廠</span><span class="sxs-lookup"><span data-stu-id="0b215-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="0b215-122">範例2：使用現有的工廠物件來建立含 repoconfiguration 詳細資料的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="0b215-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="0b215-123">這個命令會在 WestUS 位置中，在名為 [ADF] 的資源群組中，建立名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="0b215-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="0b215-124">參數</span><span class="sxs-lookup"><span data-stu-id="0b215-124">PARAMETERS</span></span>

### <span data-ttu-id="0b215-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0b215-125">-AccountName</span></span>
<span data-ttu-id="0b215-126">存放庫配置的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0b215-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="0b215-127">-CollaborationBranch</span></span>
<span data-ttu-id="0b215-128">存放庫配置的共同作業分支。</span><span class="sxs-lookup"><span data-stu-id="0b215-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b215-129">-DefaultProfile</span></span>
<span data-ttu-id="0b215-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b215-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b215-131">-Force</span><span class="sxs-lookup"><span data-stu-id="0b215-131">-Force</span></span>
<span data-ttu-id="0b215-132">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b215-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0b215-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="0b215-133">-HostName</span></span>
<span data-ttu-id="0b215-134">存放庫配置的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="0b215-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b215-135">-InputObject</span></span>
<span data-ttu-id="0b215-136">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="0b215-136">The data factory object.</span></span>

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

### <span data-ttu-id="0b215-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="0b215-137">-LastCommitId</span></span>
<span data-ttu-id="0b215-138">[存放庫] 設定的最後一個 commit id。</span><span class="sxs-lookup"><span data-stu-id="0b215-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-139">-位置</span><span class="sxs-lookup"><span data-stu-id="0b215-139">-Location</span></span>
<span data-ttu-id="0b215-140">此區域會建立資料工廠。</span><span class="sxs-lookup"><span data-stu-id="0b215-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="0b215-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b215-141">-Name</span></span>
<span data-ttu-id="0b215-142">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="0b215-142">The data factory name.</span></span>

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

### <span data-ttu-id="0b215-143">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="0b215-143">-ProjectName</span></span>
<span data-ttu-id="0b215-144">存放庫配置的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="0b215-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-145">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="0b215-145">-RepositoryName</span></span>
<span data-ttu-id="0b215-146">存放庫配置的儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0b215-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b215-147">-ResourceGroupName</span></span>
<span data-ttu-id="0b215-148">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b215-148">The resource group name.</span></span>

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

### <span data-ttu-id="0b215-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b215-149">-ResourceId</span></span>
<span data-ttu-id="0b215-150">V2 資料工廠的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b215-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="0b215-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="0b215-151">-RootFolder</span></span>
<span data-ttu-id="0b215-152">存放庫配置的根資料夾。</span><span class="sxs-lookup"><span data-stu-id="0b215-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b215-153">-Tag</span></span>
<span data-ttu-id="0b215-154">資料工廠的標籤。</span><span class="sxs-lookup"><span data-stu-id="0b215-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="0b215-155">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0b215-155">-TenantId</span></span>
<span data-ttu-id="0b215-156">存放庫配置的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b215-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="0b215-157">-確認</span><span class="sxs-lookup"><span data-stu-id="0b215-157">-Confirm</span></span>
<span data-ttu-id="0b215-158">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b215-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b215-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b215-159">-WhatIf</span></span>
<span data-ttu-id="0b215-160">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b215-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0b215-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b215-161">CommonParameters</span></span>
<span data-ttu-id="0b215-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b215-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b215-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b215-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b215-164">輸入</span><span class="sxs-lookup"><span data-stu-id="0b215-164">INPUTS</span></span>

### <span data-ttu-id="0b215-165">System.object</span><span class="sxs-lookup"><span data-stu-id="0b215-165">System.String</span></span>

### <span data-ttu-id="0b215-166">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b215-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b215-167">輸出</span><span class="sxs-lookup"><span data-stu-id="0b215-167">OUTPUTS</span></span>

### <span data-ttu-id="0b215-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0b215-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0b215-169">筆記</span><span class="sxs-lookup"><span data-stu-id="0b215-169">NOTES</span></span>
<span data-ttu-id="0b215-170">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="0b215-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0b215-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b215-171">RELATED LINKS</span></span>

[<span data-ttu-id="0b215-172">AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b215-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="0b215-173">移除-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0b215-173">Remove-AzDataFactoryV2</span></span>]()
