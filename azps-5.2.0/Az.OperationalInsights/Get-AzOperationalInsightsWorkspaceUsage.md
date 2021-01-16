---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281878"
---
# <span data-ttu-id="4cf84-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="4cf84-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="4cf84-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cf84-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf84-103">取得工作區的使用資料。</span><span class="sxs-lookup"><span data-stu-id="4cf84-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="4cf84-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cf84-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cf84-105">說明</span><span class="sxs-lookup"><span data-stu-id="4cf84-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf84-106">**AzOperationalInsightsWorkspaceUsage** Cmdlet 會檢索工作區的使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="4cf84-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="4cf84-107">這會顯示工作區在特定期間內經過分析的資料量。</span><span class="sxs-lookup"><span data-stu-id="4cf84-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="4cf84-108">示例</span><span class="sxs-lookup"><span data-stu-id="4cf84-108">EXAMPLES</span></span>

### <span data-ttu-id="4cf84-109">範例1：依工作區名稱取得使用資料</span><span class="sxs-lookup"><span data-stu-id="4cf84-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="4cf84-110">這個命令會在指定的資源群組中取得名為 MyWorkspace 之工作區的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4cf84-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="4cf84-111">範例2：使用管線取得使用資料</span><span class="sxs-lookup"><span data-stu-id="4cf84-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="4cf84-112">這個命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkSpace 的工作區，然後將工作區傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cf84-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="4cf84-113">此命令會取得該工作區的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4cf84-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="4cf84-114">參數</span><span class="sxs-lookup"><span data-stu-id="4cf84-114">PARAMETERS</span></span>

### <span data-ttu-id="4cf84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf84-115">-DefaultProfile</span></span>
<span data-ttu-id="4cf84-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4cf84-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cf84-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cf84-117">-Name</span></span>
<span data-ttu-id="4cf84-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf84-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="4cf84-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf84-119">-ResourceGroupName</span></span>
<span data-ttu-id="4cf84-120">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cf84-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="4cf84-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf84-121">CommonParameters</span></span>
<span data-ttu-id="4cf84-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cf84-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf84-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cf84-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf84-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4cf84-124">INPUTS</span></span>

### <span data-ttu-id="4cf84-125">System.object</span><span class="sxs-lookup"><span data-stu-id="4cf84-125">System.String</span></span>

## <span data-ttu-id="4cf84-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4cf84-126">OUTPUTS</span></span>

### <span data-ttu-id="4cf84-127">PSUsageMetric 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="4cf84-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="4cf84-128">筆記</span><span class="sxs-lookup"><span data-stu-id="4cf84-128">NOTES</span></span>

## <span data-ttu-id="4cf84-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cf84-129">RELATED LINKS</span></span>

[<span data-ttu-id="4cf84-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4cf84-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="4cf84-131">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4cf84-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


