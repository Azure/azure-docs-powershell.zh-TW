---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: 669e0961327b6419e86f288ec71bffa6cdc69b4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910606"
---
# <span data-ttu-id="d2451-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d2451-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="d2451-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d2451-102">SYNOPSIS</span></span>
<span data-ttu-id="d2451-103">取得事件。</span><span class="sxs-lookup"><span data-stu-id="d2451-103">Get an Incident.</span></span>

## <span data-ttu-id="d2451-104">語法</span><span class="sxs-lookup"><span data-stu-id="d2451-104">SYNTAX</span></span>

### <span data-ttu-id="d2451-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="d2451-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2451-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="d2451-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2451-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2451-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2451-108">描述</span><span class="sxs-lookup"><span data-stu-id="d2451-108">DESCRIPTION</span></span>
<span data-ttu-id="d2451-109">**Get-AzSentinelIncident** Cmdlet 會從指定的工作區取得事件。</span><span class="sxs-lookup"><span data-stu-id="d2451-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="d2451-110">如果您指定 *IncidentId* 參數，會返回單 **一事件** 物件。</span><span class="sxs-lookup"><span data-stu-id="d2451-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="d2451-111">如果您未指定 *IncidentId* 參數，則包含指定工作區中所有事件的陣列會返回。</span><span class="sxs-lookup"><span data-stu-id="d2451-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="d2451-112">您可以使用事件 **物件** 來更新事件，例如，您可以新增事件 **記事**。</span><span class="sxs-lookup"><span data-stu-id="d2451-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="d2451-113">例子</span><span class="sxs-lookup"><span data-stu-id="d2451-113">EXAMPLES</span></span>

### <span data-ttu-id="d2451-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="d2451-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="d2451-115">此範例會獲得指定工作區中所有的事件，然後將它儲存在$Incidents變數。</span><span class="sxs-lookup"><span data-stu-id="d2451-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="d2451-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="d2451-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="d2451-117">此範例 **會獲得指定** 工作區中的事件，然後將它儲存在$Incident變數。</span><span class="sxs-lookup"><span data-stu-id="d2451-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="d2451-118">參數</span><span class="sxs-lookup"><span data-stu-id="d2451-118">PARAMETERS</span></span>

### <span data-ttu-id="d2451-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2451-119">-DefaultProfile</span></span>
<span data-ttu-id="d2451-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2451-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2451-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="d2451-121">-IncidentId</span></span>
<span data-ttu-id="d2451-122">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2451-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2451-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2451-123">-ResourceGroupName</span></span>
<span data-ttu-id="d2451-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d2451-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2451-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2451-125">-ResourceId</span></span>
<span data-ttu-id="d2451-126">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2451-126">Resource Id.</span></span>

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

### <span data-ttu-id="d2451-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d2451-127">-WorkspaceName</span></span>
<span data-ttu-id="d2451-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d2451-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2451-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2451-129">CommonParameters</span></span>
<span data-ttu-id="d2451-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d2451-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2451-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2451-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2451-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d2451-132">INPUTS</span></span>

### <span data-ttu-id="d2451-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d2451-133">System.String</span></span>
## <span data-ttu-id="d2451-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d2451-134">OUTPUTS</span></span>

### <span data-ttu-id="d2451-135">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d2451-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="d2451-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d2451-136">NOTES</span></span>

## <span data-ttu-id="d2451-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2451-137">RELATED LINKS</span></span>
