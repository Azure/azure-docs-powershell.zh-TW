---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: b5b14cbf816a7872abf431f787f9e3102006901c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915274"
---
# <span data-ttu-id="8f2c7-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="8f2c7-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="8f2c7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8f2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2c7-103">獲得工作區的使用資料。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="8f2c7-104">語法</span><span class="sxs-lookup"><span data-stu-id="8f2c7-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f2c7-105">描述</span><span class="sxs-lookup"><span data-stu-id="8f2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="8f2c7-106">**Get-AzOperationalInsightsWorkspaceUsage Cmdlet** 會取得工作區的使用資料。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="8f2c7-107">這會公開工作區在一段特定期間分析的資料。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="8f2c7-108">例子</span><span class="sxs-lookup"><span data-stu-id="8f2c7-108">EXAMPLES</span></span>

### <span data-ttu-id="8f2c7-109">範例 1：根據工作區名稱取得使用方式資料</span><span class="sxs-lookup"><span data-stu-id="8f2c7-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="8f2c7-110">此命令會獲得指定資源群組中名為 MyWorkspace 的工作區的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="8f2c7-111">範例 2：使用管線取得使用狀況資料</span><span class="sxs-lookup"><span data-stu-id="8f2c7-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="8f2c7-112">此命令會使用 Cmdlet Get-AzOperationalInsightsWorkspace名為 MyWorkSpace 的工作區，然後將工作區傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="8f2c7-113">該命令會獲得該工作區的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="8f2c7-114">參數</span><span class="sxs-lookup"><span data-stu-id="8f2c7-114">PARAMETERS</span></span>

### <span data-ttu-id="8f2c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2c7-115">-DefaultProfile</span></span>
<span data-ttu-id="8f2c7-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8f2c7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f2c7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f2c7-117">-Name</span></span>
<span data-ttu-id="8f2c7-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="8f2c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f2c7-120">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="8f2c7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2c7-121">CommonParameters</span></span>
<span data-ttu-id="8f2c7-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2c7-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8f2c7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2c7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8f2c7-124">INPUTS</span></span>

### <span data-ttu-id="8f2c7-125">System.String</span><span class="sxs-lookup"><span data-stu-id="8f2c7-125">System.String</span></span>

## <span data-ttu-id="8f2c7-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8f2c7-126">OUTPUTS</span></span>

### <span data-ttu-id="8f2c7-127">Microsoft.Azure.Commands.OperationalInsights.models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="8f2c7-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="8f2c7-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8f2c7-128">NOTES</span></span>

## <span data-ttu-id="8f2c7-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f2c7-129">RELATED LINKS</span></span>

[<span data-ttu-id="8f2c7-130">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8f2c7-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="8f2c7-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f2c7-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


