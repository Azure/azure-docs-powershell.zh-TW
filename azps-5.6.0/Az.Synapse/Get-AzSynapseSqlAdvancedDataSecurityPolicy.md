---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 47800968fec9a12255bae01499618f9928416648
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917850"
---
# <span data-ttu-id="c99a1-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="c99a1-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="c99a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c99a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c99a1-103">獲得工作區的進位資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="c99a1-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="c99a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="c99a1-104">SYNTAX</span></span>

### <span data-ttu-id="c99a1-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c99a1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99a1-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99a1-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c99a1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c99a1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c99a1-108">描述</span><span class="sxs-lookup"><span data-stu-id="c99a1-108">DESCRIPTION</span></span>
<span data-ttu-id="c99a1-109">**Get-AzSynapseSqlAdvancedDataSecurityPolicy** Cmdlet 會取得工作區的進位資料安全性原則。</span><span class="sxs-lookup"><span data-stu-id="c99a1-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="c99a1-110">例子</span><span class="sxs-lookup"><span data-stu-id="c99a1-110">EXAMPLES</span></span>

### <span data-ttu-id="c99a1-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c99a1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="c99a1-112">此命令在名為 ContosoWorkspace 的工作區上獲得進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="c99a1-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c99a1-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="c99a1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="c99a1-114">此命令會透過管道在名為 ContosoWorkspace 的工作區中，獲得進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="c99a1-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c99a1-115">參數</span><span class="sxs-lookup"><span data-stu-id="c99a1-115">PARAMETERS</span></span>

### <span data-ttu-id="c99a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c99a1-116">-DefaultProfile</span></span>
<span data-ttu-id="c99a1-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c99a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c99a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c99a1-118">-InputObject</span></span>
<span data-ttu-id="c99a1-119">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="c99a1-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c99a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c99a1-120">-ResourceGroupName</span></span>
<span data-ttu-id="c99a1-121">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c99a1-121">Resource group name.</span></span>

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

### <span data-ttu-id="c99a1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c99a1-122">-ResourceId</span></span>
<span data-ttu-id="c99a1-123">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c99a1-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="c99a1-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c99a1-124">-WorkspaceName</span></span>
<span data-ttu-id="c99a1-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c99a1-125">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c99a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c99a1-126">CommonParameters</span></span>
<span data-ttu-id="c99a1-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c99a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c99a1-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c99a1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c99a1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="c99a1-129">INPUTS</span></span>

### <span data-ttu-id="c99a1-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c99a1-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c99a1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="c99a1-131">OUTPUTS</span></span>

### <span data-ttu-id="c99a1-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="c99a1-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="c99a1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="c99a1-133">NOTES</span></span>

## <span data-ttu-id="c99a1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="c99a1-134">RELATED LINKS</span></span>
