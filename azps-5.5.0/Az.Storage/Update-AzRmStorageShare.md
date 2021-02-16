---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142907"
---
# <span data-ttu-id="6f21d-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6f21d-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="6f21d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f21d-102">SYNOPSIS</span></span>
<span data-ttu-id="6f21d-103">修改儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="6f21d-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="6f21d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f21d-104">SYNTAX</span></span>

### <span data-ttu-id="6f21d-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="6f21d-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f21d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6f21d-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f21d-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="6f21d-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f21d-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="6f21d-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f21d-109">說明</span><span class="sxs-lookup"><span data-stu-id="6f21d-109">DESCRIPTION</span></span>
<span data-ttu-id="6f21d-110">**新的-AzRmStorageShare** Cmdlet 會修改儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="6f21d-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="6f21d-111">示例</span><span class="sxs-lookup"><span data-stu-id="6f21d-111">EXAMPLES</span></span>

### <span data-ttu-id="6f21d-112">範例1：修改儲存空間共用的中繼資料，並使用儲存空間帳戶名稱和共用名稱稱共用配額</span><span class="sxs-lookup"><span data-stu-id="6f21d-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
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

<span data-ttu-id="6f21d-113">這個命令會修改儲存空間共用的中繼資料，並與儲存空間帳戶名稱和共用名稱稱共用配額，並以傳回的檔案共用物件顯示 [修改結果]。</span><span class="sxs-lookup"><span data-stu-id="6f21d-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="6f21d-114">範例2：使用儲存空間帳戶物件和共用名稱稱來修改儲存空間共用上的中繼資料</span><span class="sxs-lookup"><span data-stu-id="6f21d-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="6f21d-115">這個命令會透過儲存帳戶物件和共用名稱稱來修改儲存空間共用上的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6f21d-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="6f21d-116">範例3：針對含管線的儲存空間帳戶中的所有儲存空間共用修改共用配額</span><span class="sxs-lookup"><span data-stu-id="6f21d-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="6f21d-117">這個命令會針對含管線的儲存空間帳戶中的所有儲存空間共用，以 5000 GiB 的方式來修改共用配額。</span><span class="sxs-lookup"><span data-stu-id="6f21d-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="6f21d-118">範例4：使用 accesstier 修改儲存空間共用（含超酷）</span><span class="sxs-lookup"><span data-stu-id="6f21d-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="6f21d-119">這個命令會以超酷的方式修改儲存空間共用與 accesstier。</span><span class="sxs-lookup"><span data-stu-id="6f21d-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="6f21d-120">參數</span><span class="sxs-lookup"><span data-stu-id="6f21d-120">PARAMETERS</span></span>

### <span data-ttu-id="6f21d-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="6f21d-121">-AccessTier</span></span>
<span data-ttu-id="6f21d-122">特定共用的存取層級。</span><span class="sxs-lookup"><span data-stu-id="6f21d-122">Access tier for specific share.</span></span> <span data-ttu-id="6f21d-123">StorageV2 帳戶可以選擇 TransactionOptimized (預設的 [) 、[熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="6f21d-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="6f21d-124">FileStorage 帳戶可以選擇 [特優]。</span><span class="sxs-lookup"><span data-stu-id="6f21d-124">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="6f21d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f21d-125">-DefaultProfile</span></span>
<span data-ttu-id="6f21d-126">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f21d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f21d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f21d-127">-InputObject</span></span>
<span data-ttu-id="6f21d-128">儲存空間份額物件</span><span class="sxs-lookup"><span data-stu-id="6f21d-128">Storage Share object</span></span>

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

### <span data-ttu-id="6f21d-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="6f21d-129">-Metadata</span></span>
<span data-ttu-id="6f21d-130">共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="6f21d-130">Share Metadata</span></span>

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

### <span data-ttu-id="6f21d-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f21d-131">-Name</span></span>
<span data-ttu-id="6f21d-132">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="6f21d-132">Share Name</span></span>

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

### <span data-ttu-id="6f21d-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="6f21d-133">-QuotaGiB</span></span>
<span data-ttu-id="6f21d-134">在 Gibibyte 中共用配額。</span><span class="sxs-lookup"><span data-stu-id="6f21d-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="6f21d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f21d-135">-ResourceGroupName</span></span>
<span data-ttu-id="6f21d-136">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6f21d-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="6f21d-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f21d-137">-ResourceId</span></span>
<span data-ttu-id="6f21d-138">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f21d-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="6f21d-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6f21d-139">-StorageAccount</span></span>
<span data-ttu-id="6f21d-140">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="6f21d-140">Storage account object</span></span>

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

### <span data-ttu-id="6f21d-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f21d-141">-StorageAccountName</span></span>
<span data-ttu-id="6f21d-142">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6f21d-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="6f21d-143">-確認</span><span class="sxs-lookup"><span data-stu-id="6f21d-143">-Confirm</span></span>
<span data-ttu-id="6f21d-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f21d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f21d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f21d-145">-WhatIf</span></span>
<span data-ttu-id="6f21d-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f21d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f21d-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f21d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f21d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f21d-148">CommonParameters</span></span>
<span data-ttu-id="6f21d-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f21d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f21d-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f21d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f21d-151">輸入</span><span class="sxs-lookup"><span data-stu-id="6f21d-151">INPUTS</span></span>

### <span data-ttu-id="6f21d-152">System.object</span><span class="sxs-lookup"><span data-stu-id="6f21d-152">System.String</span></span>

### <span data-ttu-id="6f21d-153">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6f21d-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6f21d-154">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6f21d-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="6f21d-155">輸出</span><span class="sxs-lookup"><span data-stu-id="6f21d-155">OUTPUTS</span></span>

### <span data-ttu-id="6f21d-156">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="6f21d-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="6f21d-157">筆記</span><span class="sxs-lookup"><span data-stu-id="6f21d-157">NOTES</span></span>

## <span data-ttu-id="6f21d-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f21d-158">RELATED LINKS</span></span>
