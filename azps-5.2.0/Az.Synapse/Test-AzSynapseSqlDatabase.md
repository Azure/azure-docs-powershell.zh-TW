---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280685"
---
# <span data-ttu-id="3b026-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="3b026-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="3b026-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b026-102">SYNOPSIS</span></span>
<span data-ttu-id="3b026-103">檢查是否存在 Synapse 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="3b026-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="3b026-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b026-104">SYNTAX</span></span>

### <span data-ttu-id="3b026-105">TestByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b026-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b026-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b026-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b026-107">說明</span><span class="sxs-lookup"><span data-stu-id="3b026-107">DESCRIPTION</span></span>
<span data-ttu-id="3b026-108">**Test AzSynapseSqlDatabase** Cmdlet 會檢查是否存在 SYNAPSE 分析 SQL 資料庫。</span><span class="sxs-lookup"><span data-stu-id="3b026-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="3b026-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b026-109">EXAMPLES</span></span>

### <span data-ttu-id="3b026-110">範例1</span><span class="sxs-lookup"><span data-stu-id="3b026-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="3b026-111">這個命令會檢查指定的 SQL 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="3b026-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="3b026-112">參數</span><span class="sxs-lookup"><span data-stu-id="3b026-112">PARAMETERS</span></span>

### <span data-ttu-id="3b026-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b026-113">-DefaultProfile</span></span>
<span data-ttu-id="3b026-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b026-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b026-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3b026-115">-Name</span></span>
<span data-ttu-id="3b026-116">Synapse SQL 資料庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b026-116">Name of Synapse SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b026-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b026-117">-ResourceGroupName</span></span>
<span data-ttu-id="3b026-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3b026-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b026-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3b026-119">-WorkspaceName</span></span>
<span data-ttu-id="3b026-120">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b026-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b026-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3b026-121">-WorkspaceObject</span></span>
<span data-ttu-id="3b026-122">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="3b026-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b026-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b026-123">CommonParameters</span></span>
<span data-ttu-id="3b026-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b026-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b026-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3b026-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b026-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3b026-126">INPUTS</span></span>

### <span data-ttu-id="3b026-127">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="3b026-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3b026-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3b026-128">OUTPUTS</span></span>

### <span data-ttu-id="3b026-129">System.object</span><span class="sxs-lookup"><span data-stu-id="3b026-129">System.Boolean</span></span>

## <span data-ttu-id="3b026-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3b026-130">NOTES</span></span>

## <span data-ttu-id="3b026-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b026-131">RELATED LINKS</span></span>
