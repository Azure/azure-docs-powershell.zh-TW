---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130787"
---
# <span data-ttu-id="8e655-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="8e655-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="8e655-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e655-102">SYNOPSIS</span></span>
<span data-ttu-id="8e655-103">取得分析規則範本。</span><span class="sxs-lookup"><span data-stu-id="8e655-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="8e655-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e655-104">SYNTAX</span></span>

### <span data-ttu-id="8e655-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="8e655-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e655-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="8e655-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e655-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e655-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e655-108">說明</span><span class="sxs-lookup"><span data-stu-id="8e655-108">DESCRIPTION</span></span>
<span data-ttu-id="8e655-109">**AzSentinelAlertRuleTemplate** Cmdlet 會從指定的工作區取得警示規則範本。</span><span class="sxs-lookup"><span data-stu-id="8e655-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="8e655-110">如果您指定 *AlertRuleTemplateId* 參數，則會傳回單一 **AlertRuleTemplate** 物件。</span><span class="sxs-lookup"><span data-stu-id="8e655-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="8e655-111">如果您沒有指定 *AlertRuleTemplateId* 參數，則會傳回包含指定工作區中所有警示規則範本的陣列。</span><span class="sxs-lookup"><span data-stu-id="8e655-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="8e655-112">您可以使用 **AlertRuleTemplate** 物件來建立新的通知規則。</span><span class="sxs-lookup"><span data-stu-id="8e655-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="8e655-113">示例</span><span class="sxs-lookup"><span data-stu-id="8e655-113">EXAMPLES</span></span>

### <span data-ttu-id="8e655-114">範例1</span><span class="sxs-lookup"><span data-stu-id="8e655-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="8e655-115">這個範例會在指定的工作區中取得所有 **AlertRuleTemplates** ，然後將它儲存在 $AlertRuleTemplates 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e655-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="8e655-116">範例2</span><span class="sxs-lookup"><span data-stu-id="8e655-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="8e655-117">這個範例會在指定的工作區中取得 **AlertRuleTemplate** ，然後將其儲存在 $AlertRuleTemplate 變數中。</span><span class="sxs-lookup"><span data-stu-id="8e655-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="8e655-118">參數</span><span class="sxs-lookup"><span data-stu-id="8e655-118">PARAMETERS</span></span>

### <span data-ttu-id="8e655-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="8e655-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="8e655-120">範本警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e655-120">Template Alert Rule Id.</span></span>

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

### <span data-ttu-id="8e655-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e655-121">-DefaultProfile</span></span>
<span data-ttu-id="8e655-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e655-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e655-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e655-123">-ResourceGroupName</span></span>
<span data-ttu-id="8e655-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8e655-124">Resource group name.</span></span>

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

### <span data-ttu-id="8e655-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e655-125">-ResourceId</span></span>
<span data-ttu-id="8e655-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8e655-126">Resource Id.</span></span>

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

### <span data-ttu-id="8e655-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e655-127">-WorkspaceName</span></span>
<span data-ttu-id="8e655-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="8e655-128">Workspace Name.</span></span>

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

### <span data-ttu-id="8e655-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e655-129">CommonParameters</span></span>
<span data-ttu-id="8e655-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e655-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e655-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8e655-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e655-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8e655-132">INPUTS</span></span>

### <span data-ttu-id="8e655-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8e655-133">System.String</span></span>
## <span data-ttu-id="8e655-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8e655-134">OUTPUTS</span></span>

### <span data-ttu-id="8e655-135">SecurityInsights AlertRuleTemplates. PSSentinelAlertRuleTemplate （）</span><span class="sxs-lookup"><span data-stu-id="8e655-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="8e655-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8e655-136">NOTES</span></span>

## <span data-ttu-id="8e655-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e655-137">RELATED LINKS</span></span>
