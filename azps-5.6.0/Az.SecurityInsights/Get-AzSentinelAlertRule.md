---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 836d566c9e75fdce825542ebb13520933c071cd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910610"
---
# <span data-ttu-id="dcfde-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="dcfde-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="dcfde-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dcfde-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfde-103">獲得分析 (警示規則) 。</span><span class="sxs-lookup"><span data-stu-id="dcfde-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="dcfde-104">語法</span><span class="sxs-lookup"><span data-stu-id="dcfde-104">SYNTAX</span></span>

### <span data-ttu-id="dcfde-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="dcfde-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcfde-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="dcfde-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcfde-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcfde-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcfde-108">描述</span><span class="sxs-lookup"><span data-stu-id="dcfde-108">DESCRIPTION</span></span>
<span data-ttu-id="dcfde-109">**Get-AzSentinelAlertRule** Cmdlet 會從 (工作區取得分析) 警示規則。</span><span class="sxs-lookup"><span data-stu-id="dcfde-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="dcfde-110">如果您指定 *AlertRuleId* 參數，會返回單 **一 AlertRule** 物件。</span><span class="sxs-lookup"><span data-stu-id="dcfde-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="dcfde-111">如果您未指定 *AlertRuleId* 參數，則會返回一個陣列，其中包含指定工作區中所有警示規則。</span><span class="sxs-lookup"><span data-stu-id="dcfde-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="dcfde-112">您可以使用 **AlertRule 物件** 來更新 AlertRule，例如您可以停用 **AlertRule。**</span><span class="sxs-lookup"><span data-stu-id="dcfde-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="dcfde-113">例子</span><span class="sxs-lookup"><span data-stu-id="dcfde-113">EXAMPLES</span></span>

### <span data-ttu-id="dcfde-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="dcfde-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="dcfde-115">此範例會獲得指定工作區的所有 **AlertRules，** 然後將它儲存在$AlertRules變數。</span><span class="sxs-lookup"><span data-stu-id="dcfde-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="dcfde-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="dcfde-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="dcfde-117">此範例會于指定的工作區中收到 **AlertRule，** 然後將它儲存在 $AlertRule 變數中。</span><span class="sxs-lookup"><span data-stu-id="dcfde-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="dcfde-118">參數</span><span class="sxs-lookup"><span data-stu-id="dcfde-118">PARAMETERS</span></span>

### <span data-ttu-id="dcfde-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="dcfde-119">-AlertRuleId</span></span>
<span data-ttu-id="dcfde-120">警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="dcfde-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcfde-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfde-121">-DefaultProfile</span></span>
<span data-ttu-id="dcfde-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcfde-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcfde-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcfde-123">-ResourceGroupName</span></span>
<span data-ttu-id="dcfde-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="dcfde-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcfde-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcfde-125">-ResourceId</span></span>
<span data-ttu-id="dcfde-126">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dcfde-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcfde-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dcfde-127">-WorkspaceName</span></span>
<span data-ttu-id="dcfde-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="dcfde-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcfde-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfde-129">CommonParameters</span></span>
<span data-ttu-id="dcfde-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dcfde-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcfde-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcfde-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfde-132">輸入</span><span class="sxs-lookup"><span data-stu-id="dcfde-132">INPUTS</span></span>

### <span data-ttu-id="dcfde-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dcfde-133">System.String</span></span>
## <span data-ttu-id="dcfde-134">輸出</span><span class="sxs-lookup"><span data-stu-id="dcfde-134">OUTPUTS</span></span>

### <span data-ttu-id="dcfde-135">Microsoft.Azure.Commands.SecurityInsights.models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="dcfde-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="dcfde-136">筆記</span><span class="sxs-lookup"><span data-stu-id="dcfde-136">NOTES</span></span>

## <span data-ttu-id="dcfde-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcfde-137">RELATED LINKS</span></span>
