---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138799"
---
# <span data-ttu-id="05857-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="05857-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="05857-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05857-102">SYNOPSIS</span></span>
<span data-ttu-id="05857-103">取得資源的擱置中維護更新。</span><span class="sxs-lookup"><span data-stu-id="05857-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="05857-104">句法</span><span class="sxs-lookup"><span data-stu-id="05857-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05857-105">說明</span><span class="sxs-lookup"><span data-stu-id="05857-105">DESCRIPTION</span></span>
<span data-ttu-id="05857-106">取得資源的擱置中維護更新。</span><span class="sxs-lookup"><span data-stu-id="05857-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="05857-107">示例</span><span class="sxs-lookup"><span data-stu-id="05857-107">EXAMPLES</span></span>

### <span data-ttu-id="05857-108">範例1</span><span class="sxs-lookup"><span data-stu-id="05857-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="05857-109">取得資源的擱置中維護更新。</span><span class="sxs-lookup"><span data-stu-id="05857-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="05857-110">參數</span><span class="sxs-lookup"><span data-stu-id="05857-110">PARAMETERS</span></span>

### <span data-ttu-id="05857-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05857-111">-DefaultProfile</span></span>
<span data-ttu-id="05857-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="05857-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05857-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="05857-113">-ProviderName</span></span>
<span data-ttu-id="05857-114">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="05857-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="05857-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05857-115">-ResourceGroupName</span></span>
<span data-ttu-id="05857-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="05857-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="05857-117">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="05857-117">-ResourceName</span></span>
<span data-ttu-id="05857-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="05857-118">The resource name.</span></span>

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

### <span data-ttu-id="05857-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="05857-119">-ResourceParentName</span></span>
<span data-ttu-id="05857-120">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="05857-120">The parent resource name.</span></span>

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

### <span data-ttu-id="05857-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="05857-121">-ResourceParentType</span></span>
<span data-ttu-id="05857-122">父級資源類型。</span><span class="sxs-lookup"><span data-stu-id="05857-122">The parent resource type.</span></span>

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

### <span data-ttu-id="05857-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="05857-123">-ResourceType</span></span>
<span data-ttu-id="05857-124">資源類型。</span><span class="sxs-lookup"><span data-stu-id="05857-124">The resource type.</span></span>

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

### <span data-ttu-id="05857-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05857-125">CommonParameters</span></span>
<span data-ttu-id="05857-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05857-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05857-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="05857-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05857-128">輸入</span><span class="sxs-lookup"><span data-stu-id="05857-128">INPUTS</span></span>

### <span data-ttu-id="05857-129">System.object</span><span class="sxs-lookup"><span data-stu-id="05857-129">System.String</span></span>

## <span data-ttu-id="05857-130">輸出</span><span class="sxs-lookup"><span data-stu-id="05857-130">OUTPUTS</span></span>

### <span data-ttu-id="05857-131">[Microsoft Azure. 管理]。模型. 更新</span><span class="sxs-lookup"><span data-stu-id="05857-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="05857-132">筆記</span><span class="sxs-lookup"><span data-stu-id="05857-132">NOTES</span></span>

## <span data-ttu-id="05857-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="05857-133">RELATED LINKS</span></span>