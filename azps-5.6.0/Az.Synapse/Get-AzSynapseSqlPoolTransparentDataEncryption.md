---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cee34e8437048f0cc59df3463b0b7f3cf2de6ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910334"
---
# <span data-ttu-id="70c61-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="70c61-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="70c61-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70c61-102">SYNOPSIS</span></span>
<span data-ttu-id="70c61-103">獲得 SQL 資料庫的 TDE 狀態。</span><span class="sxs-lookup"><span data-stu-id="70c61-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="70c61-104">語法</span><span class="sxs-lookup"><span data-stu-id="70c61-104">SYNTAX</span></span>

### <span data-ttu-id="70c61-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="70c61-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70c61-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70c61-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70c61-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70c61-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="70c61-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70c61-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70c61-109">描述</span><span class="sxs-lookup"><span data-stu-id="70c61-109">DESCRIPTION</span></span>
<span data-ttu-id="70c61-110">**Get-AzSynapseSqlPoolTransparentDataEncryption** Cmdlet 取得 Azure Synapse Analytics SQL 資料庫的透明資料加密 (TDE) 狀態。</span><span class="sxs-lookup"><span data-stu-id="70c61-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="70c61-111">例子</span><span class="sxs-lookup"><span data-stu-id="70c61-111">EXAMPLES</span></span>

### <span data-ttu-id="70c61-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="70c61-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="70c61-113">此命令會針對名為 ContosoWorkspace 的工作區下名為 ContosoSqlPool 的 SQL 資料庫，獲得 TDE 的狀態。</span><span class="sxs-lookup"><span data-stu-id="70c61-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="70c61-114">參數</span><span class="sxs-lookup"><span data-stu-id="70c61-114">PARAMETERS</span></span>

### <span data-ttu-id="70c61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c61-115">-DefaultProfile</span></span>
<span data-ttu-id="70c61-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="70c61-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c61-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70c61-117">-InputObject</span></span>
<span data-ttu-id="70c61-118">SQL 資料庫輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="70c61-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="70c61-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="70c61-119">-Name</span></span>
<span data-ttu-id="70c61-120">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c61-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="70c61-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c61-121">-ResourceGroupName</span></span>
<span data-ttu-id="70c61-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="70c61-122">Resource group name.</span></span>

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

### <span data-ttu-id="70c61-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70c61-123">-ResourceId</span></span>
<span data-ttu-id="70c61-124">Synapse SQL Pool 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="70c61-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="70c61-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="70c61-125">-WorkspaceName</span></span>
<span data-ttu-id="70c61-126">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="70c61-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="70c61-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="70c61-127">-WorkspaceObject</span></span>
<span data-ttu-id="70c61-128">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="70c61-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="70c61-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c61-129">CommonParameters</span></span>
<span data-ttu-id="70c61-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70c61-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c61-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70c61-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c61-132">輸入</span><span class="sxs-lookup"><span data-stu-id="70c61-132">INPUTS</span></span>

### <span data-ttu-id="70c61-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="70c61-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="70c61-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="70c61-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="70c61-135">輸出</span><span class="sxs-lookup"><span data-stu-id="70c61-135">OUTPUTS</span></span>

### <span data-ttu-id="70c61-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="70c61-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="70c61-137">筆記</span><span class="sxs-lookup"><span data-stu-id="70c61-137">NOTES</span></span>

## <span data-ttu-id="70c61-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="70c61-138">RELATED LINKS</span></span>
