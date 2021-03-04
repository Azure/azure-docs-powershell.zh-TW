---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 7612b323600b2f076c30225994d6e475d66c01ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907249"
---
# <span data-ttu-id="0752f-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0752f-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="0752f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0752f-102">SYNOPSIS</span></span>
<span data-ttu-id="0752f-103">修改儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="0752f-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="0752f-104">語法</span><span class="sxs-lookup"><span data-stu-id="0752f-104">SYNTAX</span></span>

### <span data-ttu-id="0752f-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="0752f-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0752f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0752f-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0752f-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="0752f-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0752f-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="0752f-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0752f-109">描述</span><span class="sxs-lookup"><span data-stu-id="0752f-109">DESCRIPTION</span></span>
<span data-ttu-id="0752f-110">**New-AzRmStorageShare** Cmdlet 會修改儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="0752f-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="0752f-111">例子</span><span class="sxs-lookup"><span data-stu-id="0752f-111">EXAMPLES</span></span>

### <span data-ttu-id="0752f-112">範例 1：使用儲存空間帳戶名稱和共用名稱稱修改儲存檔案共用中繼資料和共用配額</span><span class="sxs-lookup"><span data-stu-id="0752f-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="0752f-113">此命令會修改儲存檔案共用之中繼資料，以及使用儲存空間帳戶名稱和共用名稱稱共用配額，並且使用所返回的檔案共用物件顯示修改結果。</span><span class="sxs-lookup"><span data-stu-id="0752f-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="0752f-114">範例 2：修改儲存空間檔案共用與儲存空間帳戶物件及共用名稱稱的中繼資料</span><span class="sxs-lookup"><span data-stu-id="0752f-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="0752f-115">此命令會修改儲存空間檔案共用與儲存空間帳戶物件及共用名稱稱的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0752f-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="0752f-116">範例 3：修改儲存帳戶中所有儲存空間檔案共用與管線的共用配額</span><span class="sxs-lookup"><span data-stu-id="0752f-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="0752f-117">此命令會針對具有管線的儲存空間帳戶中的所有儲存檔案共用，將共用配額修改為 5000 GiB。</span><span class="sxs-lookup"><span data-stu-id="0752f-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="0752f-118">範例 4：使用 Accesstier 將儲存空間檔案共用修改為 Cool</span><span class="sxs-lookup"><span data-stu-id="0752f-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="0752f-119">此命令會修改與 Accesstier 的儲存空間檔案共用為 Cool。</span><span class="sxs-lookup"><span data-stu-id="0752f-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="0752f-120">參數</span><span class="sxs-lookup"><span data-stu-id="0752f-120">PARAMETERS</span></span>

### <span data-ttu-id="0752f-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="0752f-121">-AccessTier</span></span>
<span data-ttu-id="0752f-122">特定共用的存取權限層級。</span><span class="sxs-lookup"><span data-stu-id="0752f-122">Access tier for specific share.</span></span> <span data-ttu-id="0752f-123">StorageV2 帳戶可以選擇 TransactionOptimized (預設) 、Hot 和 Cool。</span><span class="sxs-lookup"><span data-stu-id="0752f-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="0752f-124">FileStorage 帳戶可以選擇進一版。</span><span class="sxs-lookup"><span data-stu-id="0752f-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0752f-125">-DefaultProfile</span></span>
<span data-ttu-id="0752f-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0752f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0752f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0752f-127">-InputObject</span></span>
<span data-ttu-id="0752f-128">儲存空間共用物件</span><span class="sxs-lookup"><span data-stu-id="0752f-128">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0752f-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="0752f-129">-Metadata</span></span>
<span data-ttu-id="0752f-130">共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="0752f-130">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752f-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="0752f-131">-Name</span></span>
<span data-ttu-id="0752f-132">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="0752f-132">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752f-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="0752f-133">-QuotaGiB</span></span>
<span data-ttu-id="0752f-134">Gibibyte 中的共用配額。</span><span class="sxs-lookup"><span data-stu-id="0752f-134">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0752f-135">-ResourceGroupName</span></span>
<span data-ttu-id="0752f-136">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0752f-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="0752f-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0752f-137">-ResourceId</span></span>
<span data-ttu-id="0752f-138">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0752f-138">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0752f-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0752f-139">-StorageAccount</span></span>
<span data-ttu-id="0752f-140">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="0752f-140">Storage account object</span></span>

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

### <span data-ttu-id="0752f-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0752f-141">-StorageAccountName</span></span>
<span data-ttu-id="0752f-142">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0752f-142">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0752f-143">-確認</span><span class="sxs-lookup"><span data-stu-id="0752f-143">-Confirm</span></span>
<span data-ttu-id="0752f-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0752f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0752f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0752f-145">-WhatIf</span></span>
<span data-ttu-id="0752f-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0752f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0752f-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0752f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0752f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0752f-148">CommonParameters</span></span>
<span data-ttu-id="0752f-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0752f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0752f-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0752f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0752f-151">輸入</span><span class="sxs-lookup"><span data-stu-id="0752f-151">INPUTS</span></span>

### <span data-ttu-id="0752f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="0752f-152">System.String</span></span>

### <span data-ttu-id="0752f-153">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0752f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="0752f-154">Microsoft.Azure.Commands.management.storage.models.PSShare</span><span class="sxs-lookup"><span data-stu-id="0752f-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="0752f-155">輸出</span><span class="sxs-lookup"><span data-stu-id="0752f-155">OUTPUTS</span></span>

### <span data-ttu-id="0752f-156">Microsoft.Azure.Commands.management.storage.models.PSShare</span><span class="sxs-lookup"><span data-stu-id="0752f-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="0752f-157">筆記</span><span class="sxs-lookup"><span data-stu-id="0752f-157">NOTES</span></span>

## <span data-ttu-id="0752f-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="0752f-158">RELATED LINKS</span></span>
