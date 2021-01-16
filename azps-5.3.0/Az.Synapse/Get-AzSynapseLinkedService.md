---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseLinkedService.md
ms.openlocfilehash: d7f494b6ba943214106363a5b7dfe4dfb5cdd877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435799"
---
# <span data-ttu-id="f3f59-101">Get-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="f3f59-101">Get-AzSynapseLinkedService</span></span>

## <span data-ttu-id="f3f59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3f59-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f59-103">取得工作區中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3f59-103">Gets information about linked services in workspace.</span></span>

## <span data-ttu-id="f3f59-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3f59-104">SYNTAX</span></span>

### <span data-ttu-id="f3f59-105">GetByName (預設) </span><span class="sxs-lookup"><span data-stu-id="f3f59-105">GetByName (Default)</span></span>
```
Get-AzSynapseLinkedService -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3f59-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="f3f59-106">GetByObject</span></span>
```
Get-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f59-107">說明</span><span class="sxs-lookup"><span data-stu-id="f3f59-107">DESCRIPTION</span></span>
<span data-ttu-id="f3f59-108">**AzSynapseLinkedService** Cmdlet 會取得工作區中連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3f59-108">The **Get-AzSynapseLinkedService** cmdlet gets information about linked services in workspace.</span></span>
<span data-ttu-id="f3f59-109">如果您指定連結服務的名稱，此 Cmdlet 會取得該連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3f59-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="f3f59-110">如果您沒有指定名稱，此 Cmdlet 會取得工作區中所有連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3f59-110">If you do not specify a name, this cmdlet gets information about all the linked services in the workspace.</span></span>

## <span data-ttu-id="f3f59-111">示例</span><span class="sxs-lookup"><span data-stu-id="f3f59-111">EXAMPLES</span></span>

### <span data-ttu-id="f3f59-112">範例1</span><span class="sxs-lookup"><span data-stu-id="f3f59-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="f3f59-113">這個命令會在名為 ContosoWorkspace 的工作區中取得所有連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3f59-113">This command gets information about all linked services in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f3f59-114">範例2</span><span class="sxs-lookup"><span data-stu-id="f3f59-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService
```

<span data-ttu-id="f3f59-115">這個命令會在名為 ContosoWorkspace 的工作區中，取得名為 ContosoLinkedService 之連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3f59-115">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f3f59-116">範例3</span><span class="sxs-lookup"><span data-stu-id="f3f59-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseLinkedService -Name ContosoLinkedService
```

<span data-ttu-id="f3f59-117">這個命令會在名為 ContosoWorkspace 至管線的工作區中，取得名為 ContosoLinkedService 的連結服務的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3f59-117">This command gets information about the linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f3f59-118">參數</span><span class="sxs-lookup"><span data-stu-id="f3f59-118">PARAMETERS</span></span>

### <span data-ttu-id="f3f59-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f59-119">-DefaultProfile</span></span>
<span data-ttu-id="f3f59-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3f59-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3f59-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3f59-121">-Name</span></span>
<span data-ttu-id="f3f59-122">連結的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="f3f59-122">The linked service name.</span></span>

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

### <span data-ttu-id="f3f59-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f3f59-123">-WorkspaceName</span></span>
<span data-ttu-id="f3f59-124">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3f59-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f3f59-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f3f59-125">-WorkspaceObject</span></span>
<span data-ttu-id="f3f59-126">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="f3f59-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f3f59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f59-127">CommonParameters</span></span>
<span data-ttu-id="f3f59-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3f59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f59-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f3f59-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f59-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f3f59-130">INPUTS</span></span>

### <span data-ttu-id="f3f59-131">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f3f59-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f3f59-132">輸出</span><span class="sxs-lookup"><span data-stu-id="f3f59-132">OUTPUTS</span></span>

### <span data-ttu-id="f3f59-133">PSLinkedServiceResource 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="f3f59-133">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="f3f59-134">筆記</span><span class="sxs-lookup"><span data-stu-id="f3f59-134">NOTES</span></span>

## <span data-ttu-id="f3f59-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3f59-135">RELATED LINKS</span></span>
