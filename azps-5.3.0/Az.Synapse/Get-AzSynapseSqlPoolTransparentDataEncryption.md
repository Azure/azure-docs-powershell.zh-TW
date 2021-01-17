---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288240"
---
# <span data-ttu-id="359a4-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="359a4-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="359a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="359a4-102">SYNOPSIS</span></span>
<span data-ttu-id="359a4-103">取得 SQL pool 的 TDE 狀態。</span><span class="sxs-lookup"><span data-stu-id="359a4-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="359a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="359a4-104">SYNTAX</span></span>

### <span data-ttu-id="359a4-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="359a4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="359a4-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="359a4-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="359a4-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="359a4-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="359a4-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="359a4-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="359a4-109">說明</span><span class="sxs-lookup"><span data-stu-id="359a4-109">DESCRIPTION</span></span>
<span data-ttu-id="359a4-110">**AzSynapseSqlPoolTransparentDataEncryption** Cmdlet 會取得 Azure SYNAPSE Analytics SQL pool) 的透明資料加密狀態 (TDE。</span><span class="sxs-lookup"><span data-stu-id="359a4-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="359a4-111">示例</span><span class="sxs-lookup"><span data-stu-id="359a4-111">EXAMPLES</span></span>

### <span data-ttu-id="359a4-112">範例1</span><span class="sxs-lookup"><span data-stu-id="359a4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="359a4-113">這個命令會在名為 ContosoWorkspace 的工作區下，取得名為 ContosoSqlPool 之 SQL pool 的 TDE 狀態。</span><span class="sxs-lookup"><span data-stu-id="359a4-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="359a4-114">參數</span><span class="sxs-lookup"><span data-stu-id="359a4-114">PARAMETERS</span></span>

### <span data-ttu-id="359a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="359a4-115">-DefaultProfile</span></span>
<span data-ttu-id="359a4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="359a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="359a4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="359a4-117">-InputObject</span></span>
<span data-ttu-id="359a4-118">SQL pool 輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="359a4-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="359a4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="359a4-119">-Name</span></span>
<span data-ttu-id="359a4-120">Synapse SQL pool 的名稱。</span><span class="sxs-lookup"><span data-stu-id="359a4-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="359a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="359a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="359a4-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="359a4-122">Resource group name.</span></span>

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

### <span data-ttu-id="359a4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="359a4-123">-ResourceId</span></span>
<span data-ttu-id="359a4-124">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="359a4-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="359a4-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="359a4-125">-WorkspaceName</span></span>
<span data-ttu-id="359a4-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="359a4-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="359a4-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="359a4-127">-WorkspaceObject</span></span>
<span data-ttu-id="359a4-128">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="359a4-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="359a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="359a4-129">CommonParameters</span></span>
<span data-ttu-id="359a4-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="359a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="359a4-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="359a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="359a4-132">輸入</span><span class="sxs-lookup"><span data-stu-id="359a4-132">INPUTS</span></span>

### <span data-ttu-id="359a4-133">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="359a4-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="359a4-134">PSSynapseSqlPool 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="359a4-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="359a4-135">輸出</span><span class="sxs-lookup"><span data-stu-id="359a4-135">OUTPUTS</span></span>

### <span data-ttu-id="359a4-136">PSTransparentDataEncryption 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="359a4-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="359a4-137">筆記</span><span class="sxs-lookup"><span data-stu-id="359a4-137">NOTES</span></span>

## <span data-ttu-id="359a4-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="359a4-138">RELATED LINKS</span></span>
