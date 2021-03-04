---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: c2dd4abcf9e917d4a34ed548cd356e02875971b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912986"
---
# <span data-ttu-id="cf62a-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="cf62a-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="cf62a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cf62a-102">SYNOPSIS</span></span>
<span data-ttu-id="cf62a-103">會調用儲存空間帳戶的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="cf62a-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="cf62a-104">語法</span><span class="sxs-lookup"><span data-stu-id="cf62a-104">SYNTAX</span></span>

### <span data-ttu-id="cf62a-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="cf62a-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf62a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cf62a-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf62a-107">描述</span><span class="sxs-lookup"><span data-stu-id="cf62a-107">DESCRIPTION</span></span>
<span data-ttu-id="cf62a-108">會調用儲存空間帳戶的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="cf62a-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="cf62a-109">如果可用性問題，可以針對儲存空間帳戶觸發容錯移轉要求。</span><span class="sxs-lookup"><span data-stu-id="cf62a-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="cf62a-110">容錯移轉會發生從儲存帳戶的主組到 RA-GRS 帳戶的次要組。</span><span class="sxs-lookup"><span data-stu-id="cf62a-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="cf62a-111">次要組會于容錯移轉後成為主要。</span><span class="sxs-lookup"><span data-stu-id="cf62a-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="cf62a-112">在您啟動容錯移轉之前，請先瞭解下列對儲存空間帳戶的影響：1.1。</span><span class="sxs-lookup"><span data-stu-id="cf62a-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="cf62a-113">請檢查使用 GET Blob 服務統計資料的上次同步處理時間 (、取得資料表服務統計資料 (以及取得您的帳戶 (佇列服務 https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats) https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) 統計資料。</span><span class="sxs-lookup"><span data-stu-id="cf62a-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="cf62a-114">這是當您啟動容錯移轉時可能會失去的資料。</span><span class="sxs-lookup"><span data-stu-id="cf62a-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="cf62a-115">2.容錯移轉之後，您的儲存空間帳戶類型將會轉換成 LRS (儲存) 。</span><span class="sxs-lookup"><span data-stu-id="cf62a-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="cf62a-116">您可以將您的帳戶轉換為使用 GS (異地) 。</span><span class="sxs-lookup"><span data-stu-id="cf62a-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="cf62a-117">3.重新啟用儲存空間帳戶的 GS 後，Microsoft 會將資料複製到新的次要區域。</span><span class="sxs-lookup"><span data-stu-id="cf62a-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="cf62a-118">複製時間取決於要複製的資料量。</span><span class="sxs-lookup"><span data-stu-id="cf62a-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="cf62a-119">請注意，開機需要支付頻寬費用。</span><span class="sxs-lookup"><span data-stu-id="cf62a-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="cf62a-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="cf62a-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="cf62a-121">例子</span><span class="sxs-lookup"><span data-stu-id="cf62a-121">EXAMPLES</span></span>

### <span data-ttu-id="cf62a-122">範例 1：在儲存空間帳戶的 Invoke 容錯移轉</span><span class="sxs-lookup"><span data-stu-id="cf62a-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="cf62a-123">此命令會檢查儲存空間帳戶的最後同步處理時間，然後調用該帳戶的容錯移轉，次要組在容錯移轉後會變成主要。</span><span class="sxs-lookup"><span data-stu-id="cf62a-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="cf62a-124">由於容錯移轉需要很長的時間，建議在後端使用 -Asjob 參數執行，然後等待工作完成。</span><span class="sxs-lookup"><span data-stu-id="cf62a-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="cf62a-125">參數</span><span class="sxs-lookup"><span data-stu-id="cf62a-125">PARAMETERS</span></span>

### <span data-ttu-id="cf62a-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf62a-126">-AsJob</span></span>
<span data-ttu-id="cf62a-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf62a-127">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf62a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf62a-128">-DefaultProfile</span></span>
<span data-ttu-id="cf62a-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf62a-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf62a-130">-強制</span><span class="sxs-lookup"><span data-stu-id="cf62a-130">-Force</span></span>
<span data-ttu-id="cf62a-131">強制容錯移轉帳戶</span><span class="sxs-lookup"><span data-stu-id="cf62a-131">Force to Failover the Account</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf62a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf62a-132">-InputObject</span></span>
<span data-ttu-id="cf62a-133">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="cf62a-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf62a-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf62a-134">-Name</span></span>
<span data-ttu-id="cf62a-135">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cf62a-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf62a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf62a-136">-ResourceGroupName</span></span>
<span data-ttu-id="cf62a-137">資源組名。</span><span class="sxs-lookup"><span data-stu-id="cf62a-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf62a-138">-確認</span><span class="sxs-lookup"><span data-stu-id="cf62a-138">-Confirm</span></span>
<span data-ttu-id="cf62a-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cf62a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf62a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf62a-140">-WhatIf</span></span>
<span data-ttu-id="cf62a-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf62a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf62a-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf62a-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf62a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf62a-143">CommonParameters</span></span>
<span data-ttu-id="cf62a-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cf62a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf62a-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cf62a-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf62a-146">輸入</span><span class="sxs-lookup"><span data-stu-id="cf62a-146">INPUTS</span></span>

### <span data-ttu-id="cf62a-147">System.String</span><span class="sxs-lookup"><span data-stu-id="cf62a-147">System.String</span></span>

## <span data-ttu-id="cf62a-148">輸出</span><span class="sxs-lookup"><span data-stu-id="cf62a-148">OUTPUTS</span></span>

### <span data-ttu-id="cf62a-149">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cf62a-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="cf62a-150">筆記</span><span class="sxs-lookup"><span data-stu-id="cf62a-150">NOTES</span></span>

## <span data-ttu-id="cf62a-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf62a-151">RELATED LINKS</span></span>
