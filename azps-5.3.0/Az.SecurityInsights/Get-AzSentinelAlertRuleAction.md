---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448588"
---
# <span data-ttu-id="d25f7-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="d25f7-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="d25f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d25f7-102">SYNOPSIS</span></span>
<span data-ttu-id="d25f7-103">取得自動回應 (警示規則動作) 。</span><span class="sxs-lookup"><span data-stu-id="d25f7-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="d25f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="d25f7-104">SYNTAX</span></span>

### <span data-ttu-id="d25f7-105">AlertRuleId (預設) </span><span class="sxs-lookup"><span data-stu-id="d25f7-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d25f7-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="d25f7-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d25f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="d25f7-107">DESCRIPTION</span></span>
<span data-ttu-id="d25f7-108">**AzSentinelAlertRuleAction** Cmdlet 會從指定的工作區取得自動回應 (警示規則動作) 。</span><span class="sxs-lookup"><span data-stu-id="d25f7-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="d25f7-109">如果您指定 *ActionId* 和 *AlertRuleId* 參數，則會傳回單一 **AlertRuleAction** 物件。</span><span class="sxs-lookup"><span data-stu-id="d25f7-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="d25f7-110">如果您沒有指定 *ActionId* 參數，則會傳回包含指定工作區中以警報規則之所有動作的陣列。</span><span class="sxs-lookup"><span data-stu-id="d25f7-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="d25f7-111">您可以使用 **action** 物件來更新動作，例如，您可以變更警示規則的 **動作** 。</span><span class="sxs-lookup"><span data-stu-id="d25f7-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="d25f7-112">示例</span><span class="sxs-lookup"><span data-stu-id="d25f7-112">EXAMPLES</span></span>

### <span data-ttu-id="d25f7-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d25f7-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="d25f7-114">這個範例會在指定的工作區中取得指定之警示規則的所有 **動作** ，然後將其儲存在 $AlertRuleActions 變數中。</span><span class="sxs-lookup"><span data-stu-id="d25f7-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="d25f7-115">範例2</span><span class="sxs-lookup"><span data-stu-id="d25f7-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="d25f7-116">這個範例會在指定的工作區中取得指定警示規則的 **AlertRuleAction** ，然後將其儲存在 $AlertRuleAction 變數中。</span><span class="sxs-lookup"><span data-stu-id="d25f7-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="d25f7-117">參數</span><span class="sxs-lookup"><span data-stu-id="d25f7-117">PARAMETERS</span></span>

### <span data-ttu-id="d25f7-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="d25f7-118">-ActionId</span></span>
<span data-ttu-id="d25f7-119">[動作識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d25f7-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25f7-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="d25f7-120">-AlertRuleId</span></span>
<span data-ttu-id="d25f7-121">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="d25f7-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25f7-122">-DefaultProfile</span></span>
<span data-ttu-id="d25f7-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d25f7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="d25f7-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d25f7-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25f7-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d25f7-126">-WorkspaceName</span></span>
<span data-ttu-id="d25f7-127">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d25f7-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25f7-128">CommonParameters</span></span>
<span data-ttu-id="d25f7-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d25f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25f7-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d25f7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25f7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d25f7-131">INPUTS</span></span>

### <span data-ttu-id="d25f7-132">所有</span><span class="sxs-lookup"><span data-stu-id="d25f7-132">None</span></span>
## <span data-ttu-id="d25f7-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d25f7-133">OUTPUTS</span></span>

### <span data-ttu-id="d25f7-134">PSSentinelActionResponse 中的 SecurityInsights.。</span><span class="sxs-lookup"><span data-stu-id="d25f7-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="d25f7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d25f7-135">NOTES</span></span>

## <span data-ttu-id="d25f7-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d25f7-136">RELATED LINKS</span></span>
