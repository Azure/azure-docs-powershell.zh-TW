---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448575"
---
# <span data-ttu-id="0d3aa-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="0d3aa-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="0d3aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="0d3aa-103">取得分析規則範本。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="0d3aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d3aa-104">SYNTAX</span></span>

### <span data-ttu-id="0d3aa-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="0d3aa-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d3aa-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="0d3aa-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d3aa-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d3aa-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d3aa-108">說明</span><span class="sxs-lookup"><span data-stu-id="0d3aa-108">DESCRIPTION</span></span>
<span data-ttu-id="0d3aa-109">**AzSentinelAlertRuleTemplate** Cmdlet 會從指定的工作區取得警示規則範本。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="0d3aa-110">如果您指定 *AlertRuleTemplateId* 參數，則會傳回單一 **AlertRuleTemplate** 物件。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="0d3aa-111">如果您沒有指定 *AlertRuleTemplateId* 參數，則會傳回包含指定工作區中所有警示規則範本的陣列。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="0d3aa-112">您可以使用 **AlertRuleTemplate** 物件來建立新的通知規則。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="0d3aa-113">示例</span><span class="sxs-lookup"><span data-stu-id="0d3aa-113">EXAMPLES</span></span>

### <span data-ttu-id="0d3aa-114">範例1</span><span class="sxs-lookup"><span data-stu-id="0d3aa-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="0d3aa-115">這個範例會在指定的工作區中取得所有 **AlertRuleTemplates** ，然後將它儲存在 $AlertRuleTemplates 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="0d3aa-116">範例2</span><span class="sxs-lookup"><span data-stu-id="0d3aa-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="0d3aa-117">這個範例會在指定的工作區中取得 **AlertRuleTemplate** ，然後將其儲存在 $AlertRuleTemplate 變數中。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="0d3aa-118">參數</span><span class="sxs-lookup"><span data-stu-id="0d3aa-118">PARAMETERS</span></span>

### <span data-ttu-id="0d3aa-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="0d3aa-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="0d3aa-120">範本警示規則識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-120">Template Alert Rule Id.</span></span>

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

### <span data-ttu-id="0d3aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d3aa-121">-DefaultProfile</span></span>
<span data-ttu-id="0d3aa-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d3aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d3aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d3aa-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-124">Resource group name.</span></span>

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

### <span data-ttu-id="0d3aa-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d3aa-125">-ResourceId</span></span>
<span data-ttu-id="0d3aa-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-126">Resource Id.</span></span>

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

### <span data-ttu-id="0d3aa-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0d3aa-127">-WorkspaceName</span></span>
<span data-ttu-id="0d3aa-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-128">Workspace Name.</span></span>

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

### <span data-ttu-id="0d3aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d3aa-129">CommonParameters</span></span>
<span data-ttu-id="0d3aa-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d3aa-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d3aa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d3aa-132">輸入</span><span class="sxs-lookup"><span data-stu-id="0d3aa-132">INPUTS</span></span>

### <span data-ttu-id="0d3aa-133">System.object</span><span class="sxs-lookup"><span data-stu-id="0d3aa-133">System.String</span></span>
## <span data-ttu-id="0d3aa-134">輸出</span><span class="sxs-lookup"><span data-stu-id="0d3aa-134">OUTPUTS</span></span>

### <span data-ttu-id="0d3aa-135">SecurityInsights AlertRuleTemplates. PSSentinelAlertRuleTemplate （）</span><span class="sxs-lookup"><span data-stu-id="0d3aa-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="0d3aa-136">筆記</span><span class="sxs-lookup"><span data-stu-id="0d3aa-136">NOTES</span></span>

## <span data-ttu-id="0d3aa-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d3aa-137">RELATED LINKS</span></span>
