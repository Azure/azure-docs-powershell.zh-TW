---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 37cc56714712d71ab34adee14a8b758cd9dd1113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910613"
---
# <span data-ttu-id="9b219-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="9b219-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="9b219-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b219-102">SYNOPSIS</span></span>
<span data-ttu-id="9b219-103">取得自動回應 (警示規則動作) 。</span><span class="sxs-lookup"><span data-stu-id="9b219-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="9b219-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b219-104">SYNTAX</span></span>

### <span data-ttu-id="9b219-105">AlertRuleId (預設) </span><span class="sxs-lookup"><span data-stu-id="9b219-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b219-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="9b219-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b219-107">描述</span><span class="sxs-lookup"><span data-stu-id="9b219-107">DESCRIPTION</span></span>
<span data-ttu-id="9b219-108">**Get-AzSentinelAlertRuleAction** Cmdlet 會從指定的工作區 (警示規則動作) 自動回應。</span><span class="sxs-lookup"><span data-stu-id="9b219-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="9b219-109">如果您指定 *ActionId* 和 *AlertRuleId* 參數，會返回單 **一 AlertRuleAction** 物件。</span><span class="sxs-lookup"><span data-stu-id="9b219-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="9b219-110">如果您未指定 *ActionId* 參數，會針對指定工作區中特定警示規則，會包含所有動作的陣列。</span><span class="sxs-lookup"><span data-stu-id="9b219-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="9b219-111">您可以使用動作 **物件** 來更新動作，例如，您可以變更警示規則的動作。 </span><span class="sxs-lookup"><span data-stu-id="9b219-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="9b219-112">例子</span><span class="sxs-lookup"><span data-stu-id="9b219-112">EXAMPLES</span></span>

### <span data-ttu-id="9b219-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="9b219-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="9b219-114">此範例會獲得指定工作區中指定警示規則的所有動作，然後將它儲存在$AlertRuleActions變數。</span><span class="sxs-lookup"><span data-stu-id="9b219-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="9b219-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="9b219-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="9b219-116">此範例會針對指定的工作區中指定的警示規則獲得 **AlertRuleAction，** 然後將它儲存在 $AlertRuleAction 變數中。</span><span class="sxs-lookup"><span data-stu-id="9b219-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="9b219-117">參數</span><span class="sxs-lookup"><span data-stu-id="9b219-117">PARAMETERS</span></span>

### <span data-ttu-id="9b219-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="9b219-118">-ActionId</span></span>
<span data-ttu-id="9b219-119">動作識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b219-119">Action Id.</span></span>

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

### <span data-ttu-id="9b219-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="9b219-120">-AlertRuleId</span></span>
<span data-ttu-id="9b219-121">警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b219-121">Alert Rule Id.</span></span>

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

### <span data-ttu-id="9b219-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b219-122">-DefaultProfile</span></span>
<span data-ttu-id="9b219-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b219-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b219-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b219-124">-ResourceGroupName</span></span>
<span data-ttu-id="9b219-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9b219-125">Resource group name.</span></span>

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

### <span data-ttu-id="9b219-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b219-126">-WorkspaceName</span></span>
<span data-ttu-id="9b219-127">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="9b219-127">Workspace Name.</span></span>

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

### <span data-ttu-id="9b219-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b219-128">CommonParameters</span></span>
<span data-ttu-id="9b219-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b219-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b219-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b219-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b219-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9b219-131">INPUTS</span></span>

### <span data-ttu-id="9b219-132">沒有</span><span class="sxs-lookup"><span data-stu-id="9b219-132">None</span></span>
## <span data-ttu-id="9b219-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9b219-133">OUTPUTS</span></span>

### <span data-ttu-id="9b219-134">Microsoft.Azure.Commands.SecurityInsights.models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="9b219-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="9b219-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9b219-135">NOTES</span></span>

## <span data-ttu-id="9b219-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b219-136">RELATED LINKS</span></span>
