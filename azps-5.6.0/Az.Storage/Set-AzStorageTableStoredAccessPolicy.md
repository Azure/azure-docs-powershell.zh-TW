---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 576b347ad260fc95cdafe7c4a11e42246feb09ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906849"
---
# <span data-ttu-id="4ca33-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca33-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="4ca33-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4ca33-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca33-103">設定 Azure 儲存資料表的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="4ca33-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4ca33-104">語法</span><span class="sxs-lookup"><span data-stu-id="4ca33-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ca33-105">描述</span><span class="sxs-lookup"><span data-stu-id="4ca33-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca33-106">**Set-AzStorageTableStoredAccessPolicy** Cmdlet 會設定 Azure 儲存資料表的儲存存取策略。</span><span class="sxs-lookup"><span data-stu-id="4ca33-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="4ca33-107">例子</span><span class="sxs-lookup"><span data-stu-id="4ca33-107">EXAMPLES</span></span>

### <span data-ttu-id="4ca33-108">範例 1：在資料表中設定具有完整許可權的儲存存取策略</span><span class="sxs-lookup"><span data-stu-id="4ca33-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="4ca33-109">此命令會針對名為 MyTable 的儲存資料表設定名為 Policy08 的存取策略。</span><span class="sxs-lookup"><span data-stu-id="4ca33-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="4ca33-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ca33-110">PARAMETERS</span></span>

### <span data-ttu-id="4ca33-111">-內容</span><span class="sxs-lookup"><span data-stu-id="4ca33-111">-Context</span></span>
<span data-ttu-id="4ca33-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="4ca33-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4ca33-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ca33-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca33-114">-DefaultProfile</span></span>
<span data-ttu-id="4ca33-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ca33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca33-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4ca33-116">-ExpiryTime</span></span>
<span data-ttu-id="4ca33-117">指定儲存的存取策略到期的時間。</span><span class="sxs-lookup"><span data-stu-id="4ca33-117">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca33-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4ca33-118">-NoExpiryTime</span></span>
<span data-ttu-id="4ca33-119">表示存取策略沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="4ca33-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="4ca33-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="4ca33-120">-NoStartTime</span></span>
<span data-ttu-id="4ca33-121">表示開始時間設定為 $Null。</span><span class="sxs-lookup"><span data-stu-id="4ca33-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="4ca33-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="4ca33-122">-Permission</span></span>
<span data-ttu-id="4ca33-123">指定儲存存取策略中存取儲存資料表的許可權。</span><span class="sxs-lookup"><span data-stu-id="4ca33-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="4ca33-124">請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。</span><span class="sxs-lookup"><span data-stu-id="4ca33-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca33-125">-策略</span><span class="sxs-lookup"><span data-stu-id="4ca33-125">-Policy</span></span>
<span data-ttu-id="4ca33-126">指定儲存存取策略的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ca33-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca33-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4ca33-127">-StartTime</span></span>
<span data-ttu-id="4ca33-128">指定儲存的存取策略生效的時間。</span><span class="sxs-lookup"><span data-stu-id="4ca33-128">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca33-129">-表格</span><span class="sxs-lookup"><span data-stu-id="4ca33-129">-Table</span></span>
<span data-ttu-id="4ca33-130">指定 Azure 儲存資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="4ca33-130">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca33-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4ca33-131">-Confirm</span></span>
<span data-ttu-id="4ca33-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4ca33-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ca33-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca33-133">-WhatIf</span></span>
<span data-ttu-id="4ca33-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ca33-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ca33-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ca33-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ca33-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca33-136">CommonParameters</span></span>
<span data-ttu-id="4ca33-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4ca33-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca33-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4ca33-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca33-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4ca33-139">INPUTS</span></span>

### <span data-ttu-id="4ca33-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4ca33-140">System.String</span></span>

### <span data-ttu-id="4ca33-141">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="4ca33-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ca33-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4ca33-142">OUTPUTS</span></span>

### <span data-ttu-id="4ca33-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4ca33-143">System.String</span></span>

## <span data-ttu-id="4ca33-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4ca33-144">NOTES</span></span>

## <span data-ttu-id="4ca33-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ca33-145">RELATED LINKS</span></span>

[<span data-ttu-id="4ca33-146">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca33-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4ca33-147">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="4ca33-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4ca33-148">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca33-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4ca33-149">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4ca33-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
