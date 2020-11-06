---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: fa238d963f472e79946632311a9f93c8586650ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456939"
---
# <span data-ttu-id="95fc8-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="95fc8-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="95fc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="95fc8-103">取得工作區的使用資料。</span><span class="sxs-lookup"><span data-stu-id="95fc8-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95fc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="95fc8-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95fc8-105">說明</span><span class="sxs-lookup"><span data-stu-id="95fc8-105">DESCRIPTION</span></span>
<span data-ttu-id="95fc8-106">**AzureRmOperationalInsightsWorkspaceUsage** Cmdlet 會檢索工作區的使用方式資料。</span><span class="sxs-lookup"><span data-stu-id="95fc8-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="95fc8-107">這會顯示工作區在特定期間內經過分析的資料量。</span><span class="sxs-lookup"><span data-stu-id="95fc8-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="95fc8-108">示例</span><span class="sxs-lookup"><span data-stu-id="95fc8-108">EXAMPLES</span></span>

### <span data-ttu-id="95fc8-109">範例1：依工作區名稱取得使用資料</span><span class="sxs-lookup"><span data-stu-id="95fc8-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="95fc8-110">這個命令會在指定的資源群組中取得名為 MyWorkspace 之工作區的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="95fc8-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="95fc8-111">範例2：使用管線取得使用資料</span><span class="sxs-lookup"><span data-stu-id="95fc8-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="95fc8-112">這個命令會使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkSpace 的工作區，然後將工作區傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95fc8-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="95fc8-113">此命令會取得該工作區的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="95fc8-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="95fc8-114">參數</span><span class="sxs-lookup"><span data-stu-id="95fc8-114">PARAMETERS</span></span>

### <span data-ttu-id="95fc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95fc8-115">-DefaultProfile</span></span>
<span data-ttu-id="95fc8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="95fc8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95fc8-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="95fc8-117">-Name</span></span>
<span data-ttu-id="95fc8-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="95fc8-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="95fc8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95fc8-119">-ResourceGroupName</span></span>
<span data-ttu-id="95fc8-120">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="95fc8-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="95fc8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95fc8-121">CommonParameters</span></span>
<span data-ttu-id="95fc8-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95fc8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95fc8-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95fc8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95fc8-124">輸入</span><span class="sxs-lookup"><span data-stu-id="95fc8-124">INPUTS</span></span>

### <span data-ttu-id="95fc8-125">System.object</span><span class="sxs-lookup"><span data-stu-id="95fc8-125">System.String</span></span>

## <span data-ttu-id="95fc8-126">輸出</span><span class="sxs-lookup"><span data-stu-id="95fc8-126">OUTPUTS</span></span>

### <span data-ttu-id="95fc8-127">PSUsageMetric 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="95fc8-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="95fc8-128">筆記</span><span class="sxs-lookup"><span data-stu-id="95fc8-128">NOTES</span></span>

## <span data-ttu-id="95fc8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="95fc8-129">RELATED LINKS</span></span>

[<span data-ttu-id="95fc8-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="95fc8-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="95fc8-131">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="95fc8-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


