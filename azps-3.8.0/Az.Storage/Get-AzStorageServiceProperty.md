---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958222"
---
# <span data-ttu-id="a88c2-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a88c2-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="a88c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a88c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a88c2-103">取得 Azure 儲存服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="a88c2-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="a88c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a88c2-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a88c2-105">說明</span><span class="sxs-lookup"><span data-stu-id="a88c2-105">DESCRIPTION</span></span>
<span data-ttu-id="a88c2-106">**AzStorageServiceProperty** Cmdlet 會取得 Azure 儲存空間服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="a88c2-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="a88c2-107">示例</span><span class="sxs-lookup"><span data-stu-id="a88c2-107">EXAMPLES</span></span>

### <span data-ttu-id="a88c2-108">範例1：取得 Blob 服務的 Azure 儲存服務屬性</span><span class="sxs-lookup"><span data-stu-id="a88c2-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29
```

<span data-ttu-id="a88c2-109">這個命令會取得 Blob 服務的 DefaultServiceVersion 屬性。</span><span class="sxs-lookup"><span data-stu-id="a88c2-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="a88c2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a88c2-110">PARAMETERS</span></span>

### <span data-ttu-id="a88c2-111">-內容</span><span class="sxs-lookup"><span data-stu-id="a88c2-111">-Context</span></span>
<span data-ttu-id="a88c2-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="a88c2-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a88c2-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a88c2-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a88c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a88c2-114">-DefaultProfile</span></span>
<span data-ttu-id="a88c2-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a88c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a88c2-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="a88c2-116">-ServiceType</span></span>
<span data-ttu-id="a88c2-117">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="a88c2-117">Specifies the storage service type.</span></span>
<span data-ttu-id="a88c2-118">這個 Cmdlet 會取得此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="a88c2-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="a88c2-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a88c2-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a88c2-120">Blob</span><span class="sxs-lookup"><span data-stu-id="a88c2-120">Blob</span></span> 
- <span data-ttu-id="a88c2-121">張</span><span class="sxs-lookup"><span data-stu-id="a88c2-121">Table</span></span>
- <span data-ttu-id="a88c2-122">序列</span><span class="sxs-lookup"><span data-stu-id="a88c2-122">Queue</span></span>
- <span data-ttu-id="a88c2-123">檔案</span><span class="sxs-lookup"><span data-stu-id="a88c2-123">File</span></span>

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

### <span data-ttu-id="a88c2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88c2-124">CommonParameters</span></span>
<span data-ttu-id="a88c2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a88c2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a88c2-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a88c2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88c2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a88c2-127">INPUTS</span></span>

### <span data-ttu-id="a88c2-128">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="a88c2-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a88c2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a88c2-129">OUTPUTS</span></span>

### <span data-ttu-id="a88c2-130">WindowsAzure. ResourceModel.. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="a88c2-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="a88c2-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a88c2-131">NOTES</span></span>

## <span data-ttu-id="a88c2-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a88c2-132">RELATED LINKS</span></span>
