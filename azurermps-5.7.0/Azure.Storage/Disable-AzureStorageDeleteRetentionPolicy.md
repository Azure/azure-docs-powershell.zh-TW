---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623628"
---
# <span data-ttu-id="e9ff9-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="e9ff9-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="e9ff9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ff9-103">停用 Azure Storage Blob 服務的 [刪除保留原則]。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9ff9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9ff9-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9ff9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ff9-106">**Disable AzureStorageDeleteRetentionPolicy** Cmdlet 會停用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="e9ff9-107">示例</span><span class="sxs-lookup"><span data-stu-id="e9ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="e9ff9-108">範例1：停用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="e9ff9-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="e9ff9-109">這個命令會停用 [刪除 Blob 服務的保留原則]。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="e9ff9-110">參數</span><span class="sxs-lookup"><span data-stu-id="e9ff9-110">PARAMETERS</span></span>

### <span data-ttu-id="e9ff9-111">-內容</span><span class="sxs-lookup"><span data-stu-id="e9ff9-111">-Context</span></span>
<span data-ttu-id="e9ff9-112">Azure 儲存區內容物件</span><span class="sxs-lookup"><span data-stu-id="e9ff9-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e9ff9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9ff9-113">-PassThru</span></span>
<span data-ttu-id="e9ff9-114">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="e9ff9-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="e9ff9-115">-確認</span><span class="sxs-lookup"><span data-stu-id="e9ff9-115">-Confirm</span></span>
<span data-ttu-id="e9ff9-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ff9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ff9-117">-WhatIf</span></span>
<span data-ttu-id="e9ff9-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9ff9-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ff9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ff9-120">CommonParameters</span></span>
<span data-ttu-id="e9ff9-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ff9-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9ff9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ff9-123">輸入</span><span class="sxs-lookup"><span data-stu-id="e9ff9-123">INPUTS</span></span>

### <span data-ttu-id="e9ff9-124">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="e9ff9-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9ff9-125">輸出</span><span class="sxs-lookup"><span data-stu-id="e9ff9-125">OUTPUTS</span></span>

### <span data-ttu-id="e9ff9-126">WindowsAzure. ResourceMode.. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="e9ff9-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="e9ff9-127">筆記</span><span class="sxs-lookup"><span data-stu-id="e9ff9-127">NOTES</span></span>

## <span data-ttu-id="e9ff9-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9ff9-128">RELATED LINKS</span></span>

