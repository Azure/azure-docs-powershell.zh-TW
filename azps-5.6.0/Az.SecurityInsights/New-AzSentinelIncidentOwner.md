---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: b8981d40f3412dd77ca120cd80d29fb160915e8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901662"
---
# <span data-ttu-id="cc20f-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="cc20f-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="cc20f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc20f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc20f-103">建立事件擁有者物件以更新事件擁有者。</span><span class="sxs-lookup"><span data-stu-id="cc20f-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="cc20f-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc20f-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc20f-105">描述</span><span class="sxs-lookup"><span data-stu-id="cc20f-105">DESCRIPTION</span></span>
<span data-ttu-id="cc20f-106">**New-AzSentinelIncident Ownerer Cmdlet** 在記憶體中建立事件擁有者物件，以更新事件。</span><span class="sxs-lookup"><span data-stu-id="cc20f-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="cc20f-107">例子</span><span class="sxs-lookup"><span data-stu-id="cc20f-107">EXAMPLES</span></span>

### <span data-ttu-id="cc20f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="cc20f-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="cc20f-109">此範例會建立 **事件擁有者，並** 更新事件給新的擁有者。</span><span class="sxs-lookup"><span data-stu-id="cc20f-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="cc20f-110">參數</span><span class="sxs-lookup"><span data-stu-id="cc20f-110">PARAMETERS</span></span>

### <span data-ttu-id="cc20f-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="cc20f-111">-AssignedTo</span></span>
<span data-ttu-id="cc20f-112">事件擁有者 - 指派給</span><span class="sxs-lookup"><span data-stu-id="cc20f-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="cc20f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc20f-113">-DefaultProfile</span></span>
<span data-ttu-id="cc20f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc20f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc20f-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="cc20f-115">-Email</span></span>
<span data-ttu-id="cc20f-116">事件擁有者 - 電子郵件</span><span class="sxs-lookup"><span data-stu-id="cc20f-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="cc20f-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc20f-117">-ObjectId</span></span>
<span data-ttu-id="cc20f-118">事件擁有者 - ObjectId</span><span class="sxs-lookup"><span data-stu-id="cc20f-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="cc20f-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="cc20f-119">-UserPrincipalName</span></span>
<span data-ttu-id="cc20f-120">事件擁有者 - 使用者主體名稱</span><span class="sxs-lookup"><span data-stu-id="cc20f-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="cc20f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc20f-121">CommonParameters</span></span>
<span data-ttu-id="cc20f-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc20f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc20f-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc20f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc20f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="cc20f-124">INPUTS</span></span>

### <span data-ttu-id="cc20f-125">沒有</span><span class="sxs-lookup"><span data-stu-id="cc20f-125">None</span></span>
## <span data-ttu-id="cc20f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="cc20f-126">OUTPUTS</span></span>

### <span data-ttu-id="cc20f-127">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="cc20f-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="cc20f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="cc20f-128">NOTES</span></span>

## <span data-ttu-id="cc20f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc20f-129">RELATED LINKS</span></span>
