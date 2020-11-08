---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141507"
---
# <span data-ttu-id="4ff79-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4ff79-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="4ff79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ff79-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff79-103">取得已註冊的復原服務提供者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ff79-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="4ff79-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ff79-104">SYNTAX</span></span>

### <span data-ttu-id="4ff79-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="4ff79-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4ff79-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4ff79-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ff79-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ff79-107">DESCRIPTION</span></span>
<span data-ttu-id="4ff79-108">取得已註冊的復原服務提供者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4ff79-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="4ff79-109">示例</span><span class="sxs-lookup"><span data-stu-id="4ff79-109">EXAMPLES</span></span>

### <span data-ttu-id="4ff79-110">範例1：取得保存庫中的所有提供者</span><span class="sxs-lookup"><span data-stu-id="4ff79-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="4ff79-111">[全部列出]。</span><span class="sxs-lookup"><span data-stu-id="4ff79-111">List all.</span></span>

## <span data-ttu-id="4ff79-112">參數</span><span class="sxs-lookup"><span data-stu-id="4ff79-112">PARAMETERS</span></span>

### <span data-ttu-id="4ff79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff79-113">-DefaultProfile</span></span>
<span data-ttu-id="4ff79-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ff79-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ff79-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="4ff79-115">-FabricName</span></span>
<span data-ttu-id="4ff79-116">Fabric name。</span><span class="sxs-lookup"><span data-stu-id="4ff79-116">Fabric name.</span></span>

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

### <span data-ttu-id="4ff79-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="4ff79-117">-ProviderName</span></span>
<span data-ttu-id="4ff79-118">Recovery services 提供者名稱</span><span class="sxs-lookup"><span data-stu-id="4ff79-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="4ff79-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff79-119">-ResourceGroupName</span></span>
<span data-ttu-id="4ff79-120">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ff79-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="4ff79-121">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="4ff79-121">-ResourceName</span></span>
<span data-ttu-id="4ff79-122">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ff79-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="4ff79-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ff79-123">-SubscriptionId</span></span>
<span data-ttu-id="4ff79-124">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="4ff79-124">The subscription Id.</span></span>

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

### <span data-ttu-id="4ff79-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff79-125">CommonParameters</span></span>
<span data-ttu-id="4ff79-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ff79-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff79-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ff79-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff79-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4ff79-128">INPUTS</span></span>

## <span data-ttu-id="4ff79-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4ff79-129">OUTPUTS</span></span>

### <span data-ttu-id="4ff79-130">IRecoveryServicesProvider 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="4ff79-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="4ff79-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4ff79-131">NOTES</span></span>

<span data-ttu-id="4ff79-132">別名</span><span class="sxs-lookup"><span data-stu-id="4ff79-132">ALIASES</span></span>

## <span data-ttu-id="4ff79-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ff79-133">RELATED LINKS</span></span>

