---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cd7dad03d8542685339778d0b0cdac967f83ea21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625115"
---
# <span data-ttu-id="7b53b-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="7b53b-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="7b53b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b53b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b53b-103">取得儲存空間洞察力的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7b53b-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b53b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b53b-104">SYNTAX</span></span>

### <span data-ttu-id="7b53b-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="7b53b-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b53b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7b53b-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b53b-107">說明</span><span class="sxs-lookup"><span data-stu-id="7b53b-107">DESCRIPTION</span></span>
<span data-ttu-id="7b53b-108">**AzureRmOperationalInsightsStorageInsight** Cmdlet 會取得有關現有儲存空間洞察力的資訊。</span><span class="sxs-lookup"><span data-stu-id="7b53b-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="7b53b-109">如果指定了儲存的洞察力名稱，此 Cmdlet 會取得有關該儲存空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="7b53b-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="7b53b-110">如果您沒有指定名稱，此 Cmdlet 會取得有關工作區中所有儲存深入資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="7b53b-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="7b53b-111">示例</span><span class="sxs-lookup"><span data-stu-id="7b53b-111">EXAMPLES</span></span>

### <span data-ttu-id="7b53b-112">範例1：依名稱取得存儲洞察力</span><span class="sxs-lookup"><span data-stu-id="7b53b-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="7b53b-113">這個命令會從名為 ContosoWorkspace 的工作區取得名為 MyStorageInsight 的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="7b53b-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7b53b-114">範例2：使用工作區物件取得儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="7b53b-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="7b53b-115">第一個命令使用 **AzureRmOperationalInsightsWorkspace** Cmdlet 來取得 Operational Insights 工作區，然後將它儲存在 $Workspace 變數中。</span><span class="sxs-lookup"><span data-stu-id="7b53b-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="7b53b-116">第二個命令會針對 $Workspace 中的工作區，取得名為 MyStorageInsight 的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="7b53b-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="7b53b-117">參數</span><span class="sxs-lookup"><span data-stu-id="7b53b-117">PARAMETERS</span></span>

### <span data-ttu-id="7b53b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b53b-118">-Name</span></span>
<span data-ttu-id="7b53b-119">指定儲存空間洞察力名稱。</span><span class="sxs-lookup"><span data-stu-id="7b53b-119">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b53b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b53b-120">-ResourceGroupName</span></span>
<span data-ttu-id="7b53b-121">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b53b-121">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b53b-122">-工作區</span><span class="sxs-lookup"><span data-stu-id="7b53b-122">-Workspace</span></span>
<span data-ttu-id="7b53b-123">指定包含儲存深入資訊的工作區。</span><span class="sxs-lookup"><span data-stu-id="7b53b-123">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b53b-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7b53b-124">-WorkspaceName</span></span>
<span data-ttu-id="7b53b-125">指定包含儲存見解的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7b53b-125">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b53b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b53b-126">-DefaultProfile</span></span>
<span data-ttu-id="7b53b-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b53b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b53b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b53b-128">CommonParameters</span></span>
<span data-ttu-id="7b53b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b53b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b53b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b53b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b53b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7b53b-131">INPUTS</span></span>

### <span data-ttu-id="7b53b-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7b53b-132">PSWorkspace</span></span>
<span data-ttu-id="7b53b-133">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="7b53b-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="7b53b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7b53b-134">OUTPUTS</span></span>

### <span data-ttu-id="7b53b-135">[System.object]. 清單 ' 1 [OperationalInsights]。 PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="7b53b-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="7b53b-136">PSStorageInsight 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="7b53b-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="7b53b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7b53b-137">NOTES</span></span>

## <span data-ttu-id="7b53b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b53b-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b53b-139">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7b53b-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


