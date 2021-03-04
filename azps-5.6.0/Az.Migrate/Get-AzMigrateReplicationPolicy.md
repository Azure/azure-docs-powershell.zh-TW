---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 261d7467d67708380f86c8df061fdda02eb095c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909653"
---
# <span data-ttu-id="93552-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="93552-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="93552-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93552-102">SYNOPSIS</span></span>
<span data-ttu-id="93552-103">獲得複寫原則的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="93552-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="93552-104">語法</span><span class="sxs-lookup"><span data-stu-id="93552-104">SYNTAX</span></span>

### <span data-ttu-id="93552-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="93552-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93552-106">獲取</span><span class="sxs-lookup"><span data-stu-id="93552-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="93552-107">描述</span><span class="sxs-lookup"><span data-stu-id="93552-107">DESCRIPTION</span></span>
<span data-ttu-id="93552-108">獲得複寫原則的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="93552-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="93552-109">例子</span><span class="sxs-lookup"><span data-stu-id="93552-109">EXAMPLES</span></span>

### <span data-ttu-id="93552-110">範例 1：取得資料庫中的所有策略</span><span class="sxs-lookup"><span data-stu-id="93552-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="93552-111">取得所有政策。</span><span class="sxs-lookup"><span data-stu-id="93552-111">Get all policies.</span></span>

### <span data-ttu-id="93552-112">範例 2：取得特定政策</span><span class="sxs-lookup"><span data-stu-id="93552-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="93552-113">取得特定專案。</span><span class="sxs-lookup"><span data-stu-id="93552-113">Get a specific one.</span></span>

## <span data-ttu-id="93552-114">參數</span><span class="sxs-lookup"><span data-stu-id="93552-114">PARAMETERS</span></span>

### <span data-ttu-id="93552-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93552-115">-DefaultProfile</span></span>
<span data-ttu-id="93552-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="93552-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93552-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="93552-117">-PolicyName</span></span>
<span data-ttu-id="93552-118">複寫原則名稱。</span><span class="sxs-lookup"><span data-stu-id="93552-118">Replication policy name.</span></span>

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

### <span data-ttu-id="93552-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93552-119">-ResourceGroupName</span></span>
<span data-ttu-id="93552-120">復原服務庫存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93552-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="93552-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="93552-121">-ResourceName</span></span>
<span data-ttu-id="93552-122">復原服務庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="93552-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="93552-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93552-123">-SubscriptionId</span></span>
<span data-ttu-id="93552-124">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="93552-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="93552-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93552-125">CommonParameters</span></span>
<span data-ttu-id="93552-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93552-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93552-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93552-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93552-128">輸入</span><span class="sxs-lookup"><span data-stu-id="93552-128">INPUTS</span></span>

## <span data-ttu-id="93552-129">輸出</span><span class="sxs-lookup"><span data-stu-id="93552-129">OUTPUTS</span></span>

### <span data-ttu-id="93552-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="93552-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="93552-131">筆記</span><span class="sxs-lookup"><span data-stu-id="93552-131">NOTES</span></span>

<span data-ttu-id="93552-132">別名</span><span class="sxs-lookup"><span data-stu-id="93552-132">ALIASES</span></span>

## <span data-ttu-id="93552-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="93552-133">RELATED LINKS</span></span>

