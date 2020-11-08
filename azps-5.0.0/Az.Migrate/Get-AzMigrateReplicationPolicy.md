---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141514"
---
# <span data-ttu-id="8d2f6-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="8d2f6-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="8d2f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2f6-103">取得複製原則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="8d2f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d2f6-104">SYNTAX</span></span>

### <span data-ttu-id="8d2f6-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="8d2f6-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8d2f6-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8d2f6-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8d2f6-107">說明</span><span class="sxs-lookup"><span data-stu-id="8d2f6-107">DESCRIPTION</span></span>
<span data-ttu-id="8d2f6-108">取得複製原則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="8d2f6-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d2f6-109">EXAMPLES</span></span>

### <span data-ttu-id="8d2f6-110">範例1：取得電子倉庫中的所有原則</span><span class="sxs-lookup"><span data-stu-id="8d2f6-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="8d2f6-111">取得所有原則。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-111">Get all policies.</span></span>

### <span data-ttu-id="8d2f6-112">範例2：取得特定原則</span><span class="sxs-lookup"><span data-stu-id="8d2f6-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="8d2f6-113">取得特定專案。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-113">Get a specific one.</span></span>

## <span data-ttu-id="8d2f6-114">參數</span><span class="sxs-lookup"><span data-stu-id="8d2f6-114">PARAMETERS</span></span>

### <span data-ttu-id="8d2f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d2f6-115">-DefaultProfile</span></span>
<span data-ttu-id="8d2f6-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d2f6-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="8d2f6-117">-PolicyName</span></span>
<span data-ttu-id="8d2f6-118">複製原則名稱。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-118">Replication policy name.</span></span>

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

### <span data-ttu-id="8d2f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d2f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d2f6-120">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="8d2f6-121">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="8d2f6-121">-ResourceName</span></span>
<span data-ttu-id="8d2f6-122">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="8d2f6-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d2f6-123">-SubscriptionId</span></span>
<span data-ttu-id="8d2f6-124">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-124">The subscription Id.</span></span>

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

### <span data-ttu-id="8d2f6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2f6-125">CommonParameters</span></span>
<span data-ttu-id="8d2f6-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2f6-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2f6-128">輸入</span><span class="sxs-lookup"><span data-stu-id="8d2f6-128">INPUTS</span></span>

## <span data-ttu-id="8d2f6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8d2f6-129">OUTPUTS</span></span>

### <span data-ttu-id="8d2f6-130">IPolicy 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="8d2f6-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="8d2f6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8d2f6-131">NOTES</span></span>

<span data-ttu-id="8d2f6-132">別名</span><span class="sxs-lookup"><span data-stu-id="8d2f6-132">ALIASES</span></span>

## <span data-ttu-id="8d2f6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d2f6-133">RELATED LINKS</span></span>

