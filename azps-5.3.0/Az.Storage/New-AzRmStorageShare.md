---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436630"
---
# <span data-ttu-id="12665-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="12665-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="12665-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12665-102">SYNOPSIS</span></span>
<span data-ttu-id="12665-103">建立儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="12665-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="12665-104">句法</span><span class="sxs-lookup"><span data-stu-id="12665-104">SYNTAX</span></span>

### <span data-ttu-id="12665-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="12665-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12665-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="12665-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12665-107">說明</span><span class="sxs-lookup"><span data-stu-id="12665-107">DESCRIPTION</span></span>
<span data-ttu-id="12665-108">**新的-AzRmStorageShare** Cmdlet 會建立儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="12665-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="12665-109">示例</span><span class="sxs-lookup"><span data-stu-id="12665-109">EXAMPLES</span></span>

### <span data-ttu-id="12665-110">範例1：使用儲存空間帳戶名稱和共用名稱稱（含中繼資料和共用配額）來建立儲存檔案共用（100 GiB）。</span><span class="sxs-lookup"><span data-stu-id="12665-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="12665-111">這個命令會建立含中繼資料的儲存空間共用，並以 100 GiB 的方式共用配額。</span><span class="sxs-lookup"><span data-stu-id="12665-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="12665-112">範例2：使用儲存空間帳戶物件建立儲存檔案共用</span><span class="sxs-lookup"><span data-stu-id="12665-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="12665-113">這個命令會建立包含儲存空間帳戶物件和共用名稱稱的儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="12665-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="12665-114">範例3：以熱 accesstier 建立儲存檔案共用</span><span class="sxs-lookup"><span data-stu-id="12665-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="12665-115">這個命令會建立與 accesstier 為熱的儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="12665-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="12665-116">參數</span><span class="sxs-lookup"><span data-stu-id="12665-116">PARAMETERS</span></span>

### <span data-ttu-id="12665-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="12665-117">-AccessTier</span></span>
<span data-ttu-id="12665-118">特定共用的存取層級。</span><span class="sxs-lookup"><span data-stu-id="12665-118">Access tier for specific share.</span></span> <span data-ttu-id="12665-119">StorageV2 帳戶可以選擇 TransactionOptimized (預設的 [) 、[熱] 和 [超酷]。</span><span class="sxs-lookup"><span data-stu-id="12665-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="12665-120">FileStorage 帳戶可以選擇 [特優]。</span><span class="sxs-lookup"><span data-stu-id="12665-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="12665-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12665-121">-DefaultProfile</span></span>
<span data-ttu-id="12665-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12665-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12665-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="12665-123">-Metadata</span></span>
<span data-ttu-id="12665-124">共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="12665-124">Share Metadata</span></span>

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

### <span data-ttu-id="12665-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="12665-125">-Name</span></span>
<span data-ttu-id="12665-126">Azure 檔案共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="12665-126">Azure File share name</span></span>

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

### <span data-ttu-id="12665-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="12665-127">-QuotaGiB</span></span>
<span data-ttu-id="12665-128">在 Gibibyte 中共用配額。</span><span class="sxs-lookup"><span data-stu-id="12665-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="12665-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12665-129">-ResourceGroupName</span></span>
<span data-ttu-id="12665-130">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="12665-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="12665-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="12665-131">-StorageAccount</span></span>
<span data-ttu-id="12665-132">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="12665-132">Storage account object</span></span>

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

### <span data-ttu-id="12665-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="12665-133">-StorageAccountName</span></span>
<span data-ttu-id="12665-134">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="12665-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="12665-135">-確認</span><span class="sxs-lookup"><span data-stu-id="12665-135">-Confirm</span></span>
<span data-ttu-id="12665-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12665-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12665-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12665-137">-WhatIf</span></span>
<span data-ttu-id="12665-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12665-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12665-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12665-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12665-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12665-140">CommonParameters</span></span>
<span data-ttu-id="12665-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12665-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12665-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12665-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12665-143">輸入</span><span class="sxs-lookup"><span data-stu-id="12665-143">INPUTS</span></span>

### <span data-ttu-id="12665-144">System.object</span><span class="sxs-lookup"><span data-stu-id="12665-144">System.String</span></span>

### <span data-ttu-id="12665-145">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="12665-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="12665-146">輸出</span><span class="sxs-lookup"><span data-stu-id="12665-146">OUTPUTS</span></span>

### <span data-ttu-id="12665-147">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="12665-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="12665-148">筆記</span><span class="sxs-lookup"><span data-stu-id="12665-148">NOTES</span></span>

## <span data-ttu-id="12665-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="12665-149">RELATED LINKS</span></span>
