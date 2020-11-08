---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 84180165e835678dc74a7ed08f6a06c51cec8134
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970782"
---
# <span data-ttu-id="37d05-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="37d05-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="37d05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37d05-102">SYNOPSIS</span></span>
<span data-ttu-id="37d05-103">更新 Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="37d05-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="37d05-104">句法</span><span class="sxs-lookup"><span data-stu-id="37d05-104">SYNTAX</span></span>

### <span data-ttu-id="37d05-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="37d05-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d05-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37d05-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d05-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37d05-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d05-108">說明</span><span class="sxs-lookup"><span data-stu-id="37d05-108">DESCRIPTION</span></span>
<span data-ttu-id="37d05-109">**AzSynapseWorkspace** Cmdlet 會更新 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="37d05-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="37d05-110">示例</span><span class="sxs-lookup"><span data-stu-id="37d05-110">EXAMPLES</span></span>

### <span data-ttu-id="37d05-111">範例1</span><span class="sxs-lookup"><span data-stu-id="37d05-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="37d05-112">這個命令會更新 specififed Azure Synapse 分析工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="37d05-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="37d05-113">範例2</span><span class="sxs-lookup"><span data-stu-id="37d05-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="37d05-114">這個命令會透過管線更新 specififed Azure Synapse 分析工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="37d05-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="37d05-115">範例3</span><span class="sxs-lookup"><span data-stu-id="37d05-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="37d05-116">這個命令會透過含資源識別碼的管線來更新 specififed Azure Synapse 分析工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="37d05-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="37d05-117">參數</span><span class="sxs-lookup"><span data-stu-id="37d05-117">PARAMETERS</span></span>

### <span data-ttu-id="37d05-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37d05-118">-AsJob</span></span>
<span data-ttu-id="37d05-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="37d05-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37d05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d05-120">-DefaultProfile</span></span>
<span data-ttu-id="37d05-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37d05-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37d05-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37d05-122">-InputObject</span></span>
<span data-ttu-id="37d05-123">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="37d05-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37d05-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="37d05-124">-Name</span></span>
<span data-ttu-id="37d05-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="37d05-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d05-126">-ResourceGroupName</span></span>
<span data-ttu-id="37d05-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="37d05-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d05-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37d05-128">-ResourceId</span></span>
<span data-ttu-id="37d05-129">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="37d05-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d05-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="37d05-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="37d05-131">工作區的新 SQL 系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="37d05-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d05-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="37d05-132">-Tag</span></span>
<span data-ttu-id="37d05-133">與資源相關聯之標記的字串字典。</span><span class="sxs-lookup"><span data-stu-id="37d05-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d05-134">-確認</span><span class="sxs-lookup"><span data-stu-id="37d05-134">-Confirm</span></span>
<span data-ttu-id="37d05-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="37d05-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37d05-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d05-136">-WhatIf</span></span>
<span data-ttu-id="37d05-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="37d05-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d05-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="37d05-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37d05-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d05-139">CommonParameters</span></span>
<span data-ttu-id="37d05-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37d05-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d05-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37d05-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d05-142">輸入</span><span class="sxs-lookup"><span data-stu-id="37d05-142">INPUTS</span></span>

### <span data-ttu-id="37d05-143">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="37d05-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="37d05-144">輸出</span><span class="sxs-lookup"><span data-stu-id="37d05-144">OUTPUTS</span></span>

### <span data-ttu-id="37d05-145">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="37d05-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="37d05-146">筆記</span><span class="sxs-lookup"><span data-stu-id="37d05-146">NOTES</span></span>

## <span data-ttu-id="37d05-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="37d05-147">RELATED LINKS</span></span>