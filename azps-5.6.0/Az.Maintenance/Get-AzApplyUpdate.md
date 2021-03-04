---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: c6ebe985d0242e626d0a417d4af3a60388cbc776
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916525"
---
# <span data-ttu-id="e3bff-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="e3bff-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="e3bff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3bff-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bff-103">追蹤資源維護更新</span><span class="sxs-lookup"><span data-stu-id="e3bff-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="e3bff-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3bff-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3bff-105">描述</span><span class="sxs-lookup"><span data-stu-id="e3bff-105">DESCRIPTION</span></span>
<span data-ttu-id="e3bff-106">追蹤資源維護更新</span><span class="sxs-lookup"><span data-stu-id="e3bff-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="e3bff-107">例子</span><span class="sxs-lookup"><span data-stu-id="e3bff-107">EXAMPLES</span></span>

### <span data-ttu-id="e3bff-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e3bff-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="e3bff-109">追蹤資源維護更新</span><span class="sxs-lookup"><span data-stu-id="e3bff-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="e3bff-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3bff-110">PARAMETERS</span></span>

### <span data-ttu-id="e3bff-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="e3bff-111">-ApplyUpdateName</span></span>
<span data-ttu-id="e3bff-112">已申請更新資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e3bff-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bff-113">-DefaultProfile</span></span>
<span data-ttu-id="e3bff-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3bff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3bff-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="e3bff-115">-ProviderName</span></span>
<span data-ttu-id="e3bff-116">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="e3bff-116">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3bff-117">-ResourceGroupName</span></span>
<span data-ttu-id="e3bff-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e3bff-118">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bff-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e3bff-119">-ResourceName</span></span>
<span data-ttu-id="e3bff-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e3bff-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bff-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="e3bff-121">-ResourceParentName</span></span>
<span data-ttu-id="e3bff-122">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e3bff-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bff-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="e3bff-123">-ResourceParentType</span></span>
<span data-ttu-id="e3bff-124">父資源類型。</span><span class="sxs-lookup"><span data-stu-id="e3bff-124">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bff-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e3bff-125">-ResourceType</span></span>
<span data-ttu-id="e3bff-126">資源類型。</span><span class="sxs-lookup"><span data-stu-id="e3bff-126">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bff-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bff-127">CommonParameters</span></span>
<span data-ttu-id="e3bff-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3bff-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bff-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3bff-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bff-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e3bff-130">INPUTS</span></span>

### <span data-ttu-id="e3bff-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e3bff-131">System.String</span></span>

## <span data-ttu-id="e3bff-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e3bff-132">OUTPUTS</span></span>

### <span data-ttu-id="e3bff-133">Microsoft.Azure.Commands.Maintenance.models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="e3bff-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="e3bff-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e3bff-134">NOTES</span></span>

## <span data-ttu-id="e3bff-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3bff-135">RELATED LINKS</span></span>
