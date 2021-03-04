---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 44ad4fadb86b84b5eacb82a15bf92b7b1d831b70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915161"
---
# <span data-ttu-id="bd20c-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="bd20c-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="bd20c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd20c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd20c-103">獲取或列出儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="bd20c-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="bd20c-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd20c-104">SYNTAX</span></span>

### <span data-ttu-id="bd20c-105">AccountNameSingle (預設) </span><span class="sxs-lookup"><span data-stu-id="bd20c-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd20c-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="bd20c-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd20c-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="bd20c-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd20c-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bd20c-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd20c-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="bd20c-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd20c-110">描述</span><span class="sxs-lookup"><span data-stu-id="bd20c-110">DESCRIPTION</span></span>
<span data-ttu-id="bd20c-111">**Get-AzRmStorageShare** Cmdlet 取得或列出儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="bd20c-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="bd20c-112">例子</span><span class="sxs-lookup"><span data-stu-id="bd20c-112">EXAMPLES</span></span>

### <span data-ttu-id="bd20c-113">範例 1：使用儲存空間帳戶名稱和共用名稱稱取得儲存空間檔案共用</span><span class="sxs-lookup"><span data-stu-id="bd20c-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="bd20c-114">此命令會使用儲存空間帳戶名稱和共用名稱稱來共用儲存空間檔案。</span><span class="sxs-lookup"><span data-stu-id="bd20c-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="bd20c-115">範例 2：列出儲存空間帳戶的所有儲存空間檔案共用</span><span class="sxs-lookup"><span data-stu-id="bd20c-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="bd20c-116">此命令會以儲存帳戶名稱列出儲存空間帳戶的所有儲存空間檔案共用。</span><span class="sxs-lookup"><span data-stu-id="bd20c-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="bd20c-117">範例 3：取得儲存空間 Blob 容器與儲存帳戶物件和容器名稱。</span><span class="sxs-lookup"><span data-stu-id="bd20c-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="bd20c-118">此命令會獲得包含儲存帳戶物件和容器名稱的儲存 Blob 容器。</span><span class="sxs-lookup"><span data-stu-id="bd20c-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="bd20c-119">範例 4：使用以位元組為單位的共用使用量取得儲存空間檔案共用</span><span class="sxs-lookup"><span data-stu-id="bd20c-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="bd20c-120">此命令會以儲存空間帳戶名稱和共用名稱稱獲得儲存空間檔案共用，並包含以位元組為單位的共用使用量。</span><span class="sxs-lookup"><span data-stu-id="bd20c-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="bd20c-121">範例 5：列出儲存空間帳戶的所有儲存空間檔案共用，包括已刪除的共用</span><span class="sxs-lookup"><span data-stu-id="bd20c-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="bd20c-122">此命令會列出所有儲存檔案共用，包括儲存空間帳戶的已刪除共用與儲存帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bd20c-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="bd20c-123">參數</span><span class="sxs-lookup"><span data-stu-id="bd20c-123">PARAMETERS</span></span>

### <span data-ttu-id="bd20c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd20c-124">-DefaultProfile</span></span>
<span data-ttu-id="bd20c-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd20c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd20c-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="bd20c-126">-GetShareUsage</span></span>
<span data-ttu-id="bd20c-127">指定此參數以取得以位元組為單位的共用使用量。</span><span class="sxs-lookup"><span data-stu-id="bd20c-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd20c-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="bd20c-128">-IncludeDeleted</span></span>
<span data-ttu-id="bd20c-129">包含已刪除的共用，根據預設清單共用不會包含已刪除的共用</span><span class="sxs-lookup"><span data-stu-id="bd20c-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd20c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd20c-130">-Name</span></span>
<span data-ttu-id="bd20c-131">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="bd20c-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd20c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd20c-132">-ResourceGroupName</span></span>
<span data-ttu-id="bd20c-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="bd20c-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd20c-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd20c-134">-ResourceId</span></span>
<span data-ttu-id="bd20c-135">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd20c-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="bd20c-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd20c-136">-StorageAccount</span></span>
<span data-ttu-id="bd20c-137">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="bd20c-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd20c-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bd20c-138">-StorageAccountName</span></span>
<span data-ttu-id="bd20c-139">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="bd20c-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd20c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd20c-140">CommonParameters</span></span>
<span data-ttu-id="bd20c-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd20c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd20c-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="bd20c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd20c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="bd20c-143">INPUTS</span></span>

### <span data-ttu-id="bd20c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="bd20c-144">System.String</span></span>

### <span data-ttu-id="bd20c-145">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd20c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bd20c-146">輸出</span><span class="sxs-lookup"><span data-stu-id="bd20c-146">OUTPUTS</span></span>

### <span data-ttu-id="bd20c-147">Microsoft.Azure.Commands.management.storage.models.PSShare</span><span class="sxs-lookup"><span data-stu-id="bd20c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="bd20c-148">筆記</span><span class="sxs-lookup"><span data-stu-id="bd20c-148">NOTES</span></span>

## <span data-ttu-id="bd20c-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd20c-149">RELATED LINKS</span></span>
