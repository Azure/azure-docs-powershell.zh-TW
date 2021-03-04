---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: 61ddc7c6a71dcc5545b8bdc2751e619d7da8e3bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905726"
---
# <span data-ttu-id="d2b06-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="d2b06-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="d2b06-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d2b06-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b06-103">在工作區中獲得連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2b06-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="d2b06-104">語法</span><span class="sxs-lookup"><span data-stu-id="d2b06-104">SYNTAX</span></span>

### <span data-ttu-id="d2b06-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d2b06-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2b06-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d2b06-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2b06-107">描述</span><span class="sxs-lookup"><span data-stu-id="d2b06-107">DESCRIPTION</span></span>
<span data-ttu-id="d2b06-108">**Get-AzSynapseLinkedService** Cmdlet 會取得工作區中連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2b06-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="d2b06-109">如果您指定連結服務的名稱，此 Cmdlet 會獲得該連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2b06-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="d2b06-110">如果您未指定名稱，此 Cmdlet 會獲得工作區中所有連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2b06-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="d2b06-111">例子</span><span class="sxs-lookup"><span data-stu-id="d2b06-111">EXAMPLES</span></span>

### <span data-ttu-id="d2b06-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d2b06-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d2b06-113">此命令會獲得名為 ContosoWorkspace 工作區中所有連結服務的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2b06-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d2b06-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d2b06-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="d2b06-115">此命令會從名為 ContosoWorkspace 的工作區中，獲得名為 ContosoLinkedService 的連結服務相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2b06-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d2b06-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="d2b06-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="d2b06-117">此命令會透過管道，在名為 ContosoWorkspace 的工作區中，獲得名為 ContosoLinkedService 的連結服務相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d2b06-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d2b06-118">參數</span><span class="sxs-lookup"><span data-stu-id="d2b06-118">PARAMETERS</span></span>

### <span data-ttu-id="d2b06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b06-119">-DefaultProfile</span></span>
<span data-ttu-id="d2b06-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2b06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2b06-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d2b06-121">-Name</span></span>
<span data-ttu-id="d2b06-122">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="d2b06-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2b06-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2b06-123">-WorkspaceName</span></span>
<span data-ttu-id="d2b06-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2b06-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d2b06-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d2b06-125">-WorkspaceObject</span></span>
<span data-ttu-id="d2b06-126">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="d2b06-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d2b06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b06-127">CommonParameters</span></span>
<span data-ttu-id="d2b06-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d2b06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b06-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2b06-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b06-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d2b06-130">INPUTS</span></span>

### <span data-ttu-id="d2b06-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2b06-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d2b06-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d2b06-132">OUTPUTS</span></span>

### <span data-ttu-id="d2b06-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="d2b06-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="d2b06-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d2b06-134">NOTES</span></span>

## <span data-ttu-id="d2b06-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2b06-135">RELATED LINKS</span></span>
