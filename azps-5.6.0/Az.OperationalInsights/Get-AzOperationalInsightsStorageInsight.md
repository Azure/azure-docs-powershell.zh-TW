---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: adbe725557ccf1535a83f5f411cfdc44fd69c6a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909345"
---
# <span data-ttu-id="8112a-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="8112a-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="8112a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8112a-102">SYNOPSIS</span></span>
<span data-ttu-id="8112a-103">獲得有關儲存空間深入資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="8112a-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="8112a-104">語法</span><span class="sxs-lookup"><span data-stu-id="8112a-104">SYNTAX</span></span>

### <span data-ttu-id="8112a-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="8112a-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8112a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8112a-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8112a-107">描述</span><span class="sxs-lookup"><span data-stu-id="8112a-107">DESCRIPTION</span></span>
<span data-ttu-id="8112a-108">**Get-AzOperationalInsightsStorageInsight** Cmdlet 會取得現有儲存深入資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="8112a-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="8112a-109">如果指定儲存深入資訊名稱，此 Cmdlet 會獲得該儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="8112a-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="8112a-110">如果您未指定名稱，此 Cmdlet 會獲得工作區中所有儲存深入資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="8112a-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="8112a-111">例子</span><span class="sxs-lookup"><span data-stu-id="8112a-111">EXAMPLES</span></span>

### <span data-ttu-id="8112a-112">範例 1：取得儲存空間深入資訊的名稱</span><span class="sxs-lookup"><span data-stu-id="8112a-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="8112a-113">此命令會從名為 ContosoWorkspace 的工作區中，獲得名為 MyStorageInsight 的儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="8112a-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8112a-114">範例 2：使用工作區物件取得儲存空間深入資訊</span><span class="sxs-lookup"><span data-stu-id="8112a-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="8112a-115">第一個命令使用 **Get-AzOperationalInsightsWorkspace** Cmdlet 取得營運深入資訊工作區，然後將它儲存在$Workspace變數。</span><span class="sxs-lookup"><span data-stu-id="8112a-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="8112a-116">第二個命令會針對工作區內的工作區，獲得名為 MyStorageInsight 的$Workspace。</span><span class="sxs-lookup"><span data-stu-id="8112a-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="8112a-117">參數</span><span class="sxs-lookup"><span data-stu-id="8112a-117">PARAMETERS</span></span>

### <span data-ttu-id="8112a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8112a-118">-DefaultProfile</span></span>
<span data-ttu-id="8112a-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8112a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8112a-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="8112a-120">-Name</span></span>
<span data-ttu-id="8112a-121">指定儲存深入資訊名稱。</span><span class="sxs-lookup"><span data-stu-id="8112a-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="8112a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8112a-122">-ResourceGroupName</span></span>
<span data-ttu-id="8112a-123">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8112a-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="8112a-124">-工作區</span><span class="sxs-lookup"><span data-stu-id="8112a-124">-Workspace</span></span>
<span data-ttu-id="8112a-125">指定包含儲存深入資訊工作區。</span><span class="sxs-lookup"><span data-stu-id="8112a-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="8112a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8112a-126">-WorkspaceName</span></span>
<span data-ttu-id="8112a-127">指定包含儲存深入資訊之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8112a-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="8112a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8112a-128">CommonParameters</span></span>
<span data-ttu-id="8112a-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8112a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8112a-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8112a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8112a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8112a-131">INPUTS</span></span>

### <span data-ttu-id="8112a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8112a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8112a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8112a-133">System.String</span></span>

## <span data-ttu-id="8112a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8112a-134">OUTPUTS</span></span>

### <span data-ttu-id="8112a-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="8112a-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="8112a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8112a-136">NOTES</span></span>

## <span data-ttu-id="8112a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8112a-137">RELATED LINKS</span></span>

[<span data-ttu-id="8112a-138">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8112a-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


