---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: 25107456afbf85aa41dd0be600a20f7a5fcbb640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906449"
---
# <span data-ttu-id="0e4c2-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e4c2-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="0e4c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4c2-103">獲得 Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0e4c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e4c2-104">SYNTAX</span></span>

### <span data-ttu-id="0e4c2-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0e4c2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e4c2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e4c2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e4c2-107">描述</span><span class="sxs-lookup"><span data-stu-id="0e4c2-107">DESCRIPTION</span></span>
<span data-ttu-id="0e4c2-108">**Get-AzSynapseWorkspace** Cmdlet 會取得 Azure Synapse Analytics 工作區相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="0e4c2-109">例子</span><span class="sxs-lookup"><span data-stu-id="0e4c2-109">EXAMPLES</span></span>

### <span data-ttu-id="0e4c2-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="0e4c2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="0e4c2-111">此命令會獲得目前訂閱下的所有 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="0e4c2-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="0e4c2-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="0e4c2-113">此命令會獲得目前訂閱下的所有 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="0e4c2-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="0e4c2-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="0e4c2-115">此命令會以指定的名稱獲得 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="0e4c2-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="0e4c2-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="0e4c2-117">此命令會獲得具有指定資源識別碼的 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="0e4c2-118">參數</span><span class="sxs-lookup"><span data-stu-id="0e4c2-118">PARAMETERS</span></span>

### <span data-ttu-id="0e4c2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4c2-119">-DefaultProfile</span></span>
<span data-ttu-id="0e4c2-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e4c2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e4c2-121">-Name</span></span>
<span data-ttu-id="0e4c2-122">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4c2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e4c2-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e4c2-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4c2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e4c2-125">-ResourceId</span></span>
<span data-ttu-id="0e4c2-126">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e4c2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4c2-127">CommonParameters</span></span>
<span data-ttu-id="0e4c2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e4c2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4c2-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e4c2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4c2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0e4c2-130">INPUTS</span></span>

### <span data-ttu-id="0e4c2-131">沒有</span><span class="sxs-lookup"><span data-stu-id="0e4c2-131">None</span></span>

## <span data-ttu-id="0e4c2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0e4c2-132">OUTPUTS</span></span>

### <span data-ttu-id="0e4c2-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e4c2-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0e4c2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0e4c2-134">NOTES</span></span>

## <span data-ttu-id="0e4c2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e4c2-135">RELATED LINKS</span></span>
