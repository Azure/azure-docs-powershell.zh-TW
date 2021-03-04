---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: 110d72f0a73a6a710e014a08c64cadf3b8be7d0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909389"
---
# <span data-ttu-id="efc3c-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="efc3c-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="efc3c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="efc3c-102">SYNOPSIS</span></span>
<span data-ttu-id="efc3c-103">匯出非書籍。</span><span class="sxs-lookup"><span data-stu-id="efc3c-103">Exports notbooks.</span></span>

## <span data-ttu-id="efc3c-104">語法</span><span class="sxs-lookup"><span data-stu-id="efc3c-104">SYNTAX</span></span>

### <span data-ttu-id="efc3c-105">ExportByName (預設) </span><span class="sxs-lookup"><span data-stu-id="efc3c-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efc3c-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="efc3c-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efc3c-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="efc3c-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efc3c-108">描述</span><span class="sxs-lookup"><span data-stu-id="efc3c-108">DESCRIPTION</span></span>
<span data-ttu-id="efc3c-109">**Export-AzSynapseNotebook Cmdlet** 會匯出 Azure Synapse 筆記本至 (.ipynb) 的筆記本。</span><span class="sxs-lookup"><span data-stu-id="efc3c-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="efc3c-110">筆記本的名稱會變成匯出檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="efc3c-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="efc3c-111">如果您指定筆記本的名稱，Cmdlet 會匯出該筆記本。</span><span class="sxs-lookup"><span data-stu-id="efc3c-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="efc3c-112">如果您未指定名稱，Cmdlet 會匯出工作區中所有的筆記本。</span><span class="sxs-lookup"><span data-stu-id="efc3c-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="efc3c-113">例子</span><span class="sxs-lookup"><span data-stu-id="efc3c-113">EXAMPLES</span></span>

### <span data-ttu-id="efc3c-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="efc3c-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="efc3c-115">將工作區 ContosoWorkspace 中所有的筆記本匯出至資料夾 "C：\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="efc3c-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="efc3c-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="efc3c-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="efc3c-117">將工作區 ContosoWorkspace 中名為 ContosoNotebook 的單一筆記本匯出至資料夾 "C：\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="efc3c-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="efc3c-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="efc3c-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="efc3c-119">透過管道將工作區 ContosoWorkspace 中名為 ContosoNotebook 的單一筆記本匯出至資料夾 "C：\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="efc3c-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="efc3c-120">範例 4</span><span class="sxs-lookup"><span data-stu-id="efc3c-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="efc3c-121">透過管道將工作區 ContosoWorkspace 中名為 ContosoNotebook 的單一筆記本匯出至資料夾 "C：\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="efc3c-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="efc3c-122">參數</span><span class="sxs-lookup"><span data-stu-id="efc3c-122">PARAMETERS</span></span>

### <span data-ttu-id="efc3c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efc3c-123">-AsJob</span></span>
<span data-ttu-id="efc3c-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="efc3c-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc3c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc3c-125">-DefaultProfile</span></span>
<span data-ttu-id="efc3c-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="efc3c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc3c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efc3c-127">-InputObject</span></span>
<span data-ttu-id="efc3c-128">筆記本物件。</span><span class="sxs-lookup"><span data-stu-id="efc3c-128">The notebook object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource
Parameter Sets: ExportByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efc3c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="efc3c-129">-Name</span></span>
<span data-ttu-id="efc3c-130">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="efc3c-130">The notebook name.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName, ExportByObject
Aliases: NotebookName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc3c-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="efc3c-131">-OutputFolder</span></span>
<span data-ttu-id="efc3c-132">應該放置筆記本的資料夾。</span><span class="sxs-lookup"><span data-stu-id="efc3c-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="efc3c-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="efc3c-133">-WorkspaceName</span></span>
<span data-ttu-id="efc3c-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="efc3c-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc3c-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="efc3c-135">-WorkspaceObject</span></span>
<span data-ttu-id="efc3c-136">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="efc3c-136">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ExportByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efc3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc3c-137">CommonParameters</span></span>
<span data-ttu-id="efc3c-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="efc3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc3c-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efc3c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc3c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="efc3c-140">INPUTS</span></span>

### <span data-ttu-id="efc3c-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="efc3c-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="efc3c-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span><span class="sxs-lookup"><span data-stu-id="efc3c-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="efc3c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="efc3c-143">OUTPUTS</span></span>

### <span data-ttu-id="efc3c-144">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="efc3c-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="efc3c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="efc3c-145">NOTES</span></span>

## <span data-ttu-id="efc3c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="efc3c-146">RELATED LINKS</span></span>
