---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141207"
---
# <span data-ttu-id="38b3f-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="38b3f-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="38b3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="38b3f-103">取得或列出儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="38b3f-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="38b3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="38b3f-104">SYNTAX</span></span>

### <span data-ttu-id="38b3f-105">AccountNameSingle (預設) </span><span class="sxs-lookup"><span data-stu-id="38b3f-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b3f-106">帳戶</span><span class="sxs-lookup"><span data-stu-id="38b3f-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b3f-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="38b3f-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b3f-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="38b3f-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b3f-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="38b3f-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38b3f-110">說明</span><span class="sxs-lookup"><span data-stu-id="38b3f-110">DESCRIPTION</span></span>
<span data-ttu-id="38b3f-111">**AzRmStorageShare** Cmdlet 會取得或列出儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="38b3f-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="38b3f-112">示例</span><span class="sxs-lookup"><span data-stu-id="38b3f-112">EXAMPLES</span></span>

### <span data-ttu-id="38b3f-113">範例1：使用儲存空間帳戶名稱和共用名稱稱來取得儲存檔案共用</span><span class="sxs-lookup"><span data-stu-id="38b3f-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="38b3f-114">這個命令會透過儲存空間帳戶名稱和共用名稱稱來取得儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="38b3f-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="38b3f-115">範例2：列出儲存空間帳戶的所有儲存空間份額</span><span class="sxs-lookup"><span data-stu-id="38b3f-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="38b3f-116">這個命令會列出儲存空間帳戶名稱的所有儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="38b3f-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="38b3f-117">範例3：使用儲存空間帳戶物件和容器名稱來取得儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="38b3f-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="38b3f-118">這個命令會取得含儲存空間帳戶物件和容器名稱的儲存 blob 容器。</span><span class="sxs-lookup"><span data-stu-id="38b3f-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="38b3f-119">範例4：取得含共用使用量的儲存檔案共用（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="38b3f-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="38b3f-120">這個命令會透過儲存帳戶名稱和共用名稱稱來取得儲存空間共用，並以位元組為單位來包含共用使用量。</span><span class="sxs-lookup"><span data-stu-id="38b3f-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="38b3f-121">範例5：列出儲存空間帳戶的所有儲存空間份額，包括刪除的共用</span><span class="sxs-lookup"><span data-stu-id="38b3f-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="38b3f-122">這個命令會列出所有儲存空間共用，包括儲存空間帳戶的已刪除共用儲存帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="38b3f-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="38b3f-123">參數</span><span class="sxs-lookup"><span data-stu-id="38b3f-123">PARAMETERS</span></span>

### <span data-ttu-id="38b3f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b3f-124">-DefaultProfile</span></span>
<span data-ttu-id="38b3f-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38b3f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b3f-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="38b3f-126">-GetShareUsage</span></span>
<span data-ttu-id="38b3f-127">指定此參數以取得共用使用量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="38b3f-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

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

### <span data-ttu-id="38b3f-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="38b3f-128">-IncludeDeleted</span></span>
<span data-ttu-id="38b3f-129">包括刪除的共用：預設清單共用不會包含已刪除的共用</span><span class="sxs-lookup"><span data-stu-id="38b3f-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

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

### <span data-ttu-id="38b3f-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="38b3f-130">-Name</span></span>
<span data-ttu-id="38b3f-131">共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="38b3f-131">Share Name</span></span>

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

### <span data-ttu-id="38b3f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b3f-132">-ResourceGroupName</span></span>
<span data-ttu-id="38b3f-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="38b3f-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="38b3f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38b3f-134">-ResourceId</span></span>
<span data-ttu-id="38b3f-135">輸入檔案共用資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="38b3f-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="38b3f-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="38b3f-136">-StorageAccount</span></span>
<span data-ttu-id="38b3f-137">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="38b3f-137">Storage account object</span></span>

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

### <span data-ttu-id="38b3f-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="38b3f-138">-StorageAccountName</span></span>
<span data-ttu-id="38b3f-139">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="38b3f-139">Storage Account Name.</span></span>

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

### <span data-ttu-id="38b3f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b3f-140">CommonParameters</span></span>
<span data-ttu-id="38b3f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38b3f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b3f-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38b3f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b3f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="38b3f-143">INPUTS</span></span>

### <span data-ttu-id="38b3f-144">System.object</span><span class="sxs-lookup"><span data-stu-id="38b3f-144">System.String</span></span>

### <span data-ttu-id="38b3f-145">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="38b3f-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="38b3f-146">輸出</span><span class="sxs-lookup"><span data-stu-id="38b3f-146">OUTPUTS</span></span>

### <span data-ttu-id="38b3f-147">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="38b3f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="38b3f-148">筆記</span><span class="sxs-lookup"><span data-stu-id="38b3f-148">NOTES</span></span>

## <span data-ttu-id="38b3f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="38b3f-149">RELATED LINKS</span></span>
