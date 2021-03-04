---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 25106d6facb65346360bf7c78b7cbef27fc9a517
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909657"
---
# <span data-ttu-id="72263-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="72263-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="72263-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72263-102">SYNOPSIS</span></span>
<span data-ttu-id="72263-103">瞭解 Azure 網站修復結構的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="72263-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="72263-104">語法</span><span class="sxs-lookup"><span data-stu-id="72263-104">SYNTAX</span></span>

### <span data-ttu-id="72263-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="72263-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72263-106">獲取</span><span class="sxs-lookup"><span data-stu-id="72263-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="72263-107">描述</span><span class="sxs-lookup"><span data-stu-id="72263-107">DESCRIPTION</span></span>
<span data-ttu-id="72263-108">瞭解 Azure 網站修復結構的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="72263-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="72263-109">例子</span><span class="sxs-lookup"><span data-stu-id="72263-109">EXAMPLES</span></span>

### <span data-ttu-id="72263-110">範例 1：根據資源群組和庫名稱取得所有布料</span><span class="sxs-lookup"><span data-stu-id="72263-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="72263-111">取得資源群組和庫中的所有結構</span><span class="sxs-lookup"><span data-stu-id="72263-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="72263-112">範例 2：根據資源群組取得結構、庫名稱及結構名稱</span><span class="sxs-lookup"><span data-stu-id="72263-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="72263-113">取得特定布料</span><span class="sxs-lookup"><span data-stu-id="72263-113">Get a specific fabric</span></span>

## <span data-ttu-id="72263-114">參數</span><span class="sxs-lookup"><span data-stu-id="72263-114">PARAMETERS</span></span>

### <span data-ttu-id="72263-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72263-115">-DefaultProfile</span></span>
<span data-ttu-id="72263-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72263-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72263-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="72263-117">-FabricName</span></span>
<span data-ttu-id="72263-118">布料名稱。</span><span class="sxs-lookup"><span data-stu-id="72263-118">Fabric name.</span></span>

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

### <span data-ttu-id="72263-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72263-119">-ResourceGroupName</span></span>
<span data-ttu-id="72263-120">復原服務庫存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="72263-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="72263-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="72263-121">-ResourceName</span></span>
<span data-ttu-id="72263-122">復原服務庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="72263-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="72263-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72263-123">-SubscriptionId</span></span>
<span data-ttu-id="72263-124">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="72263-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="72263-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72263-125">CommonParameters</span></span>
<span data-ttu-id="72263-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72263-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72263-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72263-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72263-128">輸入</span><span class="sxs-lookup"><span data-stu-id="72263-128">INPUTS</span></span>

## <span data-ttu-id="72263-129">輸出</span><span class="sxs-lookup"><span data-stu-id="72263-129">OUTPUTS</span></span>

### <span data-ttu-id="72263-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="72263-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="72263-131">筆記</span><span class="sxs-lookup"><span data-stu-id="72263-131">NOTES</span></span>

<span data-ttu-id="72263-132">別名</span><span class="sxs-lookup"><span data-stu-id="72263-132">ALIASES</span></span>

## <span data-ttu-id="72263-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="72263-133">RELATED LINKS</span></span>

