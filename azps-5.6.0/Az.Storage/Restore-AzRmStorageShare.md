---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 0ce045df6e19a964cf92d5550cfb94e30c808a3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916338"
---
# <span data-ttu-id="ea7a8-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ea7a8-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="ea7a8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea7a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7a8-103">還原已刪除的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="ea7a8-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea7a8-104">SYNTAX</span></span>

### <span data-ttu-id="ea7a8-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ea7a8-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea7a8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ea7a8-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7a8-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="ea7a8-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea7a8-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea7a8-108">DESCRIPTION</span></span>
<span data-ttu-id="ea7a8-109">如果 **已啟用共用柔刪除，Restore-AzRmStorageShare** Cmdlet 會于有效的保留天數內還原已刪除的檔案共用。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="ea7a8-110">例子</span><span class="sxs-lookup"><span data-stu-id="ea7a8-110">EXAMPLES</span></span>

### <span data-ttu-id="ea7a8-111">範例 1：移除和還原共用</span><span class="sxs-lookup"><span data-stu-id="ea7a8-111">Example 1: Remove and restore a share</span></span>
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

<span data-ttu-id="ea7a8-112">此命令會先刪除檔案共用，然後列出共用並查看已刪除的共用版本，最後將其還原回一般共用。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="ea7a8-113">刪除共用之前，需要啟用 Share Soft delete with Update-AzStorageFileServiceProperty。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="ea7a8-114">參數</span><span class="sxs-lookup"><span data-stu-id="ea7a8-114">PARAMETERS</span></span>

### <span data-ttu-id="ea7a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7a8-115">-DefaultProfile</span></span>
<span data-ttu-id="ea7a8-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea7a8-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="ea7a8-117">-DeletedShareVersion</span></span>
<span data-ttu-id="ea7a8-118">已刪除的共用版本，將會從其中還原。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-118">Deleted Share Version, which will be restored from.</span></span>

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

### <span data-ttu-id="ea7a8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea7a8-119">-InputObject</span></span>
<span data-ttu-id="ea7a8-120">已刪除 Share 物件</span><span class="sxs-lookup"><span data-stu-id="ea7a8-120">Deleted Share object</span></span>

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

### <span data-ttu-id="ea7a8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea7a8-121">-Name</span></span>
<span data-ttu-id="ea7a8-122">已刪除的共用名稱稱，將會還原。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="ea7a8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7a8-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea7a8-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea7a8-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea7a8-125">-StorageAccount</span></span>
<span data-ttu-id="ea7a8-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ea7a8-126">Storage account object</span></span>

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

### <span data-ttu-id="ea7a8-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea7a8-127">-StorageAccountName</span></span>
<span data-ttu-id="ea7a8-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="ea7a8-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ea7a8-129">-Confirm</span></span>
<span data-ttu-id="ea7a8-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7a8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7a8-131">-WhatIf</span></span>
<span data-ttu-id="ea7a8-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7a8-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7a8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7a8-134">CommonParameters</span></span>
<span data-ttu-id="ea7a8-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7a8-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ea7a8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7a8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ea7a8-137">INPUTS</span></span>

### <span data-ttu-id="ea7a8-138">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea7a8-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ea7a8-139">Microsoft.Azure.Commands.management.storage.models.PSShare</span><span class="sxs-lookup"><span data-stu-id="ea7a8-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ea7a8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ea7a8-140">OUTPUTS</span></span>

### <span data-ttu-id="ea7a8-141">Microsoft.Azure.Commands.management.storage.models.PSShare</span><span class="sxs-lookup"><span data-stu-id="ea7a8-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ea7a8-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ea7a8-142">NOTES</span></span>

## <span data-ttu-id="ea7a8-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea7a8-143">RELATED LINKS</span></span>
