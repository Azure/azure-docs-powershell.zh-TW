---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448595"
---
# <span data-ttu-id="7bd5d-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="7bd5d-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="7bd5d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7bd5d-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd5d-103">取得) 的分析 (警示規則。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="7bd5d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7bd5d-104">SYNTAX</span></span>

### <span data-ttu-id="7bd5d-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="7bd5d-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bd5d-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="7bd5d-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bd5d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd5d-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bd5d-108">說明</span><span class="sxs-lookup"><span data-stu-id="7bd5d-108">DESCRIPTION</span></span>
<span data-ttu-id="7bd5d-109">**AzSentinelAlertRule** Cmdlet 會從指定的工作區取得) 的分析 (警示規則。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="7bd5d-110">如果您指定 *AlertRuleId* 參數，則會傳回單一 **AlertRule** 物件。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="7bd5d-111">如果您沒有指定 *AlertRuleId* 參數，則會傳回包含指定工作區中所有警示規則的陣列。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="7bd5d-112">您可以使用 **AlertRule** 物件來更新 AlertRule，例如，您可以停用 **AlertRule**。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="7bd5d-113">示例</span><span class="sxs-lookup"><span data-stu-id="7bd5d-113">EXAMPLES</span></span>

### <span data-ttu-id="7bd5d-114">範例1</span><span class="sxs-lookup"><span data-stu-id="7bd5d-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="7bd5d-115">這個範例會在指定的工作區中取得所有 **AlertRules** ，然後將它儲存在 $AlertRules 變數中。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="7bd5d-116">範例2</span><span class="sxs-lookup"><span data-stu-id="7bd5d-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="7bd5d-117">這個範例會在指定的工作區中取得 **AlertRule** ，然後將其儲存在 $AlertRule 變數中。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="7bd5d-118">參數</span><span class="sxs-lookup"><span data-stu-id="7bd5d-118">PARAMETERS</span></span>

### <span data-ttu-id="7bd5d-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="7bd5d-119">-AlertRuleId</span></span>
<span data-ttu-id="7bd5d-120">[警示規則識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-120">Alert Rule Id.</span></span>

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

### <span data-ttu-id="7bd5d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd5d-121">-DefaultProfile</span></span>
<span data-ttu-id="7bd5d-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd5d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd5d-123">-ResourceGroupName</span></span>
<span data-ttu-id="7bd5d-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-124">Resource group name.</span></span>

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

### <span data-ttu-id="7bd5d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bd5d-125">-ResourceId</span></span>
<span data-ttu-id="7bd5d-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-126">Resource Id.</span></span>

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

### <span data-ttu-id="7bd5d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7bd5d-127">-WorkspaceName</span></span>
<span data-ttu-id="7bd5d-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-128">Workspace Name.</span></span>

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

### <span data-ttu-id="7bd5d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd5d-129">CommonParameters</span></span>
<span data-ttu-id="7bd5d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd5d-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7bd5d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd5d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7bd5d-132">INPUTS</span></span>

### <span data-ttu-id="7bd5d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7bd5d-133">System.String</span></span>
## <span data-ttu-id="7bd5d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7bd5d-134">OUTPUTS</span></span>

### <span data-ttu-id="7bd5d-135">SecurityInsights AlertRules. PSSentinelAlertRule （）</span><span class="sxs-lookup"><span data-stu-id="7bd5d-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="7bd5d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7bd5d-136">NOTES</span></span>

## <span data-ttu-id="7bd5d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7bd5d-137">RELATED LINKS</span></span>
