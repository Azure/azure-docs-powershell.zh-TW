---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: 074e6224c7a5b1ea1e8039901b75d223581495d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612745"
---
# <span data-ttu-id="6678e-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6678e-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="6678e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6678e-102">SYNOPSIS</span></span>
<span data-ttu-id="6678e-103">針對 Azure Data Lake Store 帳戶中的檔案設定或移除到期時間。</span><span class="sxs-lookup"><span data-stu-id="6678e-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6678e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6678e-104">SYNTAX</span></span>

### <span data-ttu-id="6678e-105">SetAbsoluteNeverExpireExpiry (預設) </span><span class="sxs-lookup"><span data-stu-id="6678e-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6678e-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="6678e-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6678e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6678e-107">DESCRIPTION</span></span>
<span data-ttu-id="6678e-108">**AzDataLakeStoreItemExpiry** Cmdlet 會針對 Azure Data Lake store 帳戶中的檔案，設定或移除到期時間。</span><span class="sxs-lookup"><span data-stu-id="6678e-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="6678e-109">示例</span><span class="sxs-lookup"><span data-stu-id="6678e-109">EXAMPLES</span></span>

### <span data-ttu-id="6678e-110">範例1：設定檔案的到期時間</span><span class="sxs-lookup"><span data-stu-id="6678e-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="6678e-111">從現在開始，將 [帳戶 ContosoADL] 中的檔案 myfile.txt 為兩個小時。</span><span class="sxs-lookup"><span data-stu-id="6678e-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="6678e-112">這會造成檔案到期， (會在兩個小時內標示為刪除) 。</span><span class="sxs-lookup"><span data-stu-id="6678e-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="6678e-113">範例2：移除檔案的到期日</span><span class="sxs-lookup"><span data-stu-id="6678e-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="6678e-114">移除先前在帳戶 "ContosoADL" 中的檔案 ' myfile.txt ' 上設定的任何過期時間。</span><span class="sxs-lookup"><span data-stu-id="6678e-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="6678e-115">這表示檔案不會自動過期， (會將它標記為 [刪除]) 且必須手動刪除，或將它設為再次過期。</span><span class="sxs-lookup"><span data-stu-id="6678e-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="6678e-116">範例3：設定檔案的過期時間相對於目前為止</span><span class="sxs-lookup"><span data-stu-id="6678e-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="6678e-117">第一個命令會設定檔案的到期時間/myfile.txt 240 秒（相對於伺服器上的目前時間）。</span><span class="sxs-lookup"><span data-stu-id="6678e-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="6678e-118">第二個命令會設定檔案的到期時間/myfile.txt 240 秒（相對於伺服器的建立時間）。</span><span class="sxs-lookup"><span data-stu-id="6678e-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="6678e-119">參數</span><span class="sxs-lookup"><span data-stu-id="6678e-119">PARAMETERS</span></span>

### <span data-ttu-id="6678e-120">-帳戶</span><span class="sxs-lookup"><span data-stu-id="6678e-120">-Account</span></span>
<span data-ttu-id="6678e-121">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6678e-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="6678e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6678e-122">-DefaultProfile</span></span>
<span data-ttu-id="6678e-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6678e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6678e-124">-到期日</span><span class="sxs-lookup"><span data-stu-id="6678e-124">-Expiration</span></span>
<span data-ttu-id="6678e-125">指定檔案的絕對到期時間。</span><span class="sxs-lookup"><span data-stu-id="6678e-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="6678e-126">如果沒有值或設定為 [無法]，檔案就不會過期。</span><span class="sxs-lookup"><span data-stu-id="6678e-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="6678e-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6678e-127">-Path</span></span>
<span data-ttu-id="6678e-128">指定要設定或移除到期之檔專案的資料 Lake Store 路徑。</span><span class="sxs-lookup"><span data-stu-id="6678e-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="6678e-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="6678e-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="6678e-130">相對到期選項。</span><span class="sxs-lookup"><span data-stu-id="6678e-130">Relative expiry options.</span></span> <span data-ttu-id="6678e-131">RelativeToNow 或 RelativeToCreationDate 是目前的選項</span><span class="sxs-lookup"><span data-stu-id="6678e-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="6678e-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="6678e-132">-RelativeTime</span></span>
<span data-ttu-id="6678e-133">現在或建立時間的相對時間（以毫秒為單位）</span><span class="sxs-lookup"><span data-stu-id="6678e-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="6678e-134">-確認</span><span class="sxs-lookup"><span data-stu-id="6678e-134">-Confirm</span></span>
<span data-ttu-id="6678e-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6678e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6678e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6678e-136">-WhatIf</span></span>
<span data-ttu-id="6678e-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6678e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6678e-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6678e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6678e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6678e-139">CommonParameters</span></span>
<span data-ttu-id="6678e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6678e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6678e-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6678e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6678e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6678e-142">INPUTS</span></span>

### <span data-ttu-id="6678e-143">System.object</span><span class="sxs-lookup"><span data-stu-id="6678e-143">System.String</span></span>

### <span data-ttu-id="6678e-144">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="6678e-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6678e-145">System.object</span><span class="sxs-lookup"><span data-stu-id="6678e-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="6678e-146">DataLakeStoreEnums + PathRelativeExpiryOptions （DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="6678e-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="6678e-147">System.object</span><span class="sxs-lookup"><span data-stu-id="6678e-147">System.Int64</span></span>

## <span data-ttu-id="6678e-148">輸出</span><span class="sxs-lookup"><span data-stu-id="6678e-148">OUTPUTS</span></span>

### <span data-ttu-id="6678e-149">DataLakeStoreItem 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="6678e-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="6678e-150">筆記</span><span class="sxs-lookup"><span data-stu-id="6678e-150">NOTES</span></span>
<span data-ttu-id="6678e-151">別名： Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="6678e-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="6678e-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="6678e-152">RELATED LINKS</span></span>

[<span data-ttu-id="6678e-153">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6678e-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

