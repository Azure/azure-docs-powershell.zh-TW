---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: eff94aac5ac9a1a71a12f31be81a1eb4c89bf73b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909269"
---
# <span data-ttu-id="c2574-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c2574-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="c2574-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c2574-102">SYNOPSIS</span></span>
<span data-ttu-id="c2574-103">獲得 Azure 儲存體服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2574-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="c2574-104">語法</span><span class="sxs-lookup"><span data-stu-id="c2574-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2574-105">描述</span><span class="sxs-lookup"><span data-stu-id="c2574-105">DESCRIPTION</span></span>
<span data-ttu-id="c2574-106">**Get-AzStorageServiceProperty** Cmdlet 會取得 Azure 儲存體服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="c2574-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="c2574-107">例子</span><span class="sxs-lookup"><span data-stu-id="c2574-107">EXAMPLES</span></span>

### <span data-ttu-id="c2574-108">範例 1：取得 Blob 服務的 Azure 儲存體服務屬性</span><span class="sxs-lookup"><span data-stu-id="c2574-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="c2574-109">此命令會獲得 Blob 服務的 DefaultServiceVersion 屬性。</span><span class="sxs-lookup"><span data-stu-id="c2574-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="c2574-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2574-110">PARAMETERS</span></span>

### <span data-ttu-id="c2574-111">-內容</span><span class="sxs-lookup"><span data-stu-id="c2574-111">-Context</span></span>
<span data-ttu-id="c2574-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="c2574-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c2574-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2574-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c2574-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2574-114">-DefaultProfile</span></span>
<span data-ttu-id="c2574-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2574-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2574-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c2574-116">-ServiceType</span></span>
<span data-ttu-id="c2574-117">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="c2574-117">Specifies the storage service type.</span></span>
<span data-ttu-id="c2574-118">此 Cmdlet 會針對此參數指定的服務類型，獲得記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="c2574-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="c2574-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c2574-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c2574-120">Blob</span><span class="sxs-lookup"><span data-stu-id="c2574-120">Blob</span></span> 
- <span data-ttu-id="c2574-121">表</span><span class="sxs-lookup"><span data-stu-id="c2574-121">Table</span></span>
- <span data-ttu-id="c2574-122">佇列</span><span class="sxs-lookup"><span data-stu-id="c2574-122">Queue</span></span>
- <span data-ttu-id="c2574-123">檔</span><span class="sxs-lookup"><span data-stu-id="c2574-123">File</span></span>

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

### <span data-ttu-id="c2574-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2574-124">CommonParameters</span></span>
<span data-ttu-id="c2574-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c2574-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2574-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c2574-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2574-127">輸入</span><span class="sxs-lookup"><span data-stu-id="c2574-127">INPUTS</span></span>

### <span data-ttu-id="c2574-128">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="c2574-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2574-129">輸出</span><span class="sxs-lookup"><span data-stu-id="c2574-129">OUTPUTS</span></span>

### <span data-ttu-id="c2574-130">Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="c2574-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="c2574-131">筆記</span><span class="sxs-lookup"><span data-stu-id="c2574-131">NOTES</span></span>

## <span data-ttu-id="c2574-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2574-132">RELATED LINKS</span></span>
