---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: dc7f579366956f8447ba64fc898e97f5c33b70f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792918"
---
# <span data-ttu-id="b3da7-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b3da7-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="b3da7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3da7-102">SYNOPSIS</span></span>
<span data-ttu-id="b3da7-103">修改 Azure 儲存空間服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3da7-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="b3da7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3da7-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3da7-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3da7-105">DESCRIPTION</span></span>
<span data-ttu-id="b3da7-106">**AzStorageServiceProperty** Cmdlet 會修改 Azure 儲存空間服務的屬性。</span><span class="sxs-lookup"><span data-stu-id="b3da7-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="b3da7-107">示例</span><span class="sxs-lookup"><span data-stu-id="b3da7-107">EXAMPLES</span></span>

### <span data-ttu-id="b3da7-108">範例1：將 Blob 服務 DefaultServiceVersion 設定為2017-04-17</span><span class="sxs-lookup"><span data-stu-id="b3da7-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="b3da7-109">這個命令會將 Blob 服務的 DefaultServiceVersion 設定為2017-04-17</span><span class="sxs-lookup"><span data-stu-id="b3da7-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="b3da7-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3da7-110">PARAMETERS</span></span>

### <span data-ttu-id="b3da7-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b3da7-111">-Context</span></span>
<span data-ttu-id="b3da7-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b3da7-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b3da7-113">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3da7-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b3da7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3da7-114">-DefaultProfile</span></span>
<span data-ttu-id="b3da7-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3da7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3da7-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="b3da7-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="b3da7-117">DefaultServiceVersion 表示如果未指定傳入要求的版本，則用於 Blob 服務要求的預設版本。</span><span class="sxs-lookup"><span data-stu-id="b3da7-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="b3da7-118">可能的值包括版本2008-10-27 和所有最新版本。</span><span class="sxs-lookup"><span data-stu-id="b3da7-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="b3da7-119">在中查看更多詳細資料 https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="b3da7-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="b3da7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3da7-120">-PassThru</span></span>
<span data-ttu-id="b3da7-121">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b3da7-121">Display ServiceProperties</span></span>

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

### <span data-ttu-id="b3da7-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b3da7-122">-ServiceType</span></span>
<span data-ttu-id="b3da7-123">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="b3da7-123">Specifies the storage service type.</span></span>
<span data-ttu-id="b3da7-124">這個 Cmdlet 會取得此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="b3da7-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b3da7-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b3da7-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b3da7-126">Blob</span><span class="sxs-lookup"><span data-stu-id="b3da7-126">Blob</span></span> 
- <span data-ttu-id="b3da7-127">張</span><span class="sxs-lookup"><span data-stu-id="b3da7-127">Table</span></span>
- <span data-ttu-id="b3da7-128">序列</span><span class="sxs-lookup"><span data-stu-id="b3da7-128">Queue</span></span>
- <span data-ttu-id="b3da7-129">檔案</span><span class="sxs-lookup"><span data-stu-id="b3da7-129">File</span></span>

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

### <span data-ttu-id="b3da7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b3da7-130">-Confirm</span></span>
<span data-ttu-id="b3da7-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3da7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3da7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3da7-132">-WhatIf</span></span>
<span data-ttu-id="b3da7-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3da7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3da7-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3da7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3da7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3da7-135">CommonParameters</span></span>
<span data-ttu-id="b3da7-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3da7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3da7-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3da7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3da7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b3da7-138">INPUTS</span></span>

### <span data-ttu-id="b3da7-139">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b3da7-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b3da7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b3da7-140">OUTPUTS</span></span>

### <span data-ttu-id="b3da7-141">WindowsAzure. ResourceModel.. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="b3da7-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="b3da7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b3da7-142">NOTES</span></span>

## <span data-ttu-id="b3da7-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3da7-143">RELATED LINKS</span></span>
