---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 1e05754245b4179d02c144538473fa586531f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916325"
---
# <span data-ttu-id="c251a-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="c251a-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="c251a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c251a-102">SYNOPSIS</span></span>
<span data-ttu-id="c251a-103">將資料存放區或雲端服務連結至工作區。</span><span class="sxs-lookup"><span data-stu-id="c251a-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="c251a-104">語法</span><span class="sxs-lookup"><span data-stu-id="c251a-104">SYNTAX</span></span>

### <span data-ttu-id="c251a-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="c251a-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c251a-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="c251a-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c251a-107">描述</span><span class="sxs-lookup"><span data-stu-id="c251a-107">DESCRIPTION</span></span>
<span data-ttu-id="c251a-108">**Set-AzSynapseLinkedService** Cmdlet 會連結資料存放區或雲端服務至工作區。</span><span class="sxs-lookup"><span data-stu-id="c251a-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="c251a-109">例子</span><span class="sxs-lookup"><span data-stu-id="c251a-109">EXAMPLES</span></span>

### <span data-ttu-id="c251a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c251a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="c251a-111">此命令在名為 ContosoWorkspace 的工作區中建立名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="c251a-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="c251a-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c251a-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="c251a-113">此命令會透過管線在名為 ContosoWorkspace 的工作區中建立名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="c251a-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="c251a-114">參數</span><span class="sxs-lookup"><span data-stu-id="c251a-114">PARAMETERS</span></span>

### <span data-ttu-id="c251a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c251a-115">-AsJob</span></span>
<span data-ttu-id="c251a-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c251a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c251a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c251a-117">-DefaultProfile</span></span>
<span data-ttu-id="c251a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c251a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c251a-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="c251a-119">-DefinitionFile</span></span>
<span data-ttu-id="c251a-120">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="c251a-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c251a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c251a-121">-Name</span></span>
<span data-ttu-id="c251a-122">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c251a-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c251a-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c251a-123">-WorkspaceName</span></span>
<span data-ttu-id="c251a-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c251a-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c251a-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c251a-125">-WorkspaceObject</span></span>
<span data-ttu-id="c251a-126">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="c251a-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c251a-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c251a-127">-Confirm</span></span>
<span data-ttu-id="c251a-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c251a-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c251a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c251a-129">-WhatIf</span></span>
<span data-ttu-id="c251a-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c251a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c251a-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c251a-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c251a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c251a-132">CommonParameters</span></span>
<span data-ttu-id="c251a-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c251a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c251a-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c251a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c251a-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c251a-135">INPUTS</span></span>

### <span data-ttu-id="c251a-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c251a-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c251a-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c251a-137">OUTPUTS</span></span>

### <span data-ttu-id="c251a-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="c251a-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="c251a-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c251a-139">NOTES</span></span>

## <span data-ttu-id="c251a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c251a-140">RELATED LINKS</span></span>
