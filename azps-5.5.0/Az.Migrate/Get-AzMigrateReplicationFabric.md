---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 6872eb3da4f67969dcb6ec57a9e300677bd4611b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134107"
---
# <span data-ttu-id="16a6a-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="16a6a-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="16a6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="16a6a-103">取得 Azure Site Recovery 結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="16a6a-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="16a6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="16a6a-104">SYNTAX</span></span>

### <span data-ttu-id="16a6a-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="16a6a-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="16a6a-106">獲取</span><span class="sxs-lookup"><span data-stu-id="16a6a-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="16a6a-107">說明</span><span class="sxs-lookup"><span data-stu-id="16a6a-107">DESCRIPTION</span></span>
<span data-ttu-id="16a6a-108">取得 Azure Site Recovery 結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="16a6a-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="16a6a-109">示例</span><span class="sxs-lookup"><span data-stu-id="16a6a-109">EXAMPLES</span></span>

### <span data-ttu-id="16a6a-110">範例1：透過資源群組和保存庫名稱取得所有結構</span><span class="sxs-lookup"><span data-stu-id="16a6a-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="16a6a-111">取得資源群組和保存庫中的所有結構</span><span class="sxs-lookup"><span data-stu-id="16a6a-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="16a6a-112">範例2：透過資源群組、保存庫名稱和結構名稱來取得結構</span><span class="sxs-lookup"><span data-stu-id="16a6a-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="16a6a-113">取得特定結構</span><span class="sxs-lookup"><span data-stu-id="16a6a-113">Get a specific fabric</span></span>

## <span data-ttu-id="16a6a-114">參數</span><span class="sxs-lookup"><span data-stu-id="16a6a-114">PARAMETERS</span></span>

### <span data-ttu-id="16a6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16a6a-115">-DefaultProfile</span></span>
<span data-ttu-id="16a6a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16a6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16a6a-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="16a6a-117">-FabricName</span></span>
<span data-ttu-id="16a6a-118">Fabric name。</span><span class="sxs-lookup"><span data-stu-id="16a6a-118">Fabric name.</span></span>

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

### <span data-ttu-id="16a6a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16a6a-119">-ResourceGroupName</span></span>
<span data-ttu-id="16a6a-120">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16a6a-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="16a6a-121">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="16a6a-121">-ResourceName</span></span>
<span data-ttu-id="16a6a-122">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="16a6a-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="16a6a-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16a6a-123">-SubscriptionId</span></span>
<span data-ttu-id="16a6a-124">在其中建立 [遷移] 專案的 Azure 訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="16a6a-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="16a6a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16a6a-125">CommonParameters</span></span>
<span data-ttu-id="16a6a-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16a6a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16a6a-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="16a6a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16a6a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="16a6a-128">INPUTS</span></span>

## <span data-ttu-id="16a6a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="16a6a-129">OUTPUTS</span></span>

### <span data-ttu-id="16a6a-130">IFabric 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="16a6a-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="16a6a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="16a6a-131">NOTES</span></span>

<span data-ttu-id="16a6a-132">別名</span><span class="sxs-lookup"><span data-stu-id="16a6a-132">ALIASES</span></span>

## <span data-ttu-id="16a6a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="16a6a-133">RELATED LINKS</span></span>

