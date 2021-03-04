---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: 952f66bfffef4d8f7636098a8280cd26b6fc7f5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907225"
---
# <span data-ttu-id="aaf9f-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="aaf9f-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="aaf9f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aaf9f-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf9f-103">修改 Azure 儲存體服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="aaf9f-104">語法</span><span class="sxs-lookup"><span data-stu-id="aaf9f-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aaf9f-105">描述</span><span class="sxs-lookup"><span data-stu-id="aaf9f-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf9f-106">**Update-AzStorageServiceProperty** Cmdlet 會修改 Azure 儲存體服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="aaf9f-107">例子</span><span class="sxs-lookup"><span data-stu-id="aaf9f-107">EXAMPLES</span></span>

### <span data-ttu-id="aaf9f-108">範例 1：將 Blob 服務 DefaultServiceVersion 設定為 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="aaf9f-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="aaf9f-109">此命令將 Blob 服務的 DefaultServiceVersion 設為 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="aaf9f-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="aaf9f-110">參數</span><span class="sxs-lookup"><span data-stu-id="aaf9f-110">PARAMETERS</span></span>

### <span data-ttu-id="aaf9f-111">-內容</span><span class="sxs-lookup"><span data-stu-id="aaf9f-111">-Context</span></span>
<span data-ttu-id="aaf9f-112">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aaf9f-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aaf9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf9f-114">-DefaultProfile</span></span>
<span data-ttu-id="aaf9f-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf9f-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="aaf9f-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="aaf9f-117">如果未指定傳入要求的版本，DefaultServiceVersion 會指出要求 Blob 服務的預設版本。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="aaf9f-118">可能的值包括版本 2008-10-27 以及所有較新版本。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="aaf9f-119">查看更多詳細資料，請參閱 https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="aaf9f-119">See more details in https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf9f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaf9f-120">-PassThru</span></span>
<span data-ttu-id="aaf9f-121">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="aaf9f-121">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf9f-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="aaf9f-122">-ServiceType</span></span>
<span data-ttu-id="aaf9f-123">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-123">Specifies the storage service type.</span></span>
<span data-ttu-id="aaf9f-124">此 Cmdlet 會針對此參數指定的服務類型，獲得記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="aaf9f-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="aaf9f-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aaf9f-126">Blob</span><span class="sxs-lookup"><span data-stu-id="aaf9f-126">Blob</span></span> 
- <span data-ttu-id="aaf9f-127">表</span><span class="sxs-lookup"><span data-stu-id="aaf9f-127">Table</span></span>
- <span data-ttu-id="aaf9f-128">佇列</span><span class="sxs-lookup"><span data-stu-id="aaf9f-128">Queue</span></span>
- <span data-ttu-id="aaf9f-129">檔</span><span class="sxs-lookup"><span data-stu-id="aaf9f-129">File</span></span>

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

### <span data-ttu-id="aaf9f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="aaf9f-130">-Confirm</span></span>
<span data-ttu-id="aaf9f-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf9f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf9f-132">-WhatIf</span></span>
<span data-ttu-id="aaf9f-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaf9f-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaf9f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf9f-135">CommonParameters</span></span>
<span data-ttu-id="aaf9f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf9f-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="aaf9f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf9f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="aaf9f-138">INPUTS</span></span>

### <span data-ttu-id="aaf9f-139">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="aaf9f-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aaf9f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="aaf9f-140">OUTPUTS</span></span>

### <span data-ttu-id="aaf9f-141">Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="aaf9f-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="aaf9f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="aaf9f-142">NOTES</span></span>

## <span data-ttu-id="aaf9f-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="aaf9f-143">RELATED LINKS</span></span>
