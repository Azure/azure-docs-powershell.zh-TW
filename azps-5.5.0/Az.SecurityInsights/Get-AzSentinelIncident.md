---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130783"
---
# <span data-ttu-id="6976d-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="6976d-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="6976d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6976d-102">SYNOPSIS</span></span>
<span data-ttu-id="6976d-103">取得事件。</span><span class="sxs-lookup"><span data-stu-id="6976d-103">Get an Incident.</span></span>

## <span data-ttu-id="6976d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6976d-104">SYNTAX</span></span>

### <span data-ttu-id="6976d-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="6976d-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6976d-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="6976d-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6976d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6976d-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6976d-108">說明</span><span class="sxs-lookup"><span data-stu-id="6976d-108">DESCRIPTION</span></span>
<span data-ttu-id="6976d-109">**AzSentinelIncident** Cmdlet 會從指定的工作區取得事件。</span><span class="sxs-lookup"><span data-stu-id="6976d-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="6976d-110">如果您指定 *IncidentId* 參數，則會傳回單一 **事件** 物件。</span><span class="sxs-lookup"><span data-stu-id="6976d-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="6976d-111">如果您沒有指定 *IncidentId* 參數，則會傳回包含指定工作區中所有事件的陣列。</span><span class="sxs-lookup"><span data-stu-id="6976d-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="6976d-112">您可以使用 **incident** 物件來更新事件，例如，您可以新增記錄給 **事件**。</span><span class="sxs-lookup"><span data-stu-id="6976d-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="6976d-113">示例</span><span class="sxs-lookup"><span data-stu-id="6976d-113">EXAMPLES</span></span>

### <span data-ttu-id="6976d-114">範例1</span><span class="sxs-lookup"><span data-stu-id="6976d-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="6976d-115">這個範例會取得指定工作區中的所有 **事件** ，然後將其儲存在 $Incidents 變數中。</span><span class="sxs-lookup"><span data-stu-id="6976d-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="6976d-116">範例2</span><span class="sxs-lookup"><span data-stu-id="6976d-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="6976d-117">這個範例會在指定的工作區中取得 **事件** ，然後將它儲存在 $Incident 變數中。</span><span class="sxs-lookup"><span data-stu-id="6976d-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="6976d-118">參數</span><span class="sxs-lookup"><span data-stu-id="6976d-118">PARAMETERS</span></span>

### <span data-ttu-id="6976d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6976d-119">-DefaultProfile</span></span>
<span data-ttu-id="6976d-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6976d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6976d-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="6976d-121">-IncidentId</span></span>
<span data-ttu-id="6976d-122">事件 Id。</span><span class="sxs-lookup"><span data-stu-id="6976d-122">Incident Id.</span></span>

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

### <span data-ttu-id="6976d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6976d-123">-ResourceGroupName</span></span>
<span data-ttu-id="6976d-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6976d-124">Resource group name.</span></span>

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

### <span data-ttu-id="6976d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6976d-125">-ResourceId</span></span>
<span data-ttu-id="6976d-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="6976d-126">Resource Id.</span></span>

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

### <span data-ttu-id="6976d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6976d-127">-WorkspaceName</span></span>
<span data-ttu-id="6976d-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="6976d-128">Workspace Name.</span></span>

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

### <span data-ttu-id="6976d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6976d-129">CommonParameters</span></span>
<span data-ttu-id="6976d-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6976d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6976d-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6976d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6976d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6976d-132">INPUTS</span></span>

### <span data-ttu-id="6976d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="6976d-133">System.String</span></span>
## <span data-ttu-id="6976d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6976d-134">OUTPUTS</span></span>

### <span data-ttu-id="6976d-135">PSSentinelIncident （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="6976d-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="6976d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6976d-136">NOTES</span></span>

## <span data-ttu-id="6976d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="6976d-137">RELATED LINKS</span></span>
