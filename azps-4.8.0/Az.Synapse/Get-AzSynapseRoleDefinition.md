---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126668"
---
# <span data-ttu-id="b4972-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b4972-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="b4972-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4972-102">SYNOPSIS</span></span>
<span data-ttu-id="b4972-103">取得 Synapse 分析角色定義。</span><span class="sxs-lookup"><span data-stu-id="b4972-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="b4972-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4972-104">SYNTAX</span></span>

### <span data-ttu-id="b4972-105">GetByWorkspaceNameAndIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b4972-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4972-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4972-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4972-107">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4972-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4972-108">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4972-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4972-109">說明</span><span class="sxs-lookup"><span data-stu-id="b4972-109">DESCRIPTION</span></span>
<span data-ttu-id="b4972-110">**AzSynapseRoleDefinition** Cmdlet 會取得 Azure Synapse Analytics 角色定義。</span><span class="sxs-lookup"><span data-stu-id="b4972-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="b4972-111">如果您沒有指定角色名稱或角色識別碼，此 Cmdlet 會取得所有角色定義。</span><span class="sxs-lookup"><span data-stu-id="b4972-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="b4972-112">示例</span><span class="sxs-lookup"><span data-stu-id="b4972-112">EXAMPLES</span></span>

### <span data-ttu-id="b4972-113">範例1</span><span class="sxs-lookup"><span data-stu-id="b4972-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="b4972-114">這個命令會在工作區中取得所有角色定義。</span><span class="sxs-lookup"><span data-stu-id="b4972-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="b4972-115">範例2</span><span class="sxs-lookup"><span data-stu-id="b4972-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="b4972-116">這個命令會在 [工作區 ContosoWorkspace] 下取得名稱為 ContosoRole 的角色定義。</span><span class="sxs-lookup"><span data-stu-id="b4972-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="b4972-117">範例3</span><span class="sxs-lookup"><span data-stu-id="b4972-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="b4972-118">這個命令會透過管線在工作區下取得所有角色定義。</span><span class="sxs-lookup"><span data-stu-id="b4972-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="b4972-119">參數</span><span class="sxs-lookup"><span data-stu-id="b4972-119">PARAMETERS</span></span>

### <span data-ttu-id="b4972-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4972-120">-DefaultProfile</span></span>
<span data-ttu-id="b4972-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4972-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4972-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b4972-122">-Id</span></span>
<span data-ttu-id="b4972-123">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4972-123">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="b4972-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4972-124">-Name</span></span>
<span data-ttu-id="b4972-125">指派給主體的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="b4972-125">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="b4972-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b4972-126">-WorkspaceName</span></span>
<span data-ttu-id="b4972-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4972-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b4972-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b4972-128">-WorkspaceObject</span></span>
<span data-ttu-id="b4972-129">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="b4972-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b4972-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4972-130">CommonParameters</span></span>
<span data-ttu-id="b4972-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4972-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4972-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b4972-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4972-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b4972-133">INPUTS</span></span>

### <span data-ttu-id="b4972-134">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b4972-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b4972-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b4972-135">OUTPUTS</span></span>

### <span data-ttu-id="b4972-136">PSSynapseRole 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="b4972-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="b4972-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b4972-137">NOTES</span></span>

## <span data-ttu-id="b4972-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4972-138">RELATED LINKS</span></span>
