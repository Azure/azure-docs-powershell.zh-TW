---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137743"
---
# <span data-ttu-id="5b335-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="5b335-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="5b335-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b335-102">SYNOPSIS</span></span>
<span data-ttu-id="5b335-103">修改 Azure 儲存空間服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b335-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="5b335-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b335-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b335-105">說明</span><span class="sxs-lookup"><span data-stu-id="5b335-105">DESCRIPTION</span></span>
<span data-ttu-id="5b335-106">**AzStorageServiceProperty** Cmdlet 會修改 Azure 儲存空間服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="5b335-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="5b335-107">示例</span><span class="sxs-lookup"><span data-stu-id="5b335-107">EXAMPLES</span></span>

### <span data-ttu-id="5b335-108">範例1：將 Blob 服務 DefaultServiceVersion 設定為2017-04-17</span><span class="sxs-lookup"><span data-stu-id="5b335-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="5b335-109">這個命令會將 Blob 服務的 DefaultServiceVersion 設定為2017-04-17</span><span class="sxs-lookup"><span data-stu-id="5b335-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="5b335-110">參數</span><span class="sxs-lookup"><span data-stu-id="5b335-110">PARAMETERS</span></span>

### <span data-ttu-id="5b335-111">-內容</span><span class="sxs-lookup"><span data-stu-id="5b335-111">-Context</span></span>
<span data-ttu-id="5b335-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="5b335-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5b335-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b335-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5b335-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b335-114">-DefaultProfile</span></span>
<span data-ttu-id="5b335-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b335-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b335-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="5b335-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="5b335-117">DefaultServiceVersion 表示如果未指定傳入要求的版本，則用於 Blob 服務要求的預設版本。</span><span class="sxs-lookup"><span data-stu-id="5b335-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="5b335-118">可能的值包括版本2008-10-27 和所有最新版本。</span><span class="sxs-lookup"><span data-stu-id="5b335-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="5b335-119">在中查看更多詳細資料 https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="5b335-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="5b335-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b335-120">-PassThru</span></span>
<span data-ttu-id="5b335-121">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="5b335-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="5b335-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5b335-122">-ServiceType</span></span>
<span data-ttu-id="5b335-123">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="5b335-123">Specifies the storage service type.</span></span>
<span data-ttu-id="5b335-124">這個 Cmdlet 會取得此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="5b335-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="5b335-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5b335-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b335-126">Blob</span><span class="sxs-lookup"><span data-stu-id="5b335-126">Blob</span></span> 
- <span data-ttu-id="5b335-127">張</span><span class="sxs-lookup"><span data-stu-id="5b335-127">Table</span></span>
- <span data-ttu-id="5b335-128">序列</span><span class="sxs-lookup"><span data-stu-id="5b335-128">Queue</span></span>
- <span data-ttu-id="5b335-129">檔案</span><span class="sxs-lookup"><span data-stu-id="5b335-129">File</span></span>

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

### <span data-ttu-id="5b335-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5b335-130">-Confirm</span></span>
<span data-ttu-id="5b335-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b335-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b335-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b335-132">-WhatIf</span></span>
<span data-ttu-id="5b335-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b335-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b335-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b335-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b335-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b335-135">CommonParameters</span></span>
<span data-ttu-id="5b335-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b335-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b335-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5b335-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b335-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5b335-138">INPUTS</span></span>

### <span data-ttu-id="5b335-139">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="5b335-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5b335-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5b335-140">OUTPUTS</span></span>

### <span data-ttu-id="5b335-141">WindowsAzure. ResourceModel.. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="5b335-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="5b335-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5b335-142">NOTES</span></span>

## <span data-ttu-id="5b335-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b335-143">RELATED LINKS</span></span>
