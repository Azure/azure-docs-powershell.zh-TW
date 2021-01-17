---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseFirewallRule.md
ms.openlocfilehash: 22a7bb4c135a4424aa27a76f9e13ba14f21ca572
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288324"
---
# <span data-ttu-id="be734-101">Get-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="be734-101">Get-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="be734-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be734-102">SYNOPSIS</span></span>
<span data-ttu-id="be734-103">取得 Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="be734-103">Gets a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="be734-104">句法</span><span class="sxs-lookup"><span data-stu-id="be734-104">SYNTAX</span></span>

### <span data-ttu-id="be734-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="be734-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be734-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be734-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseFirewallRule -WorkSpaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be734-107">說明</span><span class="sxs-lookup"><span data-stu-id="be734-107">DESCRIPTION</span></span>
<span data-ttu-id="be734-108">**AzSynapseFirewallRule** Cmdlet 會取得 Azure Synapse 分析防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="be734-108">The **Get-AzSynapseFirewallRule** cmdlet gets a Azure Synapse Analytics Firewall Rule.</span></span>
<span data-ttu-id="be734-109">如果您沒有指定規則名稱，此 Cmdlet 會取得所有規則。</span><span class="sxs-lookup"><span data-stu-id="be734-109">If you do not specify a rule name, this cmdlet gets all rules.</span></span>

## <span data-ttu-id="be734-110">示例</span><span class="sxs-lookup"><span data-stu-id="be734-110">EXAMPLES</span></span>

### <span data-ttu-id="be734-111">範例1</span><span class="sxs-lookup"><span data-stu-id="be734-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="be734-112">這個命令會取得工作區底下的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="be734-112">This command gets all firewall rules under a workspace.</span></span>

### <span data-ttu-id="be734-113">範例2</span><span class="sxs-lookup"><span data-stu-id="be734-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="be734-114">這個命令會在 [工作區 ContosoWorkspace] 下以 [名稱 ContosoFirewallRule] 來取得防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="be734-114">This command gets the firewall rule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="be734-115">範例3</span><span class="sxs-lookup"><span data-stu-id="be734-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseFirewallRule
```

<span data-ttu-id="be734-116">這個命令會透過流水線取得工作區底下的所有防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="be734-116">This command gets all firewall rules under a workspace through pipeline.</span></span>

## <span data-ttu-id="be734-117">參數</span><span class="sxs-lookup"><span data-stu-id="be734-117">PARAMETERS</span></span>

### <span data-ttu-id="be734-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be734-118">-DefaultProfile</span></span>
<span data-ttu-id="be734-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be734-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be734-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="be734-120">-Name</span></span>
<span data-ttu-id="be734-121">工作區的 firerwall 規則名稱。</span><span class="sxs-lookup"><span data-stu-id="be734-121">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be734-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be734-122">-ResourceGroupName</span></span>
<span data-ttu-id="be734-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="be734-123">Resource group name.</span></span>

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

### <span data-ttu-id="be734-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="be734-124">-WorkspaceName</span></span>
<span data-ttu-id="be734-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="be734-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be734-126">-WorkSpaceObject</span><span class="sxs-lookup"><span data-stu-id="be734-126">-WorkSpaceObject</span></span>
<span data-ttu-id="be734-127">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="be734-127">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be734-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be734-128">CommonParameters</span></span>
<span data-ttu-id="be734-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be734-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be734-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="be734-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be734-131">輸入</span><span class="sxs-lookup"><span data-stu-id="be734-131">INPUTS</span></span>

### <span data-ttu-id="be734-132">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="be734-132">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="be734-133">輸出</span><span class="sxs-lookup"><span data-stu-id="be734-133">OUTPUTS</span></span>

### <span data-ttu-id="be734-134">PSSynapseIpFirewallRule 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="be734-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="be734-135">筆記</span><span class="sxs-lookup"><span data-stu-id="be734-135">NOTES</span></span>

## <span data-ttu-id="be734-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="be734-136">RELATED LINKS</span></span>
