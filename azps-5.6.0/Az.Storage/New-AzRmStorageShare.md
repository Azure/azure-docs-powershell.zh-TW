---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: dcb4819a3ac13056acd1b51dde2ee67774d51693
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912981"
---
# <span data-ttu-id="ef7de-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ef7de-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="ef7de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ef7de-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7de-103">建立儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ef7de-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="ef7de-104">語法</span><span class="sxs-lookup"><span data-stu-id="ef7de-104">SYNTAX</span></span>

### <span data-ttu-id="ef7de-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ef7de-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef7de-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ef7de-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef7de-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef7de-107">DESCRIPTION</span></span>
<span data-ttu-id="ef7de-108">**New-AzRmStorageShare** Cmdlet 會建立儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ef7de-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="ef7de-109">例子</span><span class="sxs-lookup"><span data-stu-id="ef7de-109">EXAMPLES</span></span>

### <span data-ttu-id="ef7de-110">範例 1：使用儲存空間帳戶名稱和共用名稱稱建立儲存空間檔案共用，中繼資料和共用配額為 100 GiB。</span><span class="sxs-lookup"><span data-stu-id="ef7de-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="ef7de-111">此命令會建立包含中繼資料的儲存空間檔案共用，並共用配額為 100 GiB。</span><span class="sxs-lookup"><span data-stu-id="ef7de-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="ef7de-112">範例 2：使用 Storage 帳戶物件建立儲存空間檔案共用</span><span class="sxs-lookup"><span data-stu-id="ef7de-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="ef7de-113">此命令會使用儲存空間帳戶物件和共用名稱稱建立儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ef7de-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="ef7de-114">範例 3：使用 Accesstier 建立儲存空間檔案共用為 Hot</span><span class="sxs-lookup"><span data-stu-id="ef7de-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="ef7de-115">此命令會建立與 Accesstier 的儲存空間檔案共用為 Hot。</span><span class="sxs-lookup"><span data-stu-id="ef7de-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="ef7de-116">參數</span><span class="sxs-lookup"><span data-stu-id="ef7de-116">PARAMETERS</span></span>

### <span data-ttu-id="ef7de-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ef7de-117">-AccessTier</span></span>
<span data-ttu-id="ef7de-118">特定共用的存取權限層級。</span><span class="sxs-lookup"><span data-stu-id="ef7de-118">Access tier for specific share.</span></span> <span data-ttu-id="ef7de-119">StorageV2 帳戶可以選擇 TransactionOptimized (預設) 、Hot 和 Cool。</span><span class="sxs-lookup"><span data-stu-id="ef7de-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="ef7de-120">FileStorage 帳戶可以選擇進一版。</span><span class="sxs-lookup"><span data-stu-id="ef7de-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="ef7de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef7de-121">-DefaultProfile</span></span>
<span data-ttu-id="ef7de-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef7de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef7de-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="ef7de-123">-Metadata</span></span>
<span data-ttu-id="ef7de-124">共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="ef7de-124">Share Metadata</span></span>

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

### <span data-ttu-id="ef7de-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef7de-125">-Name</span></span>
<span data-ttu-id="ef7de-126">Azure 檔案共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="ef7de-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef7de-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="ef7de-127">-QuotaGiB</span></span>
<span data-ttu-id="ef7de-128">Gibibyte 中的共用配額。</span><span class="sxs-lookup"><span data-stu-id="ef7de-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="ef7de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef7de-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef7de-130">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ef7de-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ef7de-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ef7de-131">-StorageAccount</span></span>
<span data-ttu-id="ef7de-132">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ef7de-132">Storage account object</span></span>

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

### <span data-ttu-id="ef7de-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef7de-133">-StorageAccountName</span></span>
<span data-ttu-id="ef7de-134">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ef7de-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="ef7de-135">-確認</span><span class="sxs-lookup"><span data-stu-id="ef7de-135">-Confirm</span></span>
<span data-ttu-id="ef7de-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ef7de-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef7de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef7de-137">-WhatIf</span></span>
<span data-ttu-id="ef7de-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef7de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef7de-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef7de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef7de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7de-140">CommonParameters</span></span>
<span data-ttu-id="ef7de-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ef7de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7de-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ef7de-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7de-143">輸入</span><span class="sxs-lookup"><span data-stu-id="ef7de-143">INPUTS</span></span>

### <span data-ttu-id="ef7de-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ef7de-144">System.String</span></span>

### <span data-ttu-id="ef7de-145">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ef7de-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ef7de-146">輸出</span><span class="sxs-lookup"><span data-stu-id="ef7de-146">OUTPUTS</span></span>

### <span data-ttu-id="ef7de-147">Microsoft.Azure.Commands.management.storage.models.PSShare</span><span class="sxs-lookup"><span data-stu-id="ef7de-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ef7de-148">筆記</span><span class="sxs-lookup"><span data-stu-id="ef7de-148">NOTES</span></span>

## <span data-ttu-id="ef7de-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef7de-149">RELATED LINKS</span></span>
