---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: aa3cddd70ad1c17df9415499d0b33fa33e68f7f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448535"
---
# <span data-ttu-id="b1b17-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="b1b17-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="b1b17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1b17-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b17-103">建立事件擁有者物件來更新事件擁有者。</span><span class="sxs-lookup"><span data-stu-id="b1b17-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="b1b17-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1b17-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b17-105">說明</span><span class="sxs-lookup"><span data-stu-id="b1b17-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b17-106">**AzSentinelIncidentOwner** Cmdlet 會在記憶體中建立事件擁有者物件來更新事件。</span><span class="sxs-lookup"><span data-stu-id="b1b17-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="b1b17-107">示例</span><span class="sxs-lookup"><span data-stu-id="b1b17-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b17-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b1b17-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="b1b17-109">這個範例會建立 **IncidentOwner** ，並將事件更新給新的擁有者。</span><span class="sxs-lookup"><span data-stu-id="b1b17-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="b1b17-110">參數</span><span class="sxs-lookup"><span data-stu-id="b1b17-110">PARAMETERS</span></span>

### <span data-ttu-id="b1b17-111">-分配給</span><span class="sxs-lookup"><span data-stu-id="b1b17-111">-AssignedTo</span></span>
<span data-ttu-id="b1b17-112">事件擁有者-指派給</span><span class="sxs-lookup"><span data-stu-id="b1b17-112">Incident Owner - Assigned To</span></span>

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

### <span data-ttu-id="b1b17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b17-113">-DefaultProfile</span></span>
<span data-ttu-id="b1b17-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1b17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b17-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="b1b17-115">-Email</span></span>
<span data-ttu-id="b1b17-116">事件擁有者-電子郵件</span><span class="sxs-lookup"><span data-stu-id="b1b17-116">Incident Owner - Email</span></span>

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

### <span data-ttu-id="b1b17-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b1b17-117">-ObjectId</span></span>
<span data-ttu-id="b1b17-118">事件擁有者-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b1b17-118">Incident Owner - ObjectId</span></span>

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

### <span data-ttu-id="b1b17-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b1b17-119">-UserPrincipalName</span></span>
<span data-ttu-id="b1b17-120">事件擁有者-使用者主要名稱</span><span class="sxs-lookup"><span data-stu-id="b1b17-120">Incident Owner - User Principal Name</span></span>

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

### <span data-ttu-id="b1b17-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b17-121">CommonParameters</span></span>
<span data-ttu-id="b1b17-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1b17-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b17-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b1b17-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b17-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b1b17-124">INPUTS</span></span>

### <span data-ttu-id="b1b17-125">所有</span><span class="sxs-lookup"><span data-stu-id="b1b17-125">None</span></span>
## <span data-ttu-id="b1b17-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b1b17-126">OUTPUTS</span></span>

### <span data-ttu-id="b1b17-127">PSSentinelIncident （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="b1b17-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="b1b17-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b1b17-128">NOTES</span></span>

## <span data-ttu-id="b1b17-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1b17-129">RELATED LINKS</span></span>
