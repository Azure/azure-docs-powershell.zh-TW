---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288212"
---
# <span data-ttu-id="3c576-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3c576-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="3c576-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3c576-102">SYNOPSIS</span></span>
<span data-ttu-id="3c576-103">取得 Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="3c576-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3c576-104">句法</span><span class="sxs-lookup"><span data-stu-id="3c576-104">SYNTAX</span></span>

### <span data-ttu-id="3c576-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3c576-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c576-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c576-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c576-107">說明</span><span class="sxs-lookup"><span data-stu-id="3c576-107">DESCRIPTION</span></span>
<span data-ttu-id="3c576-108">**AzSynapseWorkspace** Cmdlet 會取得 Azure Synapse 分析工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c576-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="3c576-109">示例</span><span class="sxs-lookup"><span data-stu-id="3c576-109">EXAMPLES</span></span>

### <span data-ttu-id="3c576-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3c576-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="3c576-111">這個命令會在目前的訂閱下取得所有的 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="3c576-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="3c576-112">範例2</span><span class="sxs-lookup"><span data-stu-id="3c576-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="3c576-113">這個命令會在目前的訂閱下取得所有的 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="3c576-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="3c576-114">範例3</span><span class="sxs-lookup"><span data-stu-id="3c576-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="3c576-115">這個命令會取得具有指定名稱的 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="3c576-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="3c576-116">範例4</span><span class="sxs-lookup"><span data-stu-id="3c576-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="3c576-117">這個命令會取得具有指定資源識別碼的 Azure Synapse 分析工作區。</span><span class="sxs-lookup"><span data-stu-id="3c576-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="3c576-118">參數</span><span class="sxs-lookup"><span data-stu-id="3c576-118">PARAMETERS</span></span>

### <span data-ttu-id="3c576-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c576-119">-DefaultProfile</span></span>
<span data-ttu-id="3c576-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3c576-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c576-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3c576-121">-Name</span></span>
<span data-ttu-id="3c576-122">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c576-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3c576-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c576-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c576-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3c576-124">Resource group name.</span></span>

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

### <span data-ttu-id="3c576-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c576-125">-ResourceId</span></span>
<span data-ttu-id="3c576-126">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3c576-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="3c576-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c576-127">CommonParameters</span></span>
<span data-ttu-id="3c576-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3c576-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c576-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3c576-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c576-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3c576-130">INPUTS</span></span>

### <span data-ttu-id="3c576-131">所有</span><span class="sxs-lookup"><span data-stu-id="3c576-131">None</span></span>

## <span data-ttu-id="3c576-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3c576-132">OUTPUTS</span></span>

### <span data-ttu-id="3c576-133">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="3c576-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3c576-134">筆記</span><span class="sxs-lookup"><span data-stu-id="3c576-134">NOTES</span></span>

## <span data-ttu-id="3c576-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="3c576-135">RELATED LINKS</span></span>
