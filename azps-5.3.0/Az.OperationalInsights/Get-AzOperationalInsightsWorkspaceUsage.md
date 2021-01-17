---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450057"
---
# <span data-ttu-id="dc472-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="dc472-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="dc472-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc472-102">SYNOPSIS</span></span>
<span data-ttu-id="dc472-103">取得工作區的使用資料。</span><span class="sxs-lookup"><span data-stu-id="dc472-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="dc472-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc472-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc472-105">說明</span><span class="sxs-lookup"><span data-stu-id="dc472-105">DESCRIPTION</span></span>
<span data-ttu-id="dc472-106">**AzOperationalInsightsWorkspaceUsage** Cmdlet 會檢索工作區的使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="dc472-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="dc472-107">這會顯示工作區在特定期間內經過分析的資料量。</span><span class="sxs-lookup"><span data-stu-id="dc472-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="dc472-108">示例</span><span class="sxs-lookup"><span data-stu-id="dc472-108">EXAMPLES</span></span>

### <span data-ttu-id="dc472-109">範例1：依工作區名稱取得使用資料</span><span class="sxs-lookup"><span data-stu-id="dc472-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="dc472-110">這個命令會在指定的資源群組中取得名為 MyWorkspace 之工作區的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dc472-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="dc472-111">範例2：使用管線取得使用資料</span><span class="sxs-lookup"><span data-stu-id="dc472-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="dc472-112">這個命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkSpace 的工作區，然後將工作區傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc472-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="dc472-113">此命令會取得該工作區的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dc472-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="dc472-114">參數</span><span class="sxs-lookup"><span data-stu-id="dc472-114">PARAMETERS</span></span>

### <span data-ttu-id="dc472-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc472-115">-DefaultProfile</span></span>
<span data-ttu-id="dc472-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dc472-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc472-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc472-117">-Name</span></span>
<span data-ttu-id="dc472-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="dc472-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc472-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc472-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc472-120">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc472-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc472-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc472-121">CommonParameters</span></span>
<span data-ttu-id="dc472-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc472-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc472-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc472-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc472-124">輸入</span><span class="sxs-lookup"><span data-stu-id="dc472-124">INPUTS</span></span>

### <span data-ttu-id="dc472-125">System.object</span><span class="sxs-lookup"><span data-stu-id="dc472-125">System.String</span></span>

## <span data-ttu-id="dc472-126">輸出</span><span class="sxs-lookup"><span data-stu-id="dc472-126">OUTPUTS</span></span>

### <span data-ttu-id="dc472-127">PSUsageMetric 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="dc472-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="dc472-128">筆記</span><span class="sxs-lookup"><span data-stu-id="dc472-128">NOTES</span></span>

## <span data-ttu-id="dc472-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc472-129">RELATED LINKS</span></span>

[<span data-ttu-id="dc472-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc472-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="dc472-131">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="dc472-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


