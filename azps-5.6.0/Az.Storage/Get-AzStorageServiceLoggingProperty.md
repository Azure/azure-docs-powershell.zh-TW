---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d956dfd49e541751003d28c31285722616ab640
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913638"
---
# <span data-ttu-id="c6573-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c6573-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="c6573-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6573-102">SYNOPSIS</span></span>
<span data-ttu-id="c6573-103">為 Azure 儲存體服務獲取記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="c6573-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="c6573-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6573-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6573-105">描述</span><span class="sxs-lookup"><span data-stu-id="c6573-105">DESCRIPTION</span></span>
<span data-ttu-id="c6573-106">**Get-AzStorageServiceLoggingProperty** Cmdlet 會取得 Azure 儲存體服務的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="c6573-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="c6573-107">例子</span><span class="sxs-lookup"><span data-stu-id="c6573-107">EXAMPLES</span></span>

### <span data-ttu-id="c6573-108">範例 1：取得 Blob 服務的記錄屬性</span><span class="sxs-lookup"><span data-stu-id="c6573-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="c6573-109">此命令會獲得 Blob 儲存空間的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="c6573-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="c6573-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6573-110">PARAMETERS</span></span>

### <span data-ttu-id="c6573-111">-內容</span><span class="sxs-lookup"><span data-stu-id="c6573-111">-Context</span></span>
<span data-ttu-id="c6573-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="c6573-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c6573-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6573-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c6573-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6573-114">-DefaultProfile</span></span>
<span data-ttu-id="c6573-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6573-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6573-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c6573-116">-ServiceType</span></span>
<span data-ttu-id="c6573-117">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="c6573-117">Specifies the storage service type.</span></span>
<span data-ttu-id="c6573-118">此 Cmdlet 會針對此參數指定的服務類型，獲得記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="c6573-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c6573-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c6573-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6573-120">Blob</span><span class="sxs-lookup"><span data-stu-id="c6573-120">Blob</span></span> 
- <span data-ttu-id="c6573-121">表</span><span class="sxs-lookup"><span data-stu-id="c6573-121">Table</span></span>
- <span data-ttu-id="c6573-122">佇列</span><span class="sxs-lookup"><span data-stu-id="c6573-122">Queue</span></span>
- <span data-ttu-id="c6573-123">目前不支援檔案的值。</span><span class="sxs-lookup"><span data-stu-id="c6573-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="c6573-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6573-124">CommonParameters</span></span>
<span data-ttu-id="c6573-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6573-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6573-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c6573-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6573-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c6573-127">INPUTS</span></span>

### <span data-ttu-id="c6573-128">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c6573-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6573-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c6573-129">OUTPUTS</span></span>

### <span data-ttu-id="c6573-130">Microsoft.Azure.storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="c6573-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="c6573-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c6573-131">NOTES</span></span>

## <span data-ttu-id="c6573-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6573-132">RELATED LINKS</span></span>

[<span data-ttu-id="c6573-133">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c6573-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c6573-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="c6573-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


