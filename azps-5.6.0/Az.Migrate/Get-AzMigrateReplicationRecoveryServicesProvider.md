---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: 2e890de56cdcf0ac2b17853b10629a58fce6c3b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909630"
---
# <span data-ttu-id="888ea-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="888ea-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="888ea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="888ea-102">SYNOPSIS</span></span>
<span data-ttu-id="888ea-103">獲得已註冊的復原服務提供者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="888ea-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="888ea-104">語法</span><span class="sxs-lookup"><span data-stu-id="888ea-104">SYNTAX</span></span>

### <span data-ttu-id="888ea-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="888ea-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="888ea-106">獲取</span><span class="sxs-lookup"><span data-stu-id="888ea-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="888ea-107">描述</span><span class="sxs-lookup"><span data-stu-id="888ea-107">DESCRIPTION</span></span>
<span data-ttu-id="888ea-108">獲得已註冊的復原服務提供者詳細資料。</span><span class="sxs-lookup"><span data-stu-id="888ea-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="888ea-109">例子</span><span class="sxs-lookup"><span data-stu-id="888ea-109">EXAMPLES</span></span>

### <span data-ttu-id="888ea-110">範例 1：在 Vault 中取得所有提供者</span><span class="sxs-lookup"><span data-stu-id="888ea-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="888ea-111">全部列出。</span><span class="sxs-lookup"><span data-stu-id="888ea-111">List all.</span></span>

## <span data-ttu-id="888ea-112">參數</span><span class="sxs-lookup"><span data-stu-id="888ea-112">PARAMETERS</span></span>

### <span data-ttu-id="888ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888ea-113">-DefaultProfile</span></span>
<span data-ttu-id="888ea-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="888ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="888ea-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="888ea-115">-FabricName</span></span>
<span data-ttu-id="888ea-116">布料名稱。</span><span class="sxs-lookup"><span data-stu-id="888ea-116">Fabric name.</span></span>

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

### <span data-ttu-id="888ea-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="888ea-117">-ProviderName</span></span>
<span data-ttu-id="888ea-118">復原服務提供者名稱</span><span class="sxs-lookup"><span data-stu-id="888ea-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="888ea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="888ea-119">-ResourceGroupName</span></span>
<span data-ttu-id="888ea-120">復原服務庫存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="888ea-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="888ea-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="888ea-121">-ResourceName</span></span>
<span data-ttu-id="888ea-122">復原服務庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="888ea-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="888ea-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="888ea-123">-SubscriptionId</span></span>
<span data-ttu-id="888ea-124">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="888ea-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="888ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888ea-125">CommonParameters</span></span>
<span data-ttu-id="888ea-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="888ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888ea-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="888ea-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888ea-128">輸入</span><span class="sxs-lookup"><span data-stu-id="888ea-128">INPUTS</span></span>

## <span data-ttu-id="888ea-129">輸出</span><span class="sxs-lookup"><span data-stu-id="888ea-129">OUTPUTS</span></span>

### <span data-ttu-id="888ea-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="888ea-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="888ea-131">筆記</span><span class="sxs-lookup"><span data-stu-id="888ea-131">NOTES</span></span>

<span data-ttu-id="888ea-132">別名</span><span class="sxs-lookup"><span data-stu-id="888ea-132">ALIASES</span></span>

## <span data-ttu-id="888ea-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="888ea-133">RELATED LINKS</span></span>

