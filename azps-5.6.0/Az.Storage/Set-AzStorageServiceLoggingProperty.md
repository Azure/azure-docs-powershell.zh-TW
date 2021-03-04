---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 84eae2221564d1c1a569ea5469c44cb1cd628b04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907457"
---
# <span data-ttu-id="ec6dc-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ec6dc-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="ec6dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ec6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="ec6dc-103">修改 Azure 儲存體服務的記錄。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="ec6dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="ec6dc-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec6dc-105">描述</span><span class="sxs-lookup"><span data-stu-id="ec6dc-105">DESCRIPTION</span></span>
<span data-ttu-id="ec6dc-106">**Set-AzStorageServiceLoggingProperty** Cmdlet 會修改 Azure 儲存體服務的記錄。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="ec6dc-107">例子</span><span class="sxs-lookup"><span data-stu-id="ec6dc-107">EXAMPLES</span></span>

### <span data-ttu-id="ec6dc-108">範例 1：修改 Blob 服務的記錄屬性</span><span class="sxs-lookup"><span data-stu-id="ec6dc-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="ec6dc-109">此命令會修改 Blob 儲存空間的版本 1.0 記錄，以包含讀與寫作業。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="ec6dc-110">Azure 儲存體服務記錄會保留專案 10 天。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="ec6dc-111">由於此命令會指定 *PassThru 參數* ，因此該命令會顯示已修改的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="ec6dc-112">參數</span><span class="sxs-lookup"><span data-stu-id="ec6dc-112">PARAMETERS</span></span>

### <span data-ttu-id="ec6dc-113">-內容</span><span class="sxs-lookup"><span data-stu-id="ec6dc-113">-Context</span></span>
<span data-ttu-id="ec6dc-114">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ec6dc-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ec6dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec6dc-116">-DefaultProfile</span></span>
<span data-ttu-id="ec6dc-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec6dc-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="ec6dc-118">-LoggingOperations</span></span>
<span data-ttu-id="ec6dc-119">指定 Azure 儲存體服務作業的陣列。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="ec6dc-120">Azure 儲存體服務會記錄此參數指定的作業。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="ec6dc-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ec6dc-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec6dc-122">沒有</span><span class="sxs-lookup"><span data-stu-id="ec6dc-122">None</span></span>
- <span data-ttu-id="ec6dc-123">讀</span><span class="sxs-lookup"><span data-stu-id="ec6dc-123">Read</span></span>
- <span data-ttu-id="ec6dc-124">寫</span><span class="sxs-lookup"><span data-stu-id="ec6dc-124">Write</span></span>
- <span data-ttu-id="ec6dc-125">刪除</span><span class="sxs-lookup"><span data-stu-id="ec6dc-125">Delete</span></span>
- <span data-ttu-id="ec6dc-126">所有</span><span class="sxs-lookup"><span data-stu-id="ec6dc-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6dc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec6dc-127">-PassThru</span></span>
<span data-ttu-id="ec6dc-128">表示此 Cmdlet 會返回更新的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="ec6dc-129">如果您未指定此參數，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ec6dc-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="ec6dc-130">-RetentionDays</span></span>
<span data-ttu-id="ec6dc-131">指定 Azure 儲存體服務保留記錄資訊的天數。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6dc-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ec6dc-132">-ServiceType</span></span>
<span data-ttu-id="ec6dc-133">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-133">Specifies the storage service type.</span></span>
<span data-ttu-id="ec6dc-134">此 Cmdlet 會修改此參數指定之服務類型的記錄屬性。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="ec6dc-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ec6dc-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ec6dc-136">Blob</span><span class="sxs-lookup"><span data-stu-id="ec6dc-136">Blob</span></span> 
- <span data-ttu-id="ec6dc-137">表</span><span class="sxs-lookup"><span data-stu-id="ec6dc-137">Table</span></span>
- <span data-ttu-id="ec6dc-138">佇列</span><span class="sxs-lookup"><span data-stu-id="ec6dc-138">Queue</span></span>
- <span data-ttu-id="ec6dc-139">目前不支援檔案的值。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="ec6dc-140">-版本</span><span class="sxs-lookup"><span data-stu-id="ec6dc-140">-Version</span></span>
<span data-ttu-id="ec6dc-141">指定 Azure 儲存體服務記錄的版本。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="ec6dc-142">預設值為 1.0。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-142">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec6dc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec6dc-143">CommonParameters</span></span>
<span data-ttu-id="ec6dc-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec6dc-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ec6dc-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec6dc-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ec6dc-146">INPUTS</span></span>

### <span data-ttu-id="ec6dc-147">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ec6dc-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ec6dc-148">輸出</span><span class="sxs-lookup"><span data-stu-id="ec6dc-148">OUTPUTS</span></span>

### <span data-ttu-id="ec6dc-149">Microsoft.Azure.storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="ec6dc-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="ec6dc-150">筆記</span><span class="sxs-lookup"><span data-stu-id="ec6dc-150">NOTES</span></span>

## <span data-ttu-id="ec6dc-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec6dc-151">RELATED LINKS</span></span>

[<span data-ttu-id="ec6dc-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ec6dc-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="ec6dc-153">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="ec6dc-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


