---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286076"
---
# <span data-ttu-id="5e677-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="5e677-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="5e677-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e677-102">SYNOPSIS</span></span>
<span data-ttu-id="5e677-103">喚醒存儲帳戶的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="5e677-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="5e677-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e677-104">SYNTAX</span></span>

### <span data-ttu-id="5e677-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="5e677-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e677-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="5e677-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e677-107">說明</span><span class="sxs-lookup"><span data-stu-id="5e677-107">DESCRIPTION</span></span>
<span data-ttu-id="5e677-108">喚醒存儲帳戶的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="5e677-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="5e677-109">如果出現可用性問題，可能會針對儲存帳戶觸發容錯移轉要求。</span><span class="sxs-lookup"><span data-stu-id="5e677-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="5e677-110">從存儲帳戶的主要群集到 GRS 帳戶的輔助群集，進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="5e677-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="5e677-111">在容錯移轉之後，次要群集就會成為主要群集。</span><span class="sxs-lookup"><span data-stu-id="5e677-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="5e677-112">啟動容錯移轉之前，請先瞭解下列儲存空間的影響：1.1。</span><span class="sxs-lookup"><span data-stu-id="5e677-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="5e677-113">請檢查上次同步處理時間使用 [取得 Blob 服務的統計資料] (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) 、取得資料表服務統計資料 (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) 並取得 https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) 您帳戶的佇列服務 (統計資料。</span><span class="sxs-lookup"><span data-stu-id="5e677-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="5e677-114">如果您啟動容錯移轉，這就是您可能會遺失的資料。</span><span class="sxs-lookup"><span data-stu-id="5e677-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="5e677-115">2. 在容錯移轉之後，您的儲存帳戶類型將會轉換為本機冗余儲存空間 (LRS) 。</span><span class="sxs-lookup"><span data-stu-id="5e677-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="5e677-116">您可以將您的帳戶轉換為使用地域冗余儲存空間， (GRS) 。</span><span class="sxs-lookup"><span data-stu-id="5e677-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="5e677-117">3. 針對您的儲存空間帳戶重新啟用 GRS 後，Microsoft 會將資料複製到您的新次要區域。</span><span class="sxs-lookup"><span data-stu-id="5e677-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="5e677-118">複製時間取決於要複製的資料量。</span><span class="sxs-lookup"><span data-stu-id="5e677-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="5e677-119">請注意，引導程式有頻寬費用。</span><span class="sxs-lookup"><span data-stu-id="5e677-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="5e677-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="5e677-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="5e677-121">示例</span><span class="sxs-lookup"><span data-stu-id="5e677-121">EXAMPLES</span></span>

### <span data-ttu-id="5e677-122">範例1：喚醒儲存空間帳戶的容錯移轉</span><span class="sxs-lookup"><span data-stu-id="5e677-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="5e677-123">這個命令會檢查儲存帳戶的 [上次同步處理時間]，然後對其進行容錯移轉，次要群集會成為容錯移轉後的主要。</span><span class="sxs-lookup"><span data-stu-id="5e677-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="5e677-124">因為容錯移轉需要花很長的時間，建議您在後端使用-Asjob 參數執行此操作，然後等待工作完成。</span><span class="sxs-lookup"><span data-stu-id="5e677-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="5e677-125">參數</span><span class="sxs-lookup"><span data-stu-id="5e677-125">PARAMETERS</span></span>

### <span data-ttu-id="5e677-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e677-126">-AsJob</span></span>
<span data-ttu-id="5e677-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5e677-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e677-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e677-128">-DefaultProfile</span></span>
<span data-ttu-id="5e677-129">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e677-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e677-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5e677-130">-Force</span></span>
<span data-ttu-id="5e677-131">強制將帳戶容錯移轉</span><span class="sxs-lookup"><span data-stu-id="5e677-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="5e677-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e677-132">-InputObject</span></span>
<span data-ttu-id="5e677-133">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="5e677-133">Storage account object</span></span>

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

### <span data-ttu-id="5e677-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e677-134">-Name</span></span>
<span data-ttu-id="5e677-135">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5e677-135">Storage Account Name.</span></span>

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

### <span data-ttu-id="5e677-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e677-136">-ResourceGroupName</span></span>
<span data-ttu-id="5e677-137">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5e677-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e677-138">-確認</span><span class="sxs-lookup"><span data-stu-id="5e677-138">-Confirm</span></span>
<span data-ttu-id="5e677-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5e677-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e677-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e677-140">-WhatIf</span></span>
<span data-ttu-id="5e677-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5e677-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e677-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5e677-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e677-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e677-143">CommonParameters</span></span>
<span data-ttu-id="5e677-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e677-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e677-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e677-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e677-146">輸入</span><span class="sxs-lookup"><span data-stu-id="5e677-146">INPUTS</span></span>

### <span data-ttu-id="5e677-147">System.object</span><span class="sxs-lookup"><span data-stu-id="5e677-147">System.String</span></span>

## <span data-ttu-id="5e677-148">輸出</span><span class="sxs-lookup"><span data-stu-id="5e677-148">OUTPUTS</span></span>

### <span data-ttu-id="5e677-149">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="5e677-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="5e677-150">筆記</span><span class="sxs-lookup"><span data-stu-id="5e677-150">NOTES</span></span>

## <span data-ttu-id="5e677-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e677-151">RELATED LINKS</span></span>
