---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 7dd1fb194ebd14694b15914bdc9d633bb2973b20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913230"
---
# <span data-ttu-id="be615-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="be615-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="be615-102">簡介</span><span class="sxs-lookup"><span data-stu-id="be615-102">SYNOPSIS</span></span>
<span data-ttu-id="be615-103">設定或移除 Azure Data Lake Store 帳戶中檔案的到期時間。</span><span class="sxs-lookup"><span data-stu-id="be615-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="be615-104">語法</span><span class="sxs-lookup"><span data-stu-id="be615-104">SYNTAX</span></span>

### <span data-ttu-id="be615-105">SetAbsoluteNeverExpireExpiry (預設) </span><span class="sxs-lookup"><span data-stu-id="be615-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be615-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="be615-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be615-107">描述</span><span class="sxs-lookup"><span data-stu-id="be615-107">DESCRIPTION</span></span>
<span data-ttu-id="be615-108">**Set-AzDataLakeStoreItemExpiry Cmdlet** 會設定或移除 Azure Data Lake Store 帳戶中檔案的到期時間。</span><span class="sxs-lookup"><span data-stu-id="be615-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="be615-109">例子</span><span class="sxs-lookup"><span data-stu-id="be615-109">EXAMPLES</span></span>

### <span data-ttu-id="be615-110">範例 1：設定檔案的到期日</span><span class="sxs-lookup"><span data-stu-id="be615-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="be615-111">將帳戶 ContosoADL myfile.txt檔案的到期日設定為 2 小時後。</span><span class="sxs-lookup"><span data-stu-id="be615-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="be615-112">這會使檔案過期， (兩小時後) 刪除。</span><span class="sxs-lookup"><span data-stu-id="be615-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="be615-113">範例 2：移除檔案的到期日</span><span class="sxs-lookup"><span data-stu-id="be615-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="be615-114">移除先前在帳戶 "contosoADL" myfile.txt檔案中設定的任何到期日。</span><span class="sxs-lookup"><span data-stu-id="be615-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="be615-115">這表示檔案不會自動過期 (標示為刪除) 且必須手動刪除或設為再次過期。</span><span class="sxs-lookup"><span data-stu-id="be615-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="be615-116">範例 3：設定檔案相對於現在到期的時間</span><span class="sxs-lookup"><span data-stu-id="be615-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="be615-117">第一個命令會設定檔案 /myfile.txt相對於伺服器目前時間 240 秒的到期日。</span><span class="sxs-lookup"><span data-stu-id="be615-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="be615-118">第二個命令會設定檔案 /myfile.txt伺服器建立時間的相對到期日 240 秒。</span><span class="sxs-lookup"><span data-stu-id="be615-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="be615-119">參數</span><span class="sxs-lookup"><span data-stu-id="be615-119">PARAMETERS</span></span>

### <span data-ttu-id="be615-120">-帳戶</span><span class="sxs-lookup"><span data-stu-id="be615-120">-Account</span></span>
<span data-ttu-id="be615-121">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="be615-121">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be615-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be615-122">-DefaultProfile</span></span>
<span data-ttu-id="be615-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="be615-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be615-124">-到期</span><span class="sxs-lookup"><span data-stu-id="be615-124">-Expiration</span></span>
<span data-ttu-id="be615-125">指定檔案的絕對到期日。</span><span class="sxs-lookup"><span data-stu-id="be615-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="be615-126">如果沒有值或設為 MaxValue，檔案永遠不會過期。</span><span class="sxs-lookup"><span data-stu-id="be615-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be615-127">-路徑</span><span class="sxs-lookup"><span data-stu-id="be615-127">-Path</span></span>
<span data-ttu-id="be615-128">指定要設定或移除到期之檔案專案的 Data Lake Store 路徑。</span><span class="sxs-lookup"><span data-stu-id="be615-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be615-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="be615-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="be615-130">相對到期選項。</span><span class="sxs-lookup"><span data-stu-id="be615-130">Relative expiry options.</span></span> <span data-ttu-id="be615-131">RelativeToNow 或 RelativeToCreationDate 是目前的選項</span><span class="sxs-lookup"><span data-stu-id="be615-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be615-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="be615-132">-RelativeTime</span></span>
<span data-ttu-id="be615-133">相對於目前或建立時間的相對時間 ，以毫秒為單位</span><span class="sxs-lookup"><span data-stu-id="be615-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be615-134">-確認</span><span class="sxs-lookup"><span data-stu-id="be615-134">-Confirm</span></span>
<span data-ttu-id="be615-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="be615-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be615-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be615-136">-WhatIf</span></span>
<span data-ttu-id="be615-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be615-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be615-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be615-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be615-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be615-139">CommonParameters</span></span>
<span data-ttu-id="be615-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="be615-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be615-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="be615-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be615-142">輸入</span><span class="sxs-lookup"><span data-stu-id="be615-142">INPUTS</span></span>

### <span data-ttu-id="be615-143">System.String</span><span class="sxs-lookup"><span data-stu-id="be615-143">System.String</span></span>

### <span data-ttu-id="be615-144">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="be615-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="be615-145">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="be615-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="be615-146">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreEnums+PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="be615-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="be615-147">System.Int64</span><span class="sxs-lookup"><span data-stu-id="be615-147">System.Int64</span></span>

## <span data-ttu-id="be615-148">輸出</span><span class="sxs-lookup"><span data-stu-id="be615-148">OUTPUTS</span></span>

### <span data-ttu-id="be615-149">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="be615-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="be615-150">筆記</span><span class="sxs-lookup"><span data-stu-id="be615-150">NOTES</span></span>
<span data-ttu-id="be615-151">別名：Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="be615-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="be615-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="be615-152">RELATED LINKS</span></span>

[<span data-ttu-id="be615-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="be615-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

