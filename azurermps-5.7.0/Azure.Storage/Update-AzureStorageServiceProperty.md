---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Update-AzureStorageServiceProperty.md
ms.openlocfilehash: 7036f12b4ab47043b69fe4164ac567f4355a51ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453231"
---
# <span data-ttu-id="bc534-101">Update-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bc534-101">Update-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="bc534-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc534-102">SYNOPSIS</span></span>
<span data-ttu-id="bc534-103">修改 Azure 儲存空間服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc534-103">Modifies the properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc534-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc534-104">SYNTAX</span></span>

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc534-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc534-105">DESCRIPTION</span></span>
<span data-ttu-id="bc534-106">**AzureStorageServiceProperty** Cmdlet 會修改 Azure 儲存空間服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc534-106">The **Update-AzureStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="bc534-107">示例</span><span class="sxs-lookup"><span data-stu-id="bc534-107">EXAMPLES</span></span>

### <span data-ttu-id="bc534-108">範例1：將 Blob 服務 DefaultServiceVersion 設定為2017-04-17</span><span class="sxs-lookup"><span data-stu-id="bc534-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="bc534-109">這個命令會將 Blob 服務的 DefaultServiceVersion 設定為2017-04-17</span><span class="sxs-lookup"><span data-stu-id="bc534-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="bc534-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc534-110">PARAMETERS</span></span>

### <span data-ttu-id="bc534-111">-內容</span><span class="sxs-lookup"><span data-stu-id="bc534-111">-Context</span></span>
<span data-ttu-id="bc534-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="bc534-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bc534-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc534-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bc534-114">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="bc534-114">-DefaultServiceVersion</span></span>
<span data-ttu-id="bc534-115">DefaultServiceVersion 表示如果未指定傳入要求的版本，則用於 Blob 服務要求的預設版本。</span><span class="sxs-lookup"><span data-stu-id="bc534-115">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="bc534-116">可能的值包括版本2008-10-27 和所有最新版本。</span><span class="sxs-lookup"><span data-stu-id="bc534-116">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="bc534-117">在中查看更多詳細資料 https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span><span class="sxs-lookup"><span data-stu-id="bc534-117">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc534-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc534-118">-PassThru</span></span>
<span data-ttu-id="bc534-119">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bc534-119">Display ServiceProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc534-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bc534-120">-ServiceType</span></span>
<span data-ttu-id="bc534-121">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="bc534-121">Specifies the storage service type.</span></span>
<span data-ttu-id="bc534-122">這個 Cmdlet 會取得此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="bc534-122">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="bc534-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bc534-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc534-124">Blob</span><span class="sxs-lookup"><span data-stu-id="bc534-124">Blob</span></span> 
- <span data-ttu-id="bc534-125">張</span><span class="sxs-lookup"><span data-stu-id="bc534-125">Table</span></span>
- <span data-ttu-id="bc534-126">序列</span><span class="sxs-lookup"><span data-stu-id="bc534-126">Queue</span></span>
- <span data-ttu-id="bc534-127">檔案</span><span class="sxs-lookup"><span data-stu-id="bc534-127">File</span></span>

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

### <span data-ttu-id="bc534-128">-確認</span><span class="sxs-lookup"><span data-stu-id="bc534-128">-Confirm</span></span>
<span data-ttu-id="bc534-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc534-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc534-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc534-130">-WhatIf</span></span>
<span data-ttu-id="bc534-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc534-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc534-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc534-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc534-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc534-133">CommonParameters</span></span>
<span data-ttu-id="bc534-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc534-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc534-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc534-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc534-136">輸入</span><span class="sxs-lookup"><span data-stu-id="bc534-136">INPUTS</span></span>

### <span data-ttu-id="bc534-137">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="bc534-137">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bc534-138">輸出</span><span class="sxs-lookup"><span data-stu-id="bc534-138">OUTPUTS</span></span>

### <span data-ttu-id="bc534-139">WindowsAzure. ResourceModel.. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="bc534-139">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="bc534-140">筆記</span><span class="sxs-lookup"><span data-stu-id="bc534-140">NOTES</span></span>

## <span data-ttu-id="bc534-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc534-141">RELATED LINKS</span></span>

