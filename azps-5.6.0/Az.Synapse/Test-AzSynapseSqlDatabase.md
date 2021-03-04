---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e797cba0c05b6dbaee11d540b9efc3aca7e7efcf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916833"
---
# <span data-ttu-id="46703-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="46703-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="46703-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46703-102">SYNOPSIS</span></span>
<span data-ttu-id="46703-103">檢查 Synapse Analytics SQL 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="46703-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="46703-104">語法</span><span class="sxs-lookup"><span data-stu-id="46703-104">SYNTAX</span></span>

### <span data-ttu-id="46703-105">TestByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="46703-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46703-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46703-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46703-107">描述</span><span class="sxs-lookup"><span data-stu-id="46703-107">DESCRIPTION</span></span>
<span data-ttu-id="46703-108">**Test-AzSynapseSqlDatabase** Cmdlet 會檢查 Synapse Analytics SQL 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="46703-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="46703-109">例子</span><span class="sxs-lookup"><span data-stu-id="46703-109">EXAMPLES</span></span>

### <span data-ttu-id="46703-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="46703-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="46703-111">此命令會檢查指定的 SQL 資料庫是否存在。</span><span class="sxs-lookup"><span data-stu-id="46703-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="46703-112">參數</span><span class="sxs-lookup"><span data-stu-id="46703-112">PARAMETERS</span></span>

### <span data-ttu-id="46703-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46703-113">-DefaultProfile</span></span>
<span data-ttu-id="46703-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="46703-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46703-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="46703-115">-Name</span></span>
<span data-ttu-id="46703-116">Synapse SQL Database 的名稱。</span><span class="sxs-lookup"><span data-stu-id="46703-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="46703-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46703-117">-ResourceGroupName</span></span>
<span data-ttu-id="46703-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="46703-118">Resource group name.</span></span>

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

### <span data-ttu-id="46703-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="46703-119">-WorkspaceName</span></span>
<span data-ttu-id="46703-120">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="46703-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="46703-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="46703-121">-WorkspaceObject</span></span>
<span data-ttu-id="46703-122">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="46703-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="46703-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46703-123">CommonParameters</span></span>
<span data-ttu-id="46703-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46703-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46703-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46703-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46703-126">輸入</span><span class="sxs-lookup"><span data-stu-id="46703-126">INPUTS</span></span>

### <span data-ttu-id="46703-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="46703-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="46703-128">輸出</span><span class="sxs-lookup"><span data-stu-id="46703-128">OUTPUTS</span></span>

### <span data-ttu-id="46703-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46703-129">System.Boolean</span></span>

## <span data-ttu-id="46703-130">筆記</span><span class="sxs-lookup"><span data-stu-id="46703-130">NOTES</span></span>

## <span data-ttu-id="46703-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="46703-131">RELATED LINKS</span></span>
