---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: d0edbcc3b519f9600a2ad36832dee0305ce49be7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447888"
---
# <span data-ttu-id="ce939-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ce939-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="ce939-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce939-102">SYNOPSIS</span></span>
<span data-ttu-id="ce939-103">取得 Azure 儲存服務的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="ce939-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce939-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce939-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce939-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce939-105">DESCRIPTION</span></span>
<span data-ttu-id="ce939-106">**AzureStorageServiceLoggingProperty** Cmdlet 會取得 Azure 儲存空間服務的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="ce939-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ce939-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce939-107">EXAMPLES</span></span>

### <span data-ttu-id="ce939-108">範例1：取得 Blob 服務的記錄摘要資訊</span><span class="sxs-lookup"><span data-stu-id="ce939-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="ce939-109">這個命令會取得 blob 儲存空間的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="ce939-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="ce939-110">參數</span><span class="sxs-lookup"><span data-stu-id="ce939-110">PARAMETERS</span></span>

### <span data-ttu-id="ce939-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ce939-111">-Context</span></span>
<span data-ttu-id="ce939-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ce939-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ce939-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce939-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ce939-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ce939-114">-ServiceType</span></span>
<span data-ttu-id="ce939-115">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="ce939-115">Specifies the storage service type.</span></span>
<span data-ttu-id="ce939-116">這個 Cmdlet 會取得此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="ce939-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ce939-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ce939-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ce939-118">Blob</span><span class="sxs-lookup"><span data-stu-id="ce939-118">Blob</span></span> 
- <span data-ttu-id="ce939-119">張</span><span class="sxs-lookup"><span data-stu-id="ce939-119">Table</span></span>
- <span data-ttu-id="ce939-120">序列</span><span class="sxs-lookup"><span data-stu-id="ce939-120">Queue</span></span>
- <span data-ttu-id="ce939-121">檔案</span><span class="sxs-lookup"><span data-stu-id="ce939-121">File</span></span>

<span data-ttu-id="ce939-122">目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="ce939-122">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce939-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce939-123">CommonParameters</span></span>
<span data-ttu-id="ce939-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce939-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce939-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce939-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce939-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ce939-126">INPUTS</span></span>

### <span data-ttu-id="ce939-127">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ce939-127">IStorageContext</span></span>

<span data-ttu-id="ce939-128">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ce939-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="ce939-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ce939-129">OUTPUTS</span></span>

### <span data-ttu-id="ce939-130">LoggingProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="ce939-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="ce939-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ce939-131">NOTES</span></span>

## <span data-ttu-id="ce939-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce939-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce939-133">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ce939-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ce939-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ce939-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


