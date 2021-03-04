---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: df22eb6fa435c3cf8bca4b339e460b3415991964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905722"
---
# <span data-ttu-id="e9919-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="e9919-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="e9919-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9919-102">SYNOPSIS</span></span>
<span data-ttu-id="e9919-103">在工作區中獲取筆記本相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e9919-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="e9919-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9919-104">SYNTAX</span></span>

### <span data-ttu-id="e9919-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="e9919-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9919-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="e9919-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9919-107">描述</span><span class="sxs-lookup"><span data-stu-id="e9919-107">DESCRIPTION</span></span>
<span data-ttu-id="e9919-108">**Get-AzSynapseNotebook** Cmdlet 會取得工作區中筆記本的資訊。</span><span class="sxs-lookup"><span data-stu-id="e9919-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="e9919-109">如果您指定筆記本的名稱，Cmdlet 會獲得該筆記本的資訊。</span><span class="sxs-lookup"><span data-stu-id="e9919-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="e9919-110">如果您未指定名稱，Cmdlet 會獲得工作區中所有筆記本的資訊。</span><span class="sxs-lookup"><span data-stu-id="e9919-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="e9919-111">例子</span><span class="sxs-lookup"><span data-stu-id="e9919-111">EXAMPLES</span></span>

### <span data-ttu-id="e9919-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="e9919-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="e9919-113">在工作區 ContosoWorkspace 中，獲得所有筆記本的清單。</span><span class="sxs-lookup"><span data-stu-id="e9919-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e9919-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="e9919-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="e9919-115">在工作區 ContosoWorkspace 中，獲得名為 ContosoNotebook 的單一筆記本。</span><span class="sxs-lookup"><span data-stu-id="e9919-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="e9919-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="e9919-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="e9919-117">透過管道在工作區 ContosoWorkspace 中，獲得名為 ContosoNotebook 的單一筆記本。</span><span class="sxs-lookup"><span data-stu-id="e9919-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="e9919-118">參數</span><span class="sxs-lookup"><span data-stu-id="e9919-118">PARAMETERS</span></span>

### <span data-ttu-id="e9919-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9919-119">-DefaultProfile</span></span>
<span data-ttu-id="e9919-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9919-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9919-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9919-121">-Name</span></span>
<span data-ttu-id="e9919-122">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="e9919-122">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9919-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e9919-123">-WorkspaceName</span></span>
<span data-ttu-id="e9919-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9919-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9919-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e9919-125">-WorkspaceObject</span></span>
<span data-ttu-id="e9919-126">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="e9919-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9919-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9919-127">CommonParameters</span></span>
<span data-ttu-id="e9919-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9919-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9919-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9919-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9919-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e9919-130">INPUTS</span></span>

### <span data-ttu-id="e9919-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e9919-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e9919-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e9919-132">OUTPUTS</span></span>

### <span data-ttu-id="e9919-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="e9919-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="e9919-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e9919-134">NOTES</span></span>

## <span data-ttu-id="e9919-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9919-135">RELATED LINKS</span></span>
