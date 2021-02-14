---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127322"
---
# <span data-ttu-id="ecac5-101">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ecac5-101">Get-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="ecac5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecac5-102">SYNOPSIS</span></span>
<span data-ttu-id="ecac5-103">取得 Azure 儲存服務的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="ecac5-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ecac5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecac5-104">SYNTAX</span></span>

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecac5-105">說明</span><span class="sxs-lookup"><span data-stu-id="ecac5-105">DESCRIPTION</span></span>
<span data-ttu-id="ecac5-106">**AzStorageServiceLoggingProperty** Cmdlet 會取得 Azure 儲存空間服務的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="ecac5-106">The **Get-AzStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="ecac5-107">示例</span><span class="sxs-lookup"><span data-stu-id="ecac5-107">EXAMPLES</span></span>

### <span data-ttu-id="ecac5-108">範例1：取得 Blob 服務的記錄摘要資訊</span><span class="sxs-lookup"><span data-stu-id="ecac5-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="ecac5-109">這個命令會取得 blob 儲存空間的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="ecac5-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="ecac5-110">參數</span><span class="sxs-lookup"><span data-stu-id="ecac5-110">PARAMETERS</span></span>

### <span data-ttu-id="ecac5-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ecac5-111">-Context</span></span>
<span data-ttu-id="ecac5-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="ecac5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ecac5-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ecac5-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ecac5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecac5-114">-DefaultProfile</span></span>
<span data-ttu-id="ecac5-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecac5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecac5-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ecac5-116">-ServiceType</span></span>
<span data-ttu-id="ecac5-117">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="ecac5-117">Specifies the storage service type.</span></span>
<span data-ttu-id="ecac5-118">這個 Cmdlet 會取得此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="ecac5-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ecac5-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ecac5-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ecac5-120">Blob</span><span class="sxs-lookup"><span data-stu-id="ecac5-120">Blob</span></span> 
- <span data-ttu-id="ecac5-121">張</span><span class="sxs-lookup"><span data-stu-id="ecac5-121">Table</span></span>
- <span data-ttu-id="ecac5-122">序列</span><span class="sxs-lookup"><span data-stu-id="ecac5-122">Queue</span></span>
- <span data-ttu-id="ecac5-123">檔案目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="ecac5-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ecac5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecac5-124">CommonParameters</span></span>
<span data-ttu-id="ecac5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecac5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecac5-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ecac5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecac5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ecac5-127">INPUTS</span></span>

### <span data-ttu-id="ecac5-128">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="ecac5-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ecac5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="ecac5-129">OUTPUTS</span></span>

### <span data-ttu-id="ecac5-130">LoggingProperties （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="ecac5-130">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="ecac5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ecac5-131">NOTES</span></span>

## <span data-ttu-id="ecac5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecac5-132">RELATED LINKS</span></span>

[<span data-ttu-id="ecac5-133">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ecac5-133">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ecac5-134">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ecac5-134">Set-AzStorageServiceLoggingProperty</span></span>](./Set-AzStorageServiceLoggingProperty.md)


