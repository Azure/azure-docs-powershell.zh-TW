---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: fe98eee14797ff26c39b003d8ab1c9826c8ec687
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795029"
---
# <span data-ttu-id="6ebc9-101">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ebc9-101">Set-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="6ebc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ebc9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebc9-103">設定 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="6ebc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ebc9-104">SYNTAX</span></span>

```
Set-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ebc9-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ebc9-105">DESCRIPTION</span></span>
<span data-ttu-id="6ebc9-106">**AzStorageTableStoredAccessPolicy** Cmdlet 設定 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-106">The **Set-AzStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="6ebc9-107">示例</span><span class="sxs-lookup"><span data-stu-id="6ebc9-107">EXAMPLES</span></span>

### <span data-ttu-id="6ebc9-108">範例1：以完整許可權在資料表中設定儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="6ebc9-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="6ebc9-109">這個命令會為名為 MyTable 的儲存空間資料表設定一個名為 Policy08 的存取原則。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="6ebc9-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ebc9-110">PARAMETERS</span></span>

### <span data-ttu-id="6ebc9-111">-內容</span><span class="sxs-lookup"><span data-stu-id="6ebc9-111">-Context</span></span>
<span data-ttu-id="6ebc9-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ebc9-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6ebc9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebc9-114">-DefaultProfile</span></span>
<span data-ttu-id="6ebc9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebc9-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6ebc9-116">-ExpiryTime</span></span>
<span data-ttu-id="6ebc9-117">指定儲存的存取原則到期的時間。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-117">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="6ebc9-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6ebc9-118">-NoExpiryTime</span></span>
<span data-ttu-id="6ebc9-119">指示存取原則沒有到期日。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="6ebc9-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="6ebc9-120">-NoStartTime</span></span>
<span data-ttu-id="6ebc9-121">表示 [開始時間] 設定為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-121">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="6ebc9-122">-許可權</span><span class="sxs-lookup"><span data-stu-id="6ebc9-122">-Permission</span></span>
<span data-ttu-id="6ebc9-123">指定儲存的存取原則中的許可權來存取儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-123">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="6ebc9-124">請務必注意，這是字串，就像是 `rwd` 讀取、寫入及刪除) 的 (。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="6ebc9-125">-原則</span><span class="sxs-lookup"><span data-stu-id="6ebc9-125">-Policy</span></span>
<span data-ttu-id="6ebc9-126">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="6ebc9-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6ebc9-127">-StartTime</span></span>
<span data-ttu-id="6ebc9-128">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-128">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="6ebc9-129">-資料表</span><span class="sxs-lookup"><span data-stu-id="6ebc9-129">-Table</span></span>
<span data-ttu-id="6ebc9-130">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-130">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="6ebc9-131">-確認</span><span class="sxs-lookup"><span data-stu-id="6ebc9-131">-Confirm</span></span>
<span data-ttu-id="6ebc9-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ebc9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebc9-133">-WhatIf</span></span>
<span data-ttu-id="6ebc9-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ebc9-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ebc9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebc9-136">CommonParameters</span></span>
<span data-ttu-id="6ebc9-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebc9-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ebc9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebc9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6ebc9-139">INPUTS</span></span>

### <span data-ttu-id="6ebc9-140">System.object</span><span class="sxs-lookup"><span data-stu-id="6ebc9-140">System.String</span></span>

### <span data-ttu-id="6ebc9-141">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="6ebc9-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ebc9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6ebc9-142">OUTPUTS</span></span>

### <span data-ttu-id="6ebc9-143">System.object</span><span class="sxs-lookup"><span data-stu-id="6ebc9-143">System.String</span></span>

## <span data-ttu-id="6ebc9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6ebc9-144">NOTES</span></span>

## <span data-ttu-id="6ebc9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ebc9-145">RELATED LINKS</span></span>

[<span data-ttu-id="6ebc9-146">AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ebc9-146">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6ebc9-147">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="6ebc9-147">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="6ebc9-148">新-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ebc9-148">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="6ebc9-149">移除-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6ebc9-149">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)
