---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseNotebook.md
ms.openlocfilehash: 28a4742b2e744fb41bca9402a8c48b830554e231
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435796"
---
# <span data-ttu-id="98253-101">Get-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="98253-101">Get-AzSynapseNotebook</span></span>

## <span data-ttu-id="98253-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98253-102">SYNOPSIS</span></span>
<span data-ttu-id="98253-103">取得有關工作區中筆記本的資訊。</span><span class="sxs-lookup"><span data-stu-id="98253-103">Gets information about notebooks in a workspace.</span></span>

## <span data-ttu-id="98253-104">句法</span><span class="sxs-lookup"><span data-stu-id="98253-104">SYNTAX</span></span>

### <span data-ttu-id="98253-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="98253-105">GetByName (Default)</span></span>
```
Get-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98253-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="98253-106">GetByObject</span></span>
```
Get-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98253-107">說明</span><span class="sxs-lookup"><span data-stu-id="98253-107">DESCRIPTION</span></span>
<span data-ttu-id="98253-108">**AzSynapseNotebook** Cmdlet 會取得有關工作區中筆記本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98253-108">The **Get-AzSynapseNotebook** cmdlet gets information about notebooks in a workspace.</span></span> <span data-ttu-id="98253-109">如果您指定筆記本的名稱，此 Cmdlet 會取得該筆記本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98253-109">If you specify the name of a notebook, the cmdlet gets information about that notebook.</span></span> <span data-ttu-id="98253-110">如果您沒有指定名稱，此 Cmdlet 會取得工作區中所有筆記本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="98253-110">If you do not specify a name, the cmdlet gets information about all notebooks in the workspace.</span></span>

## <span data-ttu-id="98253-111">示例</span><span class="sxs-lookup"><span data-stu-id="98253-111">EXAMPLES</span></span>

### <span data-ttu-id="98253-112">範例1</span><span class="sxs-lookup"><span data-stu-id="98253-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace | Format-Table

WorkspaceName    Properties                                         Name
-------------    ----------                                         --
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook1
ContosoWorkspace Microsoft.Azure.Commands.Synapse.Models.PSNotebook ContosoNotebook2
```

<span data-ttu-id="98253-113">取得工作區 ContosoWorkspace 中所有筆記本的清單。</span><span class="sxs-lookup"><span data-stu-id="98253-113">Gets a list of all notebooks in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="98253-114">範例2</span><span class="sxs-lookup"><span data-stu-id="98253-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
```

<span data-ttu-id="98253-115">在工作區 ContosoWorkspace 中取得稱為 ContosoNotebook 的單一筆記本。</span><span class="sxs-lookup"><span data-stu-id="98253-115">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="98253-116">範例3</span><span class="sxs-lookup"><span data-stu-id="98253-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseNotebook -Name ContosoNotebook
```

<span data-ttu-id="98253-117">透過管線在工作區 ContosoWorkspace 中取得稱為 ContosoNotebook 的單一筆記本。</span><span class="sxs-lookup"><span data-stu-id="98253-117">Gets a single notebook called ContosoNotebook in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="98253-118">參數</span><span class="sxs-lookup"><span data-stu-id="98253-118">PARAMETERS</span></span>

### <span data-ttu-id="98253-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98253-119">-DefaultProfile</span></span>
<span data-ttu-id="98253-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98253-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98253-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="98253-121">-Name</span></span>
<span data-ttu-id="98253-122">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="98253-122">The notebook name.</span></span>

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

### <span data-ttu-id="98253-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98253-123">-WorkspaceName</span></span>
<span data-ttu-id="98253-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="98253-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="98253-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="98253-125">-WorkspaceObject</span></span>
<span data-ttu-id="98253-126">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="98253-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="98253-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98253-127">CommonParameters</span></span>
<span data-ttu-id="98253-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98253-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98253-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98253-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98253-130">輸入</span><span class="sxs-lookup"><span data-stu-id="98253-130">INPUTS</span></span>

### <span data-ttu-id="98253-131">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="98253-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="98253-132">輸出</span><span class="sxs-lookup"><span data-stu-id="98253-132">OUTPUTS</span></span>

### <span data-ttu-id="98253-133">PSNotebookResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="98253-133">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="98253-134">筆記</span><span class="sxs-lookup"><span data-stu-id="98253-134">NOTES</span></span>

## <span data-ttu-id="98253-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="98253-135">RELATED LINKS</span></span>
