---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: ''
schema: 2.0.0
ms.openlocfilehash: b9117d5a4149842ffd136caf1c986c70a4b5e187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443428"
---
# <span data-ttu-id="23e96-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="23e96-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="23e96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23e96-102">SYNOPSIS</span></span>
<span data-ttu-id="23e96-103">取得 Azure 儲存服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="23e96-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="23e96-104">句法</span><span class="sxs-lookup"><span data-stu-id="23e96-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="23e96-105">說明</span><span class="sxs-lookup"><span data-stu-id="23e96-105">DESCRIPTION</span></span>
<span data-ttu-id="23e96-106">**AzureStorageServiceMetricsProperty** Cmdlet 會取得 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="23e96-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="23e96-107">示例</span><span class="sxs-lookup"><span data-stu-id="23e96-107">EXAMPLES</span></span>

### <span data-ttu-id="23e96-108">範例1：取得 Blob 服務的度量屬性</span><span class="sxs-lookup"><span data-stu-id="23e96-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="23e96-109">這個命令會針對小時標準類型取得 blob 儲存空間的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="23e96-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="23e96-110">參數</span><span class="sxs-lookup"><span data-stu-id="23e96-110">PARAMETERS</span></span>

### <span data-ttu-id="23e96-111">-內容</span><span class="sxs-lookup"><span data-stu-id="23e96-111">-Context</span></span>
<span data-ttu-id="23e96-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="23e96-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="23e96-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23e96-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="23e96-114">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="23e96-114">-MetricsType</span></span>
<span data-ttu-id="23e96-115">指定公制類型。</span><span class="sxs-lookup"><span data-stu-id="23e96-115">Specifies a metrics type.</span></span>
<span data-ttu-id="23e96-116">這個 Cmdlet 會針對此參數指定的公制類型，取得 Azure Storage service 公制屬性。</span><span class="sxs-lookup"><span data-stu-id="23e96-116">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="23e96-117">此參數可接受的值為： Hour 和 Minute。</span><span class="sxs-lookup"><span data-stu-id="23e96-117">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="23e96-118">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="23e96-118">-ServiceType</span></span>
<span data-ttu-id="23e96-119">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="23e96-119">Specifies the storage service type.</span></span>
<span data-ttu-id="23e96-120">這個 Cmdlet 會取得此參數指定之類型的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="23e96-120">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="23e96-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="23e96-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="23e96-122">Blob</span><span class="sxs-lookup"><span data-stu-id="23e96-122">Blob</span></span> 
- <span data-ttu-id="23e96-123">張</span><span class="sxs-lookup"><span data-stu-id="23e96-123">Table</span></span>
- <span data-ttu-id="23e96-124">序列</span><span class="sxs-lookup"><span data-stu-id="23e96-124">Queue</span></span>
- <span data-ttu-id="23e96-125">檔案</span><span class="sxs-lookup"><span data-stu-id="23e96-125">File</span></span> 

<span data-ttu-id="23e96-126">目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="23e96-126">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="23e96-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e96-127">CommonParameters</span></span>
<span data-ttu-id="23e96-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23e96-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e96-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23e96-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e96-130">輸入</span><span class="sxs-lookup"><span data-stu-id="23e96-130">INPUTS</span></span>

## <span data-ttu-id="23e96-131">輸出</span><span class="sxs-lookup"><span data-stu-id="23e96-131">OUTPUTS</span></span>

## <span data-ttu-id="23e96-132">筆記</span><span class="sxs-lookup"><span data-stu-id="23e96-132">NOTES</span></span>

## <span data-ttu-id="23e96-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="23e96-133">RELATED LINKS</span></span>

[<span data-ttu-id="23e96-134">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="23e96-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="23e96-135">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="23e96-135">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


