---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: f3930216e93f13004d7d2e8b149867cf511e3708
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445284"
---
# <span data-ttu-id="351d2-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="351d2-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="351d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="351d2-102">SYNOPSIS</span></span>
<span data-ttu-id="351d2-103">取得 Azure 儲存服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="351d2-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="351d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="351d2-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="351d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="351d2-105">DESCRIPTION</span></span>
<span data-ttu-id="351d2-106">**AzureStorageServiceMetricsProperty** Cmdlet 會取得 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="351d2-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="351d2-107">示例</span><span class="sxs-lookup"><span data-stu-id="351d2-107">EXAMPLES</span></span>

### <span data-ttu-id="351d2-108">範例1：取得 Blob 服務的度量屬性</span><span class="sxs-lookup"><span data-stu-id="351d2-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="351d2-109">這個命令會針對小時標準類型取得 blob 儲存空間的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="351d2-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="351d2-110">參數</span><span class="sxs-lookup"><span data-stu-id="351d2-110">PARAMETERS</span></span>

### <span data-ttu-id="351d2-111">-內容</span><span class="sxs-lookup"><span data-stu-id="351d2-111">-Context</span></span>
<span data-ttu-id="351d2-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="351d2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="351d2-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="351d2-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="351d2-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="351d2-114">-MetricsType</span></span>
<span data-ttu-id="351d2-115">指定公制類型。</span><span class="sxs-lookup"><span data-stu-id="351d2-115">Specifies a metrics type.</span></span>
<span data-ttu-id="351d2-116">這個 Cmdlet 會針對此參數指定的公制類型，取得 Azure Storage service 公制屬性。</span><span class="sxs-lookup"><span data-stu-id="351d2-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="351d2-117">此參數可接受的值為： Hour 和 Minute。</span><span class="sxs-lookup"><span data-stu-id="351d2-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="351d2-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="351d2-118">-ServiceType</span></span>
<span data-ttu-id="351d2-119">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="351d2-119">Specifies the storage service type.</span></span>
<span data-ttu-id="351d2-120">這個 Cmdlet 會取得此參數指定之類型的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="351d2-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="351d2-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="351d2-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="351d2-122">Blob</span><span class="sxs-lookup"><span data-stu-id="351d2-122">Blob</span></span> 
- <span data-ttu-id="351d2-123">張</span><span class="sxs-lookup"><span data-stu-id="351d2-123">Table</span></span>
- <span data-ttu-id="351d2-124">序列</span><span class="sxs-lookup"><span data-stu-id="351d2-124">Queue</span></span>
- <span data-ttu-id="351d2-125">檔案</span><span class="sxs-lookup"><span data-stu-id="351d2-125">File</span></span> 

<span data-ttu-id="351d2-126">目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="351d2-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="351d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="351d2-127">CommonParameters</span></span>
<span data-ttu-id="351d2-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="351d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="351d2-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="351d2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="351d2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="351d2-130">INPUTS</span></span>

### <span data-ttu-id="351d2-131">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="351d2-131">IStorageContext</span></span>

<span data-ttu-id="351d2-132">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="351d2-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="351d2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="351d2-133">OUTPUTS</span></span>

### <span data-ttu-id="351d2-134">MetricsProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="351d2-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="351d2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="351d2-135">NOTES</span></span>

## <span data-ttu-id="351d2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="351d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="351d2-137">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="351d2-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="351d2-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="351d2-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


