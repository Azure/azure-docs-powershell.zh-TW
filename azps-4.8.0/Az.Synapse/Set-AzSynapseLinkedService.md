---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 635c1e064dbc081a5207f5c912c14166b2b01e17
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129100"
---
# <span data-ttu-id="f960e-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="f960e-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="f960e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f960e-102">SYNOPSIS</span></span>
<span data-ttu-id="f960e-103">將資料存放區或雲端服務連結到工作區。</span><span class="sxs-lookup"><span data-stu-id="f960e-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="f960e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f960e-104">SYNTAX</span></span>

### <span data-ttu-id="f960e-105">SetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="f960e-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f960e-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="f960e-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f960e-107">說明</span><span class="sxs-lookup"><span data-stu-id="f960e-107">DESCRIPTION</span></span>
<span data-ttu-id="f960e-108">**AzSynapseLinkedService** Cmdlet 會將資料存放區或雲端服務連結到工作區。</span><span class="sxs-lookup"><span data-stu-id="f960e-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="f960e-109">示例</span><span class="sxs-lookup"><span data-stu-id="f960e-109">EXAMPLES</span></span>

### <span data-ttu-id="f960e-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f960e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="f960e-111">這個命令會在名為 [ContosoWorkspace] 的工作區中，建立名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="f960e-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f960e-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f960e-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="f960e-113">這個命令會在名為 ContosoWorkspace 至管線的工作區中，建立名為 ContosoLinkedService 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="f960e-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f960e-114">參數</span><span class="sxs-lookup"><span data-stu-id="f960e-114">PARAMETERS</span></span>

### <span data-ttu-id="f960e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f960e-115">-AsJob</span></span>
<span data-ttu-id="f960e-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f960e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f960e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f960e-117">-DefaultProfile</span></span>
<span data-ttu-id="f960e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f960e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f960e-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="f960e-119">-DefinitionFile</span></span>
<span data-ttu-id="f960e-120">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="f960e-120">The JSON file path.</span></span>

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

### <span data-ttu-id="f960e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f960e-121">-Name</span></span>
<span data-ttu-id="f960e-122">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f960e-122">The linked service name.</span></span>

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

### <span data-ttu-id="f960e-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f960e-123">-WorkspaceName</span></span>
<span data-ttu-id="f960e-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f960e-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f960e-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f960e-125">-WorkspaceObject</span></span>
<span data-ttu-id="f960e-126">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="f960e-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f960e-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f960e-127">-Confirm</span></span>
<span data-ttu-id="f960e-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f960e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f960e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f960e-129">-WhatIf</span></span>
<span data-ttu-id="f960e-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f960e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f960e-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f960e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f960e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f960e-132">CommonParameters</span></span>
<span data-ttu-id="f960e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f960e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f960e-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f960e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f960e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f960e-135">INPUTS</span></span>

### <span data-ttu-id="f960e-136">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f960e-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f960e-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f960e-137">OUTPUTS</span></span>

### <span data-ttu-id="f960e-138">PSLinkedServiceResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f960e-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="f960e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f960e-139">NOTES</span></span>

## <span data-ttu-id="f960e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f960e-140">RELATED LINKS</span></span>
