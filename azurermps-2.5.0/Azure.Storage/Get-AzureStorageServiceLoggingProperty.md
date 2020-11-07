---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800225"
---
# <span data-ttu-id="b210a-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b210a-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="b210a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b210a-102">SYNOPSIS</span></span>
<span data-ttu-id="b210a-103">取得 Azure 儲存服務的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="b210a-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b210a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b210a-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b210a-105">說明</span><span class="sxs-lookup"><span data-stu-id="b210a-105">DESCRIPTION</span></span>
<span data-ttu-id="b210a-106">**AzureStorageServiceLoggingProperty** Cmdlet 會取得 Azure 儲存空間服務的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="b210a-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="b210a-107">示例</span><span class="sxs-lookup"><span data-stu-id="b210a-107">EXAMPLES</span></span>

### <span data-ttu-id="b210a-108">範例1：取得 Blob 服務的記錄摘要資訊</span><span class="sxs-lookup"><span data-stu-id="b210a-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="b210a-109">這個命令會取得 blob 儲存空間的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="b210a-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="b210a-110">參數</span><span class="sxs-lookup"><span data-stu-id="b210a-110">PARAMETERS</span></span>

### <span data-ttu-id="b210a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b210a-111">-Context</span></span>
<span data-ttu-id="b210a-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b210a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b210a-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b210a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b210a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b210a-114">-DefaultProfile</span></span>
<span data-ttu-id="b210a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b210a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b210a-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b210a-116">-ServiceType</span></span>
<span data-ttu-id="b210a-117">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="b210a-117">Specifies the storage service type.</span></span>
<span data-ttu-id="b210a-118">這個 Cmdlet 會取得此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="b210a-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b210a-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b210a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b210a-120">Blob</span><span class="sxs-lookup"><span data-stu-id="b210a-120">Blob</span></span> 
- <span data-ttu-id="b210a-121">張</span><span class="sxs-lookup"><span data-stu-id="b210a-121">Table</span></span>
- <span data-ttu-id="b210a-122">序列</span><span class="sxs-lookup"><span data-stu-id="b210a-122">Queue</span></span>
- <span data-ttu-id="b210a-123">檔案目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="b210a-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="b210a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b210a-124">CommonParameters</span></span>
<span data-ttu-id="b210a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b210a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b210a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b210a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b210a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b210a-127">INPUTS</span></span>

### <span data-ttu-id="b210a-128">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b210a-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b210a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b210a-129">OUTPUTS</span></span>

### <span data-ttu-id="b210a-130">LoggingProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="b210a-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="b210a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b210a-131">NOTES</span></span>

## <span data-ttu-id="b210a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b210a-132">RELATED LINKS</span></span>

[<span data-ttu-id="b210a-133">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b210a-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b210a-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b210a-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


