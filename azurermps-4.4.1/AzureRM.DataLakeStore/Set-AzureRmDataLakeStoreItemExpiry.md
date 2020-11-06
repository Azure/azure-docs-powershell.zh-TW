---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457608"
---
# <span data-ttu-id="70680-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="70680-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="70680-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70680-102">SYNOPSIS</span></span>
<span data-ttu-id="70680-103">針對 Azure Data Lake Store 帳戶中的檔案設定或移除到期時間。</span><span class="sxs-lookup"><span data-stu-id="70680-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70680-104">句法</span><span class="sxs-lookup"><span data-stu-id="70680-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70680-105">說明</span><span class="sxs-lookup"><span data-stu-id="70680-105">DESCRIPTION</span></span>
<span data-ttu-id="70680-106">**AzureRmDataLakeStoreItemExpiry** Cmdlet 會針對 Azure Data Lake store 帳戶中的檔案，設定或移除到期時間。</span><span class="sxs-lookup"><span data-stu-id="70680-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="70680-107">示例</span><span class="sxs-lookup"><span data-stu-id="70680-107">EXAMPLES</span></span>

### <span data-ttu-id="70680-108">範例1：設定檔案的到期時間</span><span class="sxs-lookup"><span data-stu-id="70680-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="70680-109">從現在開始，將 [帳戶 ContosoADL] 中的檔案 myfile.txt 為兩個小時。</span><span class="sxs-lookup"><span data-stu-id="70680-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="70680-110">這會造成檔案到期， (會在兩個小時內標示為刪除) 。</span><span class="sxs-lookup"><span data-stu-id="70680-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="70680-111">範例2：移除檔案的到期日</span><span class="sxs-lookup"><span data-stu-id="70680-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="70680-112">移除先前在帳戶 "ContosoADL" 中的檔案 ' myfile.txt ' 上設定的任何過期時間。</span><span class="sxs-lookup"><span data-stu-id="70680-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="70680-113">這表示檔案不會自動過期， (會將它標記為 [刪除]) 且必須手動刪除，或將它設為再次過期。</span><span class="sxs-lookup"><span data-stu-id="70680-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="70680-114">參數</span><span class="sxs-lookup"><span data-stu-id="70680-114">PARAMETERS</span></span>

### <span data-ttu-id="70680-115">-帳戶</span><span class="sxs-lookup"><span data-stu-id="70680-115">-Account</span></span>
<span data-ttu-id="70680-116">指定 Data Lake Store 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="70680-116">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="70680-117">-到期日</span><span class="sxs-lookup"><span data-stu-id="70680-117">-Expiration</span></span>
<span data-ttu-id="70680-118">指定檔案的絕對到期時間。</span><span class="sxs-lookup"><span data-stu-id="70680-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="70680-119">如果沒有值或設定為 [無法]，檔案就不會過期。</span><span class="sxs-lookup"><span data-stu-id="70680-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70680-120">-Path</span><span class="sxs-lookup"><span data-stu-id="70680-120">-Path</span></span>
<span data-ttu-id="70680-121">指定要設定或移除到期之檔專案的資料 Lake Store 路徑。</span><span class="sxs-lookup"><span data-stu-id="70680-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="70680-122">-確認</span><span class="sxs-lookup"><span data-stu-id="70680-122">-Confirm</span></span>
<span data-ttu-id="70680-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="70680-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70680-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70680-124">-WhatIf</span></span>
<span data-ttu-id="70680-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70680-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70680-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70680-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70680-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70680-127">-DefaultProfile</span></span>
<span data-ttu-id="70680-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70680-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70680-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70680-129">CommonParameters</span></span>
<span data-ttu-id="70680-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70680-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70680-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70680-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70680-132">輸入</span><span class="sxs-lookup"><span data-stu-id="70680-132">INPUTS</span></span>

## <span data-ttu-id="70680-133">輸出</span><span class="sxs-lookup"><span data-stu-id="70680-133">OUTPUTS</span></span>

### <span data-ttu-id="70680-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="70680-134">DataLakeStoreItem</span></span>
<span data-ttu-id="70680-135">已更新的檔案，包含新的到期時間。</span><span class="sxs-lookup"><span data-stu-id="70680-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="70680-136">筆記</span><span class="sxs-lookup"><span data-stu-id="70680-136">NOTES</span></span>
<span data-ttu-id="70680-137">別名： Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="70680-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="70680-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="70680-138">RELATED LINKS</span></span>

[<span data-ttu-id="70680-139">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="70680-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

