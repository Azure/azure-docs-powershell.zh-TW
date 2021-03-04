---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 87fa8d8653d0409eb4b322e0ce21dbc9c8cfa668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909633"
---
# <span data-ttu-id="e65c7-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e65c7-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="e65c7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e65c7-102">SYNOPSIS</span></span>
<span data-ttu-id="e65c7-103">獲得保護容器地圖的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e65c7-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="e65c7-104">語法</span><span class="sxs-lookup"><span data-stu-id="e65c7-104">SYNTAX</span></span>

### <span data-ttu-id="e65c7-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="e65c7-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e65c7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e65c7-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e65c7-107">清單</span><span class="sxs-lookup"><span data-stu-id="e65c7-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e65c7-108">描述</span><span class="sxs-lookup"><span data-stu-id="e65c7-108">DESCRIPTION</span></span>
<span data-ttu-id="e65c7-109">獲得保護容器地圖的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e65c7-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="e65c7-110">例子</span><span class="sxs-lookup"><span data-stu-id="e65c7-110">EXAMPLES</span></span>

### <span data-ttu-id="e65c7-111">範例 1：取得特定地圖</span><span class="sxs-lookup"><span data-stu-id="e65c7-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="e65c7-112">取得地圖詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e65c7-112">Get a mapping detail.</span></span>

## <span data-ttu-id="e65c7-113">參數</span><span class="sxs-lookup"><span data-stu-id="e65c7-113">PARAMETERS</span></span>

### <span data-ttu-id="e65c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e65c7-114">-DefaultProfile</span></span>
<span data-ttu-id="e65c7-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e65c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65c7-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="e65c7-116">-FabricName</span></span>
<span data-ttu-id="e65c7-117">布料名稱。</span><span class="sxs-lookup"><span data-stu-id="e65c7-117">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65c7-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="e65c7-118">-MappingName</span></span>
<span data-ttu-id="e65c7-119">保護容器的映射名稱。</span><span class="sxs-lookup"><span data-stu-id="e65c7-119">Protection Container mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65c7-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="e65c7-120">-ProtectionContainerName</span></span>
<span data-ttu-id="e65c7-121">保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="e65c7-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e65c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="e65c7-123">復原服務庫存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e65c7-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="e65c7-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e65c7-124">-ResourceName</span></span>
<span data-ttu-id="e65c7-125">復原服務庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e65c7-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="e65c7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e65c7-126">-SubscriptionId</span></span>
<span data-ttu-id="e65c7-127">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="e65c7-127">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e65c7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e65c7-128">CommonParameters</span></span>
<span data-ttu-id="e65c7-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e65c7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e65c7-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e65c7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e65c7-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e65c7-131">INPUTS</span></span>

## <span data-ttu-id="e65c7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e65c7-132">OUTPUTS</span></span>

### <span data-ttu-id="e65c7-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="e65c7-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="e65c7-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e65c7-134">NOTES</span></span>

<span data-ttu-id="e65c7-135">別名</span><span class="sxs-lookup"><span data-stu-id="e65c7-135">ALIASES</span></span>

## <span data-ttu-id="e65c7-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e65c7-136">RELATED LINKS</span></span>

