---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: db398fe5870a1ff304637c9aa33bf168c49a7759
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915874"
---
# <span data-ttu-id="17fdc-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="17fdc-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="17fdc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="17fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="17fdc-103">取得分析規則範本。</span><span class="sxs-lookup"><span data-stu-id="17fdc-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="17fdc-104">語法</span><span class="sxs-lookup"><span data-stu-id="17fdc-104">SYNTAX</span></span>

### <span data-ttu-id="17fdc-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="17fdc-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17fdc-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="17fdc-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17fdc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="17fdc-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17fdc-108">描述</span><span class="sxs-lookup"><span data-stu-id="17fdc-108">DESCRIPTION</span></span>
<span data-ttu-id="17fdc-109">**Get-AzSentinelAlertRuleTemplate** Cmdlet 會從指定的工作區取得警示規則範本。</span><span class="sxs-lookup"><span data-stu-id="17fdc-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="17fdc-110">如果您指定 *AlertRuleTemplateId* 參數，會返回單 **一 AlertRuleTemplate** 物件。</span><span class="sxs-lookup"><span data-stu-id="17fdc-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="17fdc-111">如果您未指定 *AlertRuleTemplateId* 參數，則會返回包含指定工作區中所有警示規則範本的陣列。</span><span class="sxs-lookup"><span data-stu-id="17fdc-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="17fdc-112">您可以使用 **AlertRuleTemplate 物件** 來建立新警示規則。</span><span class="sxs-lookup"><span data-stu-id="17fdc-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="17fdc-113">例子</span><span class="sxs-lookup"><span data-stu-id="17fdc-113">EXAMPLES</span></span>

### <span data-ttu-id="17fdc-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="17fdc-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="17fdc-115">此範例會獲得指定工作區中所有 **AlertRuleTemplates，** 然後將它儲存在 $AlertRuleTemplates 變數中。</span><span class="sxs-lookup"><span data-stu-id="17fdc-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="17fdc-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="17fdc-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="17fdc-117">此範例會獲得指定工作區中的 **AlertRuleTemplate，** 然後將它儲存在 $AlertRuleTemplate 變數中。</span><span class="sxs-lookup"><span data-stu-id="17fdc-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="17fdc-118">參數</span><span class="sxs-lookup"><span data-stu-id="17fdc-118">PARAMETERS</span></span>

### <span data-ttu-id="17fdc-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="17fdc-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="17fdc-120">範本通知規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="17fdc-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fdc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fdc-121">-DefaultProfile</span></span>
<span data-ttu-id="17fdc-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="17fdc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17fdc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fdc-123">-ResourceGroupName</span></span>
<span data-ttu-id="17fdc-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="17fdc-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fdc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17fdc-125">-ResourceId</span></span>
<span data-ttu-id="17fdc-126">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="17fdc-126">Resource Id.</span></span>

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

### <span data-ttu-id="17fdc-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="17fdc-127">-WorkspaceName</span></span>
<span data-ttu-id="17fdc-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="17fdc-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fdc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fdc-129">CommonParameters</span></span>
<span data-ttu-id="17fdc-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="17fdc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fdc-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17fdc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fdc-132">輸入</span><span class="sxs-lookup"><span data-stu-id="17fdc-132">INPUTS</span></span>

### <span data-ttu-id="17fdc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="17fdc-133">System.String</span></span>
## <span data-ttu-id="17fdc-134">輸出</span><span class="sxs-lookup"><span data-stu-id="17fdc-134">OUTPUTS</span></span>

### <span data-ttu-id="17fdc-135">Microsoft.Azure.Commands.SecurityInsights.models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="17fdc-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="17fdc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="17fdc-136">NOTES</span></span>

## <span data-ttu-id="17fdc-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="17fdc-137">RELATED LINKS</span></span>
