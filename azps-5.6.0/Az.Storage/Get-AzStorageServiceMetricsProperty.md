---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 36b2251fa0fb2324a58368df75e43c9aa1480546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909273"
---
# <span data-ttu-id="2430d-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2430d-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="2430d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2430d-102">SYNOPSIS</span></span>
<span data-ttu-id="2430d-103">為 Azure 儲存體服務獲取計量屬性。</span><span class="sxs-lookup"><span data-stu-id="2430d-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="2430d-104">語法</span><span class="sxs-lookup"><span data-stu-id="2430d-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2430d-105">描述</span><span class="sxs-lookup"><span data-stu-id="2430d-105">DESCRIPTION</span></span>
<span data-ttu-id="2430d-106">**Get-AzStorageServiceMetricsProperty** Cmdlet 會取得 Azure 儲存體服務的計量屬性。</span><span class="sxs-lookup"><span data-stu-id="2430d-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="2430d-107">例子</span><span class="sxs-lookup"><span data-stu-id="2430d-107">EXAMPLES</span></span>

### <span data-ttu-id="2430d-108">範例 1：取得 Blob 服務的度量屬性</span><span class="sxs-lookup"><span data-stu-id="2430d-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="2430d-109">此命令會針對 Hour 計量類型，獲得 Blob 儲存的度量屬性。</span><span class="sxs-lookup"><span data-stu-id="2430d-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="2430d-110">參數</span><span class="sxs-lookup"><span data-stu-id="2430d-110">PARAMETERS</span></span>

### <span data-ttu-id="2430d-111">-內容</span><span class="sxs-lookup"><span data-stu-id="2430d-111">-Context</span></span>
<span data-ttu-id="2430d-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="2430d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2430d-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2430d-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2430d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2430d-114">-DefaultProfile</span></span>
<span data-ttu-id="2430d-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2430d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2430d-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="2430d-116">-MetricsType</span></span>
<span data-ttu-id="2430d-117">指定度量類型。</span><span class="sxs-lookup"><span data-stu-id="2430d-117">Specifies a metrics type.</span></span>
<span data-ttu-id="2430d-118">此 Cmdlet 會針對此參數指定的計量類型，獲得 Azure 儲存體服務計量屬性。</span><span class="sxs-lookup"><span data-stu-id="2430d-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="2430d-119">此參數可接受的值為：小時和分鐘。</span><span class="sxs-lookup"><span data-stu-id="2430d-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="2430d-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="2430d-120">-ServiceType</span></span>
<span data-ttu-id="2430d-121">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="2430d-121">Specifies the storage service type.</span></span>
<span data-ttu-id="2430d-122">此 Cmdlet 會針對此參數指定的類型，獲得度量屬性。</span><span class="sxs-lookup"><span data-stu-id="2430d-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="2430d-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2430d-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2430d-124">Blob</span><span class="sxs-lookup"><span data-stu-id="2430d-124">Blob</span></span> 
- <span data-ttu-id="2430d-125">表</span><span class="sxs-lookup"><span data-stu-id="2430d-125">Table</span></span>
- <span data-ttu-id="2430d-126">佇列</span><span class="sxs-lookup"><span data-stu-id="2430d-126">Queue</span></span>
- <span data-ttu-id="2430d-127">目前不支援檔案的值。</span><span class="sxs-lookup"><span data-stu-id="2430d-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="2430d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2430d-128">CommonParameters</span></span>
<span data-ttu-id="2430d-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2430d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2430d-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2430d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2430d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2430d-131">INPUTS</span></span>

### <span data-ttu-id="2430d-132">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2430d-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2430d-133">輸出</span><span class="sxs-lookup"><span data-stu-id="2430d-133">OUTPUTS</span></span>

### <span data-ttu-id="2430d-134">Microsoft.Azure.storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="2430d-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="2430d-135">筆記</span><span class="sxs-lookup"><span data-stu-id="2430d-135">NOTES</span></span>

## <span data-ttu-id="2430d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="2430d-136">RELATED LINKS</span></span>

[<span data-ttu-id="2430d-137">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="2430d-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="2430d-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2430d-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


