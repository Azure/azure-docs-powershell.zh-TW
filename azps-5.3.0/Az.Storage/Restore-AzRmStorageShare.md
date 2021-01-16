---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448004"
---
# <span data-ttu-id="f1f47-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f1f47-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="f1f47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1f47-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f47-103">還原已刪除的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="f1f47-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="f1f47-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1f47-104">SYNTAX</span></span>

### <span data-ttu-id="f1f47-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="f1f47-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f1f47-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f1f47-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1f47-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="f1f47-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1f47-108">說明</span><span class="sxs-lookup"><span data-stu-id="f1f47-108">DESCRIPTION</span></span>
<span data-ttu-id="f1f47-109">如果啟用 [共用虛刪除]， **Restore-AzRmStorageShare** Cmdlet 會在有效的保留天數內還原已刪除的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="f1f47-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="f1f47-110">示例</span><span class="sxs-lookup"><span data-stu-id="f1f47-110">EXAMPLES</span></span>

### <span data-ttu-id="f1f47-111">範例1：移除並還原共用</span><span class="sxs-lookup"><span data-stu-id="f1f47-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="f1f47-112">這個命令會先刪除檔案共用，然後列出 [共用] 並查看已刪除的共用版本，最後再將它還原為 [標準] 共用。</span><span class="sxs-lookup"><span data-stu-id="f1f47-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="f1f47-113">需要啟用 AzStorageFileServiceProperty 的 [共用虛刪除]，再刪除 [共用]。</span><span class="sxs-lookup"><span data-stu-id="f1f47-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="f1f47-114">參數</span><span class="sxs-lookup"><span data-stu-id="f1f47-114">PARAMETERS</span></span>

### <span data-ttu-id="f1f47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1f47-115">-DefaultProfile</span></span>
<span data-ttu-id="f1f47-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1f47-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1f47-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="f1f47-117">-DeletedShareVersion</span></span>
<span data-ttu-id="f1f47-118">已刪除的共用版本，將會從此還原。</span><span class="sxs-lookup"><span data-stu-id="f1f47-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1f47-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1f47-119">-InputObject</span></span>
<span data-ttu-id="f1f47-120">已刪除的共用物件</span><span class="sxs-lookup"><span data-stu-id="f1f47-120">Deleted Share object</span></span>

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

### <span data-ttu-id="f1f47-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1f47-121">-Name</span></span>
<span data-ttu-id="f1f47-122">已刪除的共用名稱稱將會還原。</span><span class="sxs-lookup"><span data-stu-id="f1f47-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="f1f47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f47-123">-ResourceGroupName</span></span>
<span data-ttu-id="f1f47-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f1f47-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1f47-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1f47-125">-StorageAccount</span></span>
<span data-ttu-id="f1f47-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="f1f47-126">Storage account object</span></span>

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

### <span data-ttu-id="f1f47-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1f47-127">-StorageAccountName</span></span>
<span data-ttu-id="f1f47-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f1f47-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="f1f47-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f1f47-129">-Confirm</span></span>
<span data-ttu-id="f1f47-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1f47-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1f47-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1f47-131">-WhatIf</span></span>
<span data-ttu-id="f1f47-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1f47-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1f47-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1f47-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1f47-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f47-134">CommonParameters</span></span>
<span data-ttu-id="f1f47-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1f47-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f47-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1f47-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f47-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f1f47-137">INPUTS</span></span>

### <span data-ttu-id="f1f47-138">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f1f47-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f1f47-139">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f1f47-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f1f47-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f1f47-140">OUTPUTS</span></span>

### <span data-ttu-id="f1f47-141">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f1f47-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f1f47-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f1f47-142">NOTES</span></span>

## <span data-ttu-id="f1f47-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1f47-143">RELATED LINKS</span></span>
