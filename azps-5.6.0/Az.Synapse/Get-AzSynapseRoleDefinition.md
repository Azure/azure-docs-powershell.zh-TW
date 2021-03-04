---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: 061cd16f4a2c9099be73fa2c2bdb54ff9f089949
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916458"
---
# <span data-ttu-id="f9c29-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9c29-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="f9c29-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9c29-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c29-103">獲得 Synapse Analyticss 角色定義。</span><span class="sxs-lookup"><span data-stu-id="f9c29-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="f9c29-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9c29-104">SYNTAX</span></span>

### <span data-ttu-id="f9c29-105">GetByWorkspaceNameAndIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f9c29-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9c29-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9c29-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9c29-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9c29-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9c29-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9c29-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9c29-109">描述</span><span class="sxs-lookup"><span data-stu-id="f9c29-109">DESCRIPTION</span></span>
<span data-ttu-id="f9c29-110">**Get-AzSynapseRoleDefinition** Cmdlet 會取得 Azure Synapse Analytics 角色定義。</span><span class="sxs-lookup"><span data-stu-id="f9c29-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="f9c29-111">如果您未指定角色名稱或角色識別碼，此 Cmdlet 會獲得所有角色定義。</span><span class="sxs-lookup"><span data-stu-id="f9c29-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="f9c29-112">例子</span><span class="sxs-lookup"><span data-stu-id="f9c29-112">EXAMPLES</span></span>

### <span data-ttu-id="f9c29-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="f9c29-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f9c29-114">此命令會獲得工作區下的所有角色定義。</span><span class="sxs-lookup"><span data-stu-id="f9c29-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="f9c29-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="f9c29-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="f9c29-116">此命令會獲得 Workspace ContosoWorkspace 下的角色定義，名稱為 ContosoRole。</span><span class="sxs-lookup"><span data-stu-id="f9c29-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="f9c29-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="f9c29-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="f9c29-118">此命令會透過管線在工作區下獲得所有角色定義。</span><span class="sxs-lookup"><span data-stu-id="f9c29-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="f9c29-119">參數</span><span class="sxs-lookup"><span data-stu-id="f9c29-119">PARAMETERS</span></span>

### <span data-ttu-id="f9c29-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c29-120">-DefaultProfile</span></span>
<span data-ttu-id="f9c29-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9c29-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9c29-122">-Id</span><span class="sxs-lookup"><span data-stu-id="f9c29-122">-Id</span></span>
<span data-ttu-id="f9c29-123">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9c29-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c29-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9c29-124">-Name</span></span>
<span data-ttu-id="f9c29-125">指派給主體的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c29-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c29-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f9c29-126">-WorkspaceName</span></span>
<span data-ttu-id="f9c29-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c29-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c29-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f9c29-128">-WorkspaceObject</span></span>
<span data-ttu-id="f9c29-129">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="f9c29-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c29-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c29-130">CommonParameters</span></span>
<span data-ttu-id="f9c29-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9c29-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c29-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9c29-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c29-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f9c29-133">INPUTS</span></span>

### <span data-ttu-id="f9c29-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f9c29-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f9c29-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f9c29-135">OUTPUTS</span></span>

### <span data-ttu-id="f9c29-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="f9c29-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="f9c29-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f9c29-137">NOTES</span></span>

## <span data-ttu-id="f9c29-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9c29-138">RELATED LINKS</span></span>
