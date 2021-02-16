---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 417f28feb03bbe55c787ff72021c2d9b16778cbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134095"
---
# <span data-ttu-id="1731e-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1731e-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="1731e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1731e-102">SYNOPSIS</span></span>
<span data-ttu-id="1731e-103">取得保護容器對應的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1731e-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="1731e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1731e-104">SYNTAX</span></span>

### <span data-ttu-id="1731e-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="1731e-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1731e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="1731e-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1731e-107">清單</span><span class="sxs-lookup"><span data-stu-id="1731e-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1731e-108">說明</span><span class="sxs-lookup"><span data-stu-id="1731e-108">DESCRIPTION</span></span>
<span data-ttu-id="1731e-109">取得保護容器對應的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1731e-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="1731e-110">示例</span><span class="sxs-lookup"><span data-stu-id="1731e-110">EXAMPLES</span></span>

### <span data-ttu-id="1731e-111">範例1：取得特定的對應</span><span class="sxs-lookup"><span data-stu-id="1731e-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="1731e-112">取得對應的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1731e-112">Get a mapping detail.</span></span>

## <span data-ttu-id="1731e-113">參數</span><span class="sxs-lookup"><span data-stu-id="1731e-113">PARAMETERS</span></span>

### <span data-ttu-id="1731e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1731e-114">-DefaultProfile</span></span>
<span data-ttu-id="1731e-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1731e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1731e-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="1731e-116">-FabricName</span></span>
<span data-ttu-id="1731e-117">Fabric name。</span><span class="sxs-lookup"><span data-stu-id="1731e-117">Fabric name.</span></span>

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

### <span data-ttu-id="1731e-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="1731e-118">-MappingName</span></span>
<span data-ttu-id="1731e-119">保護容器對應名稱。</span><span class="sxs-lookup"><span data-stu-id="1731e-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="1731e-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="1731e-120">-ProtectionContainerName</span></span>
<span data-ttu-id="1731e-121">保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="1731e-121">Protection container name.</span></span>

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

### <span data-ttu-id="1731e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1731e-122">-ResourceGroupName</span></span>
<span data-ttu-id="1731e-123">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1731e-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="1731e-124">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="1731e-124">-ResourceName</span></span>
<span data-ttu-id="1731e-125">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="1731e-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="1731e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1731e-126">-SubscriptionId</span></span>
<span data-ttu-id="1731e-127">在其中建立 [遷移] 專案的 Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="1731e-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="1731e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1731e-128">CommonParameters</span></span>
<span data-ttu-id="1731e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1731e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1731e-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1731e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1731e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1731e-131">INPUTS</span></span>

## <span data-ttu-id="1731e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1731e-132">OUTPUTS</span></span>

### <span data-ttu-id="1731e-133">IProtectionContainerMapping 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="1731e-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="1731e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="1731e-134">NOTES</span></span>

<span data-ttu-id="1731e-135">別名</span><span class="sxs-lookup"><span data-stu-id="1731e-135">ALIASES</span></span>

## <span data-ttu-id="1731e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="1731e-136">RELATED LINKS</span></span>

