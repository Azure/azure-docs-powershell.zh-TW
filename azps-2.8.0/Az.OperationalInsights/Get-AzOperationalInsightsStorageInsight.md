---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 589b6012a1819eac638f6197d0569972e4727fba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799421"
---
# <span data-ttu-id="277f4-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="277f4-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="277f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="277f4-102">SYNOPSIS</span></span>
<span data-ttu-id="277f4-103">取得儲存空間洞察力的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="277f4-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="277f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="277f4-104">SYNTAX</span></span>

### <span data-ttu-id="277f4-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="277f4-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="277f4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="277f4-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="277f4-107">說明</span><span class="sxs-lookup"><span data-stu-id="277f4-107">DESCRIPTION</span></span>
<span data-ttu-id="277f4-108">**AzOperationalInsightsStorageInsight** Cmdlet 會取得有關現有儲存空間洞察力的資訊。</span><span class="sxs-lookup"><span data-stu-id="277f4-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="277f4-109">如果指定了儲存的洞察力名稱，此 Cmdlet 會取得有關該儲存空間的資訊。</span><span class="sxs-lookup"><span data-stu-id="277f4-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="277f4-110">如果您沒有指定名稱，此 Cmdlet 會取得有關工作區中所有儲存深入資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="277f4-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="277f4-111">示例</span><span class="sxs-lookup"><span data-stu-id="277f4-111">EXAMPLES</span></span>

### <span data-ttu-id="277f4-112">範例1：依名稱取得存儲洞察力</span><span class="sxs-lookup"><span data-stu-id="277f4-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="277f4-113">這個命令會從名為 ContosoWorkspace 的工作區取得名為 MyStorageInsight 的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="277f4-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="277f4-114">範例2：使用工作區物件取得儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="277f4-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="277f4-115">第一個命令使用 **AzOperationalInsightsWorkspace** Cmdlet 來取得 Operational Insights 工作區，然後將它儲存在 $Workspace 變數中。</span><span class="sxs-lookup"><span data-stu-id="277f4-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="277f4-116">第二個命令會針對 $Workspace 中的工作區，取得名為 MyStorageInsight 的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="277f4-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="277f4-117">參數</span><span class="sxs-lookup"><span data-stu-id="277f4-117">PARAMETERS</span></span>

### <span data-ttu-id="277f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277f4-118">-DefaultProfile</span></span>
<span data-ttu-id="277f4-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="277f4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="277f4-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="277f4-120">-Name</span></span>
<span data-ttu-id="277f4-121">指定儲存空間洞察力名稱。</span><span class="sxs-lookup"><span data-stu-id="277f4-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="277f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="277f4-123">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="277f4-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="277f4-124">-工作區</span><span class="sxs-lookup"><span data-stu-id="277f4-124">-Workspace</span></span>
<span data-ttu-id="277f4-125">指定包含儲存深入資訊的工作區。</span><span class="sxs-lookup"><span data-stu-id="277f4-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="277f4-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="277f4-126">-WorkspaceName</span></span>
<span data-ttu-id="277f4-127">指定包含儲存見解的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="277f4-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="277f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277f4-128">CommonParameters</span></span>
<span data-ttu-id="277f4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="277f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277f4-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="277f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277f4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="277f4-131">INPUTS</span></span>

### <span data-ttu-id="277f4-132">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="277f4-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="277f4-133">System.object</span><span class="sxs-lookup"><span data-stu-id="277f4-133">System.String</span></span>

## <span data-ttu-id="277f4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="277f4-134">OUTPUTS</span></span>

### <span data-ttu-id="277f4-135">PSStorageInsight 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="277f4-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="277f4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="277f4-136">NOTES</span></span>

## <span data-ttu-id="277f4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="277f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="277f4-138">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="277f4-138">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


