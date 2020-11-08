---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141515"
---
# <span data-ttu-id="c766f-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="c766f-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="c766f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c766f-102">SYNOPSIS</span></span>
<span data-ttu-id="c766f-103">取得 Azure Site Recovery 結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c766f-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="c766f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c766f-104">SYNTAX</span></span>

### <span data-ttu-id="c766f-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c766f-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c766f-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c766f-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c766f-107">說明</span><span class="sxs-lookup"><span data-stu-id="c766f-107">DESCRIPTION</span></span>
<span data-ttu-id="c766f-108">取得 Azure Site Recovery 結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c766f-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="c766f-109">示例</span><span class="sxs-lookup"><span data-stu-id="c766f-109">EXAMPLES</span></span>

### <span data-ttu-id="c766f-110">範例1：透過資源群組和保存庫名稱取得所有結構</span><span class="sxs-lookup"><span data-stu-id="c766f-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="c766f-111">取得資源群組和保存庫中的所有結構</span><span class="sxs-lookup"><span data-stu-id="c766f-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="c766f-112">範例2：透過資源群組、保存庫名稱和結構名稱來取得結構</span><span class="sxs-lookup"><span data-stu-id="c766f-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="c766f-113">取得特定結構</span><span class="sxs-lookup"><span data-stu-id="c766f-113">Get a specific fabric</span></span>

## <span data-ttu-id="c766f-114">參數</span><span class="sxs-lookup"><span data-stu-id="c766f-114">PARAMETERS</span></span>

### <span data-ttu-id="c766f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c766f-115">-DefaultProfile</span></span>
<span data-ttu-id="c766f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c766f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c766f-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="c766f-117">-FabricName</span></span>
<span data-ttu-id="c766f-118">Fabric name。</span><span class="sxs-lookup"><span data-stu-id="c766f-118">Fabric name.</span></span>

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

### <span data-ttu-id="c766f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c766f-119">-ResourceGroupName</span></span>
<span data-ttu-id="c766f-120">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c766f-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c766f-121">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="c766f-121">-ResourceName</span></span>
<span data-ttu-id="c766f-122">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c766f-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c766f-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c766f-123">-SubscriptionId</span></span>
<span data-ttu-id="c766f-124">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="c766f-124">The subscription Id.</span></span>

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

### <span data-ttu-id="c766f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c766f-125">CommonParameters</span></span>
<span data-ttu-id="c766f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c766f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c766f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c766f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c766f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="c766f-128">INPUTS</span></span>

## <span data-ttu-id="c766f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c766f-129">OUTPUTS</span></span>

### <span data-ttu-id="c766f-130">IFabric 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="c766f-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="c766f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c766f-131">NOTES</span></span>

<span data-ttu-id="c766f-132">別名</span><span class="sxs-lookup"><span data-stu-id="c766f-132">ALIASES</span></span>

## <span data-ttu-id="c766f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="c766f-133">RELATED LINKS</span></span>

