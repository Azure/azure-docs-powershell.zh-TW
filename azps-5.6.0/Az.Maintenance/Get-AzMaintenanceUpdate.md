---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: dd2fb366e4e15a2c2b21c53c5bddb32bc99939ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904054"
---
# <span data-ttu-id="9a0df-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="9a0df-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="9a0df-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a0df-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0df-103">取得資源的擱置維護更新。</span><span class="sxs-lookup"><span data-stu-id="9a0df-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="9a0df-104">語法</span><span class="sxs-lookup"><span data-stu-id="9a0df-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a0df-105">描述</span><span class="sxs-lookup"><span data-stu-id="9a0df-105">DESCRIPTION</span></span>
<span data-ttu-id="9a0df-106">取得資源的擱置維護更新。</span><span class="sxs-lookup"><span data-stu-id="9a0df-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="9a0df-107">例子</span><span class="sxs-lookup"><span data-stu-id="9a0df-107">EXAMPLES</span></span>

### <span data-ttu-id="9a0df-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9a0df-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="9a0df-109">取得資源的擱置維護更新。</span><span class="sxs-lookup"><span data-stu-id="9a0df-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="9a0df-110">參數</span><span class="sxs-lookup"><span data-stu-id="9a0df-110">PARAMETERS</span></span>

### <span data-ttu-id="9a0df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0df-111">-DefaultProfile</span></span>
<span data-ttu-id="9a0df-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a0df-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a0df-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="9a0df-113">-ProviderName</span></span>
<span data-ttu-id="9a0df-114">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="9a0df-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="9a0df-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0df-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a0df-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9a0df-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="9a0df-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9a0df-117">-ResourceName</span></span>
<span data-ttu-id="9a0df-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9a0df-118">The resource name.</span></span>

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

### <span data-ttu-id="9a0df-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="9a0df-119">-ResourceParentName</span></span>
<span data-ttu-id="9a0df-120">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9a0df-120">The parent resource name.</span></span>

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

### <span data-ttu-id="9a0df-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="9a0df-121">-ResourceParentType</span></span>
<span data-ttu-id="9a0df-122">父資源類型。</span><span class="sxs-lookup"><span data-stu-id="9a0df-122">The parent resource type.</span></span>

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

### <span data-ttu-id="9a0df-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9a0df-123">-ResourceType</span></span>
<span data-ttu-id="9a0df-124">資源類型。</span><span class="sxs-lookup"><span data-stu-id="9a0df-124">The resource type.</span></span>

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

### <span data-ttu-id="9a0df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0df-125">CommonParameters</span></span>
<span data-ttu-id="9a0df-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a0df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0df-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a0df-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0df-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9a0df-128">INPUTS</span></span>

### <span data-ttu-id="9a0df-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9a0df-129">System.String</span></span>

## <span data-ttu-id="9a0df-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9a0df-130">OUTPUTS</span></span>

### <span data-ttu-id="9a0df-131">Microsoft.Azure.management.Maintenance.models.Update</span><span class="sxs-lookup"><span data-stu-id="9a0df-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="9a0df-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9a0df-132">NOTES</span></span>

## <span data-ttu-id="9a0df-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a0df-133">RELATED LINKS</span></span>
