---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: 7a1cec73706d1ed799966bc3d97da06867139c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909637"
---
# <span data-ttu-id="d1f7c-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d1f7c-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="d1f7c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d1f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f7c-103">獲得保護容器的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="d1f7c-104">語法</span><span class="sxs-lookup"><span data-stu-id="d1f7c-104">SYNTAX</span></span>

### <span data-ttu-id="d1f7c-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="d1f7c-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1f7c-106">獲取</span><span class="sxs-lookup"><span data-stu-id="d1f7c-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d1f7c-107">清單</span><span class="sxs-lookup"><span data-stu-id="d1f7c-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d1f7c-108">描述</span><span class="sxs-lookup"><span data-stu-id="d1f7c-108">DESCRIPTION</span></span>
<span data-ttu-id="d1f7c-109">獲得保護容器的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="d1f7c-110">例子</span><span class="sxs-lookup"><span data-stu-id="d1f7c-110">EXAMPLES</span></span>

### <span data-ttu-id="d1f7c-111">範例 1：列出庫和布料中所有的保護容器</span><span class="sxs-lookup"><span data-stu-id="d1f7c-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="d1f7c-112">全部列出。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-112">Lists all.</span></span>

### <span data-ttu-id="d1f7c-113">範例 2：取得特定容器</span><span class="sxs-lookup"><span data-stu-id="d1f7c-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="d1f7c-114">獲得特定專案。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-114">Gets a specific one.</span></span>

## <span data-ttu-id="d1f7c-115">參數</span><span class="sxs-lookup"><span data-stu-id="d1f7c-115">PARAMETERS</span></span>

### <span data-ttu-id="d1f7c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f7c-116">-DefaultProfile</span></span>
<span data-ttu-id="d1f7c-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f7c-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="d1f7c-118">-FabricName</span></span>
<span data-ttu-id="d1f7c-119">布料名稱。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-119">Fabric name.</span></span>

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

### <span data-ttu-id="d1f7c-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="d1f7c-120">-ProtectionContainerName</span></span>
<span data-ttu-id="d1f7c-121">保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-121">Protection container name.</span></span>

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

### <span data-ttu-id="d1f7c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f7c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d1f7c-123">復原服務庫存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="d1f7c-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d1f7c-124">-ResourceName</span></span>
<span data-ttu-id="d1f7c-125">復原服務庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="d1f7c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1f7c-126">-SubscriptionId</span></span>
<span data-ttu-id="d1f7c-127">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="d1f7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f7c-128">CommonParameters</span></span>
<span data-ttu-id="d1f7c-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d1f7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f7c-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1f7c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f7c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d1f7c-131">INPUTS</span></span>

## <span data-ttu-id="d1f7c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d1f7c-132">OUTPUTS</span></span>

### <span data-ttu-id="d1f7c-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d1f7c-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="d1f7c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d1f7c-134">NOTES</span></span>

<span data-ttu-id="d1f7c-135">別名</span><span class="sxs-lookup"><span data-stu-id="d1f7c-135">ALIASES</span></span>

## <span data-ttu-id="d1f7c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1f7c-136">RELATED LINKS</span></span>

