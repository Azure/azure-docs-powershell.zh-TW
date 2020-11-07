---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 1d7d536d7815206f942a89da4458f4669c0c9fd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800222"
---
# <span data-ttu-id="f8092-101">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f8092-101">Get-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="f8092-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f8092-102">SYNOPSIS</span></span>
<span data-ttu-id="f8092-103">取得 Azure 儲存服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="f8092-103">Gets metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8092-104">句法</span><span class="sxs-lookup"><span data-stu-id="f8092-104">SYNTAX</span></span>

```
Get-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8092-105">說明</span><span class="sxs-lookup"><span data-stu-id="f8092-105">DESCRIPTION</span></span>
<span data-ttu-id="f8092-106">**AzureStorageServiceMetricsProperty** Cmdlet 會取得 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="f8092-106">The **Get-AzureStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="f8092-107">示例</span><span class="sxs-lookup"><span data-stu-id="f8092-107">EXAMPLES</span></span>

### <span data-ttu-id="f8092-108">範例1：取得 Blob 服務的度量屬性</span><span class="sxs-lookup"><span data-stu-id="f8092-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="f8092-109">這個命令會針對小時標準類型取得 blob 儲存空間的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="f8092-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="f8092-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8092-110">PARAMETERS</span></span>

### <span data-ttu-id="f8092-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f8092-111">-Context</span></span>
<span data-ttu-id="f8092-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="f8092-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f8092-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8092-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f8092-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8092-114">-DefaultProfile</span></span>
<span data-ttu-id="f8092-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8092-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8092-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="f8092-116">-MetricsType</span></span>
<span data-ttu-id="f8092-117">指定公制類型。</span><span class="sxs-lookup"><span data-stu-id="f8092-117">Specifies a metrics type.</span></span>
<span data-ttu-id="f8092-118">這個 Cmdlet 會針對此參數指定的公制類型，取得 Azure Storage service 公制屬性。</span><span class="sxs-lookup"><span data-stu-id="f8092-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="f8092-119">此參數可接受的值為： Hour 和 Minute。</span><span class="sxs-lookup"><span data-stu-id="f8092-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8092-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f8092-120">-ServiceType</span></span>
<span data-ttu-id="f8092-121">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="f8092-121">Specifies the storage service type.</span></span>
<span data-ttu-id="f8092-122">這個 Cmdlet 會取得此參數指定之類型的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="f8092-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="f8092-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f8092-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f8092-124">Blob</span><span class="sxs-lookup"><span data-stu-id="f8092-124">Blob</span></span> 
- <span data-ttu-id="f8092-125">張</span><span class="sxs-lookup"><span data-stu-id="f8092-125">Table</span></span>
- <span data-ttu-id="f8092-126">序列</span><span class="sxs-lookup"><span data-stu-id="f8092-126">Queue</span></span>
- <span data-ttu-id="f8092-127">檔案目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="f8092-127">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8092-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8092-128">CommonParameters</span></span>
<span data-ttu-id="f8092-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f8092-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8092-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f8092-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8092-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f8092-131">INPUTS</span></span>

### <span data-ttu-id="f8092-132">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="f8092-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f8092-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f8092-133">OUTPUTS</span></span>

### <span data-ttu-id="f8092-134">MetricsProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="f8092-134">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="f8092-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f8092-135">NOTES</span></span>

## <span data-ttu-id="f8092-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8092-136">RELATED LINKS</span></span>

[<span data-ttu-id="f8092-137">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="f8092-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f8092-138">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="f8092-138">Set-AzureStorageServiceMetricsProperty</span></span>](./Set-AzureStorageServiceMetricsProperty.md)


