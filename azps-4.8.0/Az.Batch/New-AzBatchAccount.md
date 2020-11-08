---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: db35d5f6f0a8c8345fb10d13e4d2ca5c6169a090
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126565"
---
# <span data-ttu-id="2ecae-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2ecae-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="2ecae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ecae-102">SYNOPSIS</span></span>
<span data-ttu-id="2ecae-103">建立 Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2ecae-103">Creates a Batch account.</span></span>

## <span data-ttu-id="2ecae-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ecae-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-PublicNetworkAccess <PublicNetworkAccessType>]
 [-IdentityType <ResourceIdentityType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ecae-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ecae-105">DESCRIPTION</span></span>
<span data-ttu-id="2ecae-106">**新的-AzBatchAccount** Cmdlet 會針對指定的資源群組和位置建立 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="2ecae-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="2ecae-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ecae-107">EXAMPLES</span></span>

### <span data-ttu-id="2ecae-108">範例1：建立批次帳戶</span><span class="sxs-lookup"><span data-stu-id="2ecae-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="2ecae-109">這個命令會使用 [西部美國] 位置中的 [ResourceGroup03] 資源群組，建立名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="2ecae-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="2ecae-110">參數</span><span class="sxs-lookup"><span data-stu-id="2ecae-110">PARAMETERS</span></span>

### <span data-ttu-id="2ecae-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ecae-111">-AccountName</span></span>
<span data-ttu-id="2ecae-112">指定此 Cmdlet 所建立之 Batch 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ecae-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="2ecae-113">Batch 帳戶名稱長度必須介於3到24個字元之間，且只包含數位和小寫字母。</span><span class="sxs-lookup"><span data-stu-id="2ecae-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2ecae-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="2ecae-115">指定要用於自動儲存的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ecae-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ecae-116">-DefaultProfile</span></span>
<span data-ttu-id="2ecae-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ecae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-118">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2ecae-118">-IdentityType</span></span>
<span data-ttu-id="2ecae-119">與 BatchAccount 相關聯的身分識別</span><span class="sxs-lookup"><span data-stu-id="2ecae-119">The identity associated with the BatchAccount</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.ResourceIdentityType
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-120">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="2ecae-120">-KeyVaultId</span></span>
<span data-ttu-id="2ecae-121">與 Batch 帳戶相關聯之 Azure 金鑰電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ecae-121">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-122">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="2ecae-122">-KeyVaultUrl</span></span>
<span data-ttu-id="2ecae-123">與 Batch 帳戶相關聯之 Azure 金鑰電子倉庫的 URL。</span><span class="sxs-lookup"><span data-stu-id="2ecae-123">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-124">-位置</span><span class="sxs-lookup"><span data-stu-id="2ecae-124">-Location</span></span>
<span data-ttu-id="2ecae-125">指定此 Cmdlet 建立帳戶的地區。</span><span class="sxs-lookup"><span data-stu-id="2ecae-125">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="2ecae-126">如需詳細資訊，請參閱 [Azure 地區](https://azure.microsoft.com/en-us/regions)。</span><span class="sxs-lookup"><span data-stu-id="2ecae-126">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-127">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="2ecae-127">-PoolAllocationMode</span></span>
<span data-ttu-id="2ecae-128">在批次帳戶中建立池的配置模式。</span><span class="sxs-lookup"><span data-stu-id="2ecae-128">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-129">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2ecae-129">-PublicNetworkAccess</span></span>
<span data-ttu-id="2ecae-130">公用網路存取類型</span><span class="sxs-lookup"><span data-stu-id="2ecae-130">The public network access type</span></span>

```yaml
Type: Microsoft.Azure.Management.Batch.Models.PublicNetworkAccessType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ecae-131">-ResourceGroupName</span></span>
<span data-ttu-id="2ecae-132">指定此 Cmdlet 在其中建立帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ecae-132">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ecae-133">-Tag</span></span>
<span data-ttu-id="2ecae-134">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="2ecae-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ecae-135">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2ecae-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ecae-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ecae-136">CommonParameters</span></span>
<span data-ttu-id="2ecae-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ecae-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ecae-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2ecae-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ecae-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2ecae-139">INPUTS</span></span>

### <span data-ttu-id="2ecae-140">System.object</span><span class="sxs-lookup"><span data-stu-id="2ecae-140">System.String</span></span>

### <span data-ttu-id="2ecae-141">System.object "1 [Microsoft.Azure.Management.Batch。PoolAllocationMode、Microsoft.Azure.Management.Batch、版本 = 9.0.0.0、Culture = 中立、PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2ecae-141">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=9.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2ecae-142">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ecae-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ecae-143">輸出</span><span class="sxs-lookup"><span data-stu-id="2ecae-143">OUTPUTS</span></span>

### <span data-ttu-id="2ecae-144">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="2ecae-144">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2ecae-145">筆記</span><span class="sxs-lookup"><span data-stu-id="2ecae-145">NOTES</span></span>

## <span data-ttu-id="2ecae-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ecae-146">RELATED LINKS</span></span>

[<span data-ttu-id="2ecae-147">AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2ecae-147">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="2ecae-148">移除-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2ecae-148">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="2ecae-149">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="2ecae-149">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="2ecae-150">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2ecae-150">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
