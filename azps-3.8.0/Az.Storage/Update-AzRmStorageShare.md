---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 6e3c71900e5fe4a4ac8e4f092691dcde3e759c2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957434"
---
# <span data-ttu-id="3bb20-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3bb20-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="3bb20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bb20-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb20-103">修改儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="3bb20-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="3bb20-104">句法</span><span class="sxs-lookup"><span data-stu-id="3bb20-104">SYNTAX</span></span>

### <span data-ttu-id="3bb20-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="3bb20-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bb20-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3bb20-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb20-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="3bb20-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb20-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="3bb20-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bb20-109">說明</span><span class="sxs-lookup"><span data-stu-id="3bb20-109">DESCRIPTION</span></span>
<span data-ttu-id="3bb20-110">**新的-AzRmStorageShare** Cmdlet 會修改儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="3bb20-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="3bb20-111">示例</span><span class="sxs-lookup"><span data-stu-id="3bb20-111">EXAMPLES</span></span>

### <span data-ttu-id="3bb20-112">範例1：修改儲存空間共用的中繼資料，並使用儲存空間帳戶名稱和共用名稱稱共用配額</span><span class="sxs-lookup"><span data-stu-id="3bb20-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="3bb20-113">這個命令會修改儲存空間共用的中繼資料，並與儲存空間帳戶名稱和共用名稱稱共用配額，並以傳回的檔案共用物件顯示 [修改結果]。</span><span class="sxs-lookup"><span data-stu-id="3bb20-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="3bb20-114">範例2：使用儲存空間帳戶物件和共用名稱稱來修改儲存空間共用上的中繼資料</span><span class="sxs-lookup"><span data-stu-id="3bb20-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="3bb20-115">這個命令會透過儲存帳戶物件和共用名稱稱來修改儲存空間共用上的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3bb20-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="3bb20-116">範例3：針對含管線的儲存空間帳戶中的所有儲存空間共用修改共用配額</span><span class="sxs-lookup"><span data-stu-id="3bb20-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="3bb20-117">這個命令會針對含管線的儲存空間帳戶中的所有儲存空間共用，以 5000 GiB 的方式來修改共用配額。</span><span class="sxs-lookup"><span data-stu-id="3bb20-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="3bb20-118">參數</span><span class="sxs-lookup"><span data-stu-id="3bb20-118">PARAMETERS</span></span>

### <span data-ttu-id="3bb20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb20-119">-DefaultProfile</span></span>
<span data-ttu-id="3bb20-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bb20-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb20-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3bb20-121">-InputObject</span></span>
<span data-ttu-id="3bb20-122">儲存空間份額物件</span><span class="sxs-lookup"><span data-stu-id="3bb20-122">Storage Share object</span></span>

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

### <span data-ttu-id="3bb20-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="3bb20-123">-Metadata</span></span>
<span data-ttu-id="3bb20-124">共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="3bb20-124">Share Metadata</span></span>

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

### <span data-ttu-id="3bb20-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bb20-125">-Name</span></span>
<span data-ttu-id="3bb20-126">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="3bb20-126">Share Name</span></span>

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

### <span data-ttu-id="3bb20-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="3bb20-127">-QuotaGiB</span></span>
<span data-ttu-id="3bb20-128">在 Gibibyte 中共用配額。</span><span class="sxs-lookup"><span data-stu-id="3bb20-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="3bb20-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb20-129">-ResourceGroupName</span></span>
<span data-ttu-id="3bb20-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb20-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="3bb20-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3bb20-131">-ResourceId</span></span>
<span data-ttu-id="3bb20-132">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3bb20-132">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="3bb20-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3bb20-133">-StorageAccount</span></span>
<span data-ttu-id="3bb20-134">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="3bb20-134">Storage account object</span></span>

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

### <span data-ttu-id="3bb20-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3bb20-135">-StorageAccountName</span></span>
<span data-ttu-id="3bb20-136">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3bb20-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="3bb20-137">-確認</span><span class="sxs-lookup"><span data-stu-id="3bb20-137">-Confirm</span></span>
<span data-ttu-id="3bb20-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3bb20-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb20-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb20-139">-WhatIf</span></span>
<span data-ttu-id="3bb20-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3bb20-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb20-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3bb20-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb20-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb20-142">CommonParameters</span></span>
<span data-ttu-id="3bb20-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bb20-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb20-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3bb20-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb20-145">輸入</span><span class="sxs-lookup"><span data-stu-id="3bb20-145">INPUTS</span></span>

### <span data-ttu-id="3bb20-146">System.object</span><span class="sxs-lookup"><span data-stu-id="3bb20-146">System.String</span></span>

### <span data-ttu-id="3bb20-147">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3bb20-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="3bb20-148">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3bb20-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="3bb20-149">輸出</span><span class="sxs-lookup"><span data-stu-id="3bb20-149">OUTPUTS</span></span>

### <span data-ttu-id="3bb20-150">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="3bb20-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="3bb20-151">筆記</span><span class="sxs-lookup"><span data-stu-id="3bb20-151">NOTES</span></span>

## <span data-ttu-id="3bb20-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bb20-152">RELATED LINKS</span></span>
