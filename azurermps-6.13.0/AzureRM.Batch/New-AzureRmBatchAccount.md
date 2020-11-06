---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: d634ab23912c45a0916ccf64244dda24190c6ee3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447467"
---
# <span data-ttu-id="97103-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="97103-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="97103-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97103-102">SYNOPSIS</span></span>
<span data-ttu-id="97103-103">建立 Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="97103-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97103-104">句法</span><span class="sxs-lookup"><span data-stu-id="97103-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97103-105">說明</span><span class="sxs-lookup"><span data-stu-id="97103-105">DESCRIPTION</span></span>
<span data-ttu-id="97103-106">**新的-AzureRmBatchAccount** Cmdlet 會針對指定的資源群組和位置建立 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="97103-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="97103-107">示例</span><span class="sxs-lookup"><span data-stu-id="97103-107">EXAMPLES</span></span>

### <span data-ttu-id="97103-108">範例1：建立批次帳戶</span><span class="sxs-lookup"><span data-stu-id="97103-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="97103-109">這個命令會使用 [西部美國] 位置中的 [ResourceGroup03] 資源群組，建立名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="97103-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="97103-110">參數</span><span class="sxs-lookup"><span data-stu-id="97103-110">PARAMETERS</span></span>

### <span data-ttu-id="97103-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="97103-111">-AccountName</span></span>
<span data-ttu-id="97103-112">指定此 Cmdlet 所建立之 Batch 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="97103-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="97103-113">Batch 帳戶名稱長度必須介於3到24個字元之間，且只包含數位和小寫字母。</span><span class="sxs-lookup"><span data-stu-id="97103-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="97103-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="97103-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="97103-115">指定要用於自動儲存的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="97103-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="97103-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97103-116">-DefaultProfile</span></span>
<span data-ttu-id="97103-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97103-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97103-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="97103-118">-KeyVaultId</span></span>
<span data-ttu-id="97103-119">與 Batch 帳戶相關聯之 Azure 金鑰電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="97103-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="97103-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="97103-120">-KeyVaultUrl</span></span>
<span data-ttu-id="97103-121">與 Batch 帳戶相關聯之 Azure 金鑰電子倉庫的 URL。</span><span class="sxs-lookup"><span data-stu-id="97103-121">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="97103-122">-位置</span><span class="sxs-lookup"><span data-stu-id="97103-122">-Location</span></span>
<span data-ttu-id="97103-123">指定此 Cmdlet 建立帳戶的地區。</span><span class="sxs-lookup"><span data-stu-id="97103-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="97103-124">如需詳細資訊，請參閱 [Azure 地區](https://azure.microsoft.com/en-us/regions)。</span><span class="sxs-lookup"><span data-stu-id="97103-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="97103-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="97103-125">-PoolAllocationMode</span></span>
<span data-ttu-id="97103-126">在批次帳戶中建立池的配置模式。</span><span class="sxs-lookup"><span data-stu-id="97103-126">The allocation mode for creating pools in the Batch account.</span></span>

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

### <span data-ttu-id="97103-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97103-127">-ResourceGroupName</span></span>
<span data-ttu-id="97103-128">指定此 Cmdlet 在其中建立帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97103-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="97103-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="97103-129">-Tag</span></span>
<span data-ttu-id="97103-130">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="97103-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97103-131">例如： @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="97103-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="97103-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97103-132">CommonParameters</span></span>
<span data-ttu-id="97103-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97103-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97103-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97103-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97103-135">輸入</span><span class="sxs-lookup"><span data-stu-id="97103-135">INPUTS</span></span>

### <span data-ttu-id="97103-136">System.object</span><span class="sxs-lookup"><span data-stu-id="97103-136">System.String</span></span>

### <span data-ttu-id="97103-137">System.object "1 [Microsoft.Azure.Management.Batch。PoolAllocationMode、Microsoft.Azure.Management.Batch、版本 = 4.0.0.0、Culture = 中立、PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="97103-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="97103-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="97103-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="97103-139">輸出</span><span class="sxs-lookup"><span data-stu-id="97103-139">OUTPUTS</span></span>

### <span data-ttu-id="97103-140">Microsoft.Azure.Commands.Batch.BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="97103-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="97103-141">筆記</span><span class="sxs-lookup"><span data-stu-id="97103-141">NOTES</span></span>

## <span data-ttu-id="97103-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="97103-142">RELATED LINKS</span></span>

[<span data-ttu-id="97103-143">AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="97103-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="97103-144">移除-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="97103-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="97103-145">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="97103-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="97103-146">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97103-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
