---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/export-azsynapsenotebook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Export-AzSynapseNotebook.md
ms.openlocfilehash: d61038add8ded9f697bfef551e00aec24c8aaf3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137610"
---
# <span data-ttu-id="6acad-101">Export-AzSynapseNotebook</span><span class="sxs-lookup"><span data-stu-id="6acad-101">Export-AzSynapseNotebook</span></span>

## <span data-ttu-id="6acad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6acad-102">SYNOPSIS</span></span>
<span data-ttu-id="6acad-103">匯出 notbooks。</span><span class="sxs-lookup"><span data-stu-id="6acad-103">Exports notbooks.</span></span>

## <span data-ttu-id="6acad-104">句法</span><span class="sxs-lookup"><span data-stu-id="6acad-104">SYNTAX</span></span>

### <span data-ttu-id="6acad-105">ExportByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6acad-105">ExportByName (Default)</span></span>
```
Export-AzSynapseNotebook -WorkspaceName <String> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6acad-106">ExportByObject</span><span class="sxs-lookup"><span data-stu-id="6acad-106">ExportByObject</span></span>
```
Export-AzSynapseNotebook -WorkspaceObject <PSSynapseWorkspace> [-Name <String>] -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6acad-107">ExportByInputObject</span><span class="sxs-lookup"><span data-stu-id="6acad-107">ExportByInputObject</span></span>
```
Export-AzSynapseNotebook -InputObject <PSNotebookResource> -OutputFolder <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6acad-108">說明</span><span class="sxs-lookup"><span data-stu-id="6acad-108">DESCRIPTION</span></span>
<span data-ttu-id="6acad-109">**Export AzSynapseNotebook** Cmdlet 會將 Azure Synapse 筆記本匯出至筆記本 ( ipynb) 檔案。</span><span class="sxs-lookup"><span data-stu-id="6acad-109">The **Export-AzSynapseNotebook** cmdlet exports an Azure Synapse notebook to a notebook (.ipynb) file.</span></span> <span data-ttu-id="6acad-110">筆記本的名稱會變成匯出檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6acad-110">The name of the notebook becomes the name of the exported file.</span></span> <span data-ttu-id="6acad-111">如果您指定筆記本的名稱，Cmdlet 會匯出該筆記本。</span><span class="sxs-lookup"><span data-stu-id="6acad-111">If you specify the name of a notebook, the cmdlet exports that notebook.</span></span> <span data-ttu-id="6acad-112">如果您沒有指定名稱，此 Cmdlet 會匯出工作區中的所有筆記本。</span><span class="sxs-lookup"><span data-stu-id="6acad-112">If you do not specify a name, the cmdlet export all notebooks in the workspace.</span></span>

## <span data-ttu-id="6acad-113">示例</span><span class="sxs-lookup"><span data-stu-id="6acad-113">EXAMPLES</span></span>

### <span data-ttu-id="6acad-114">範例1</span><span class="sxs-lookup"><span data-stu-id="6acad-114">Example 1</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6acad-115">將工作區 ContosoWorkspace 中的所有筆記本匯出至資料夾 "C:\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="6acad-115">Exports all notebooks in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="6acad-116">範例2</span><span class="sxs-lookup"><span data-stu-id="6acad-116">Example 2</span></span>
```powershell
PS C:\> Export-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6acad-117">將工作區 ContosoWorkspace 中稱為 ContosoNotebook 的單一筆記本匯出至資料夾 "C:\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="6acad-117">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook".</span></span>

### <span data-ttu-id="6acad-118">範例3</span><span class="sxs-lookup"><span data-stu-id="6acad-118">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Export-AzSynapseNotebook -Name ContosoNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6acad-119">在工作區 ContosoWorkspace 中，將稱為 ContosoNotebook 的單一筆記本匯出至透過管線的資料夾 "C:\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="6acad-119">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

### <span data-ttu-id="6acad-120">範例4</span><span class="sxs-lookup"><span data-stu-id="6acad-120">Example 4</span></span>
```powershell
PS C:\> $notebook = Get-AzSynapseNotebook -WorkspaceName ContosoWorkspace -Name ContosoNotebook
PS C:\> $notebook | Export-AzSynapseNotebook -OutputFolder "C:\Notebook"
```

<span data-ttu-id="6acad-121">在工作區 ContosoWorkspace 中，將稱為 ContosoNotebook 的單一筆記本匯出至透過管線的資料夾 "C:\Notebook"。</span><span class="sxs-lookup"><span data-stu-id="6acad-121">Exports a single notebook called ContosoNotebook in the workspace ContosoWorkspace to the folder "C:\Notebook" through pipeline.</span></span>

## <span data-ttu-id="6acad-122">參數</span><span class="sxs-lookup"><span data-stu-id="6acad-122">PARAMETERS</span></span>

### <span data-ttu-id="6acad-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6acad-123">-AsJob</span></span>
<span data-ttu-id="6acad-124">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6acad-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6acad-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6acad-125">-DefaultProfile</span></span>
<span data-ttu-id="6acad-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6acad-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6acad-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6acad-127">-InputObject</span></span>
<span data-ttu-id="6acad-128">[筆記本] 物件。</span><span class="sxs-lookup"><span data-stu-id="6acad-128">The notebook object.</span></span>

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

### <span data-ttu-id="6acad-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6acad-129">-Name</span></span>
<span data-ttu-id="6acad-130">筆記本名稱。</span><span class="sxs-lookup"><span data-stu-id="6acad-130">The notebook name.</span></span>

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

### <span data-ttu-id="6acad-131">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="6acad-131">-OutputFolder</span></span>
<span data-ttu-id="6acad-132">放置筆記本的資料夾。</span><span class="sxs-lookup"><span data-stu-id="6acad-132">The folder where the notebook should be placed.</span></span>

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

### <span data-ttu-id="6acad-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6acad-133">-WorkspaceName</span></span>
<span data-ttu-id="6acad-134">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6acad-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6acad-135">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6acad-135">-WorkspaceObject</span></span>
<span data-ttu-id="6acad-136">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6acad-136">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6acad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6acad-137">CommonParameters</span></span>
<span data-ttu-id="6acad-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6acad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6acad-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6acad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6acad-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6acad-140">INPUTS</span></span>

### <span data-ttu-id="6acad-141">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6acad-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6acad-142">PSNotebookResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6acad-142">Microsoft.Azure.Commands.Synapse.Models.PSNotebookResource</span></span>

## <span data-ttu-id="6acad-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6acad-143">OUTPUTS</span></span>

### <span data-ttu-id="6acad-144">FileInfo</span><span class="sxs-lookup"><span data-stu-id="6acad-144">System.IO.FileInfo</span></span>

## <span data-ttu-id="6acad-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6acad-145">NOTES</span></span>

## <span data-ttu-id="6acad-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="6acad-146">RELATED LINKS</span></span>