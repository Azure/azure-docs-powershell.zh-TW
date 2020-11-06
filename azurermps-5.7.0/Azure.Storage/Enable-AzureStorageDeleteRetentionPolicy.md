---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446595"
---
# <span data-ttu-id="b21ac-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b21ac-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="b21ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b21ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b21ac-103">針對 Azure Storage Blob 服務啟用刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="b21ac-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b21ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="b21ac-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b21ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="b21ac-105">DESCRIPTION</span></span>
<span data-ttu-id="b21ac-106">**Enable-AzureStorageDeleteRetentionPolicy** Cmdlet 會啟用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="b21ac-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b21ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="b21ac-107">EXAMPLES</span></span>

### <span data-ttu-id="b21ac-108">範例1：啟用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="b21ac-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="b21ac-109">這個命令會啟用 Blob 服務的 [刪除保留原則]，並將 [刪除的 blob 保留天數] 設定為3。</span><span class="sxs-lookup"><span data-stu-id="b21ac-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="b21ac-110">參數</span><span class="sxs-lookup"><span data-stu-id="b21ac-110">PARAMETERS</span></span>

### <span data-ttu-id="b21ac-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b21ac-111">-Context</span></span>
<span data-ttu-id="b21ac-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="b21ac-112">Azure Storage Context Object</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b21ac-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b21ac-113">-PassThru</span></span>
<span data-ttu-id="b21ac-114">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="b21ac-114">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ac-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="b21ac-115">-RetentionDays</span></span>
<span data-ttu-id="b21ac-116">設定 DeleteRetentionPolicy 的保留天數。</span><span class="sxs-lookup"><span data-stu-id="b21ac-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ac-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b21ac-117">-Confirm</span></span>
<span data-ttu-id="b21ac-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b21ac-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ac-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b21ac-119">-WhatIf</span></span>
<span data-ttu-id="b21ac-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b21ac-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b21ac-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b21ac-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b21ac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b21ac-122">CommonParameters</span></span>
<span data-ttu-id="b21ac-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b21ac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b21ac-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b21ac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b21ac-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b21ac-125">INPUTS</span></span>

### <span data-ttu-id="b21ac-126">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b21ac-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b21ac-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b21ac-127">OUTPUTS</span></span>

### <span data-ttu-id="b21ac-128">DeleteRetentionPolicyProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="b21ac-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="b21ac-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b21ac-129">NOTES</span></span>

## <span data-ttu-id="b21ac-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b21ac-130">RELATED LINKS</span></span>

