---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448568"
---
# <span data-ttu-id="38566-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="38566-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="38566-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38566-102">SYNOPSIS</span></span>
<span data-ttu-id="38566-103">取得事件。</span><span class="sxs-lookup"><span data-stu-id="38566-103">Get an Incident.</span></span>

## <span data-ttu-id="38566-104">句法</span><span class="sxs-lookup"><span data-stu-id="38566-104">SYNTAX</span></span>

### <span data-ttu-id="38566-105">WorkspaceScope (預設) </span><span class="sxs-lookup"><span data-stu-id="38566-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38566-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="38566-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38566-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38566-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38566-108">說明</span><span class="sxs-lookup"><span data-stu-id="38566-108">DESCRIPTION</span></span>
<span data-ttu-id="38566-109">**AzSentinelIncident** Cmdlet 會從指定的工作區取得事件。</span><span class="sxs-lookup"><span data-stu-id="38566-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="38566-110">如果您指定 *IncidentId* 參數，則會傳回單一 **事件** 物件。</span><span class="sxs-lookup"><span data-stu-id="38566-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="38566-111">如果您沒有指定 *IncidentId* 參數，則會傳回包含指定工作區中所有事件的陣列。</span><span class="sxs-lookup"><span data-stu-id="38566-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="38566-112">您可以使用 **incident** 物件來更新事件，例如，您可以新增記錄給 **事件**。</span><span class="sxs-lookup"><span data-stu-id="38566-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="38566-113">示例</span><span class="sxs-lookup"><span data-stu-id="38566-113">EXAMPLES</span></span>

### <span data-ttu-id="38566-114">範例1</span><span class="sxs-lookup"><span data-stu-id="38566-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="38566-115">這個範例會取得指定工作區中的所有 **事件** ，然後將其儲存在 $Incidents 變數中。</span><span class="sxs-lookup"><span data-stu-id="38566-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="38566-116">範例2</span><span class="sxs-lookup"><span data-stu-id="38566-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="38566-117">這個範例會在指定的工作區中取得 **事件** ，然後將它儲存在 $Incident 變數中。</span><span class="sxs-lookup"><span data-stu-id="38566-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="38566-118">參數</span><span class="sxs-lookup"><span data-stu-id="38566-118">PARAMETERS</span></span>

### <span data-ttu-id="38566-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38566-119">-DefaultProfile</span></span>
<span data-ttu-id="38566-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38566-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38566-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="38566-121">-IncidentId</span></span>
<span data-ttu-id="38566-122">事件 Id。</span><span class="sxs-lookup"><span data-stu-id="38566-122">Incident Id.</span></span>

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

### <span data-ttu-id="38566-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38566-123">-ResourceGroupName</span></span>
<span data-ttu-id="38566-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="38566-124">Resource group name.</span></span>

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

### <span data-ttu-id="38566-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38566-125">-ResourceId</span></span>
<span data-ttu-id="38566-126">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="38566-126">Resource Id.</span></span>

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

### <span data-ttu-id="38566-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38566-127">-WorkspaceName</span></span>
<span data-ttu-id="38566-128">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="38566-128">Workspace Name.</span></span>

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

### <span data-ttu-id="38566-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38566-129">CommonParameters</span></span>
<span data-ttu-id="38566-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38566-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38566-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="38566-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38566-132">輸入</span><span class="sxs-lookup"><span data-stu-id="38566-132">INPUTS</span></span>

### <span data-ttu-id="38566-133">System.object</span><span class="sxs-lookup"><span data-stu-id="38566-133">System.String</span></span>
## <span data-ttu-id="38566-134">輸出</span><span class="sxs-lookup"><span data-stu-id="38566-134">OUTPUTS</span></span>

### <span data-ttu-id="38566-135">PSSentinelIncident （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="38566-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="38566-136">筆記</span><span class="sxs-lookup"><span data-stu-id="38566-136">NOTES</span></span>

## <span data-ttu-id="38566-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="38566-137">RELATED LINKS</span></span>
