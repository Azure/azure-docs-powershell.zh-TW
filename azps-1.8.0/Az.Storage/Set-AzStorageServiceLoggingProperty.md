---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d671e99ed8b5c26b98b8e224728785e034e450b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614472"
---
# <span data-ttu-id="b7fc3-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b7fc3-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="b7fc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fc3-103">修改 Azure 儲存服務的記錄。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="b7fc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7fc3-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7fc3-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="b7fc3-106">**AzStorageServiceLoggingProperty** Cmdlet 會修改 Azure 儲存空間服務的記錄。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="b7fc3-107">示例</span><span class="sxs-lookup"><span data-stu-id="b7fc3-107">EXAMPLES</span></span>

### <span data-ttu-id="b7fc3-108">範例1：修改 Blob 服務的記錄摘要屬性</span><span class="sxs-lookup"><span data-stu-id="b7fc3-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="b7fc3-109">這個命令會修改 blob 儲存的版本1.0 記錄，以包含讀取和寫入操作。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="b7fc3-110">Azure 儲存服務記錄會保留10天的專案。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="b7fc3-111">由於這個命令會指定 *PassThru* 參數，因此命令會顯示已修改的記錄摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="b7fc3-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7fc3-112">PARAMETERS</span></span>

### <span data-ttu-id="b7fc3-113">-內容</span><span class="sxs-lookup"><span data-stu-id="b7fc3-113">-Context</span></span>
<span data-ttu-id="b7fc3-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b7fc3-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b7fc3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fc3-116">-DefaultProfile</span></span>
<span data-ttu-id="b7fc3-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fc3-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="b7fc3-118">-LoggingOperations</span></span>
<span data-ttu-id="b7fc3-119">指定 Azure 儲存服務作業的陣列。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="b7fc3-120">Azure 儲存服務會記錄此參數指定的操作。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="b7fc3-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b7fc3-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7fc3-122">所有</span><span class="sxs-lookup"><span data-stu-id="b7fc3-122">None</span></span>
- <span data-ttu-id="b7fc3-123">查看</span><span class="sxs-lookup"><span data-stu-id="b7fc3-123">Read</span></span>
- <span data-ttu-id="b7fc3-124">撰寫</span><span class="sxs-lookup"><span data-stu-id="b7fc3-124">Write</span></span>
- <span data-ttu-id="b7fc3-125">Delete</span><span class="sxs-lookup"><span data-stu-id="b7fc3-125">Delete</span></span>
- <span data-ttu-id="b7fc3-126">同時</span><span class="sxs-lookup"><span data-stu-id="b7fc3-126">All</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7fc3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7fc3-127">-PassThru</span></span>
<span data-ttu-id="b7fc3-128">表示此 Cmdlet 會傳回更新的記錄摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="b7fc3-129">如果您沒有指定此參數，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b7fc3-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="b7fc3-130">-RetentionDays</span></span>
<span data-ttu-id="b7fc3-131">指定 Azure 儲存服務保留記錄資訊的天數。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="b7fc3-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b7fc3-132">-ServiceType</span></span>
<span data-ttu-id="b7fc3-133">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-133">Specifies the storage service type.</span></span>
<span data-ttu-id="b7fc3-134">這個 Cmdlet 會修改此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b7fc3-135">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b7fc3-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7fc3-136">Blob</span><span class="sxs-lookup"><span data-stu-id="b7fc3-136">Blob</span></span> 
- <span data-ttu-id="b7fc3-137">張</span><span class="sxs-lookup"><span data-stu-id="b7fc3-137">Table</span></span>
- <span data-ttu-id="b7fc3-138">序列</span><span class="sxs-lookup"><span data-stu-id="b7fc3-138">Queue</span></span>
- <span data-ttu-id="b7fc3-139">檔案目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="b7fc3-140">-版本</span><span class="sxs-lookup"><span data-stu-id="b7fc3-140">-Version</span></span>
<span data-ttu-id="b7fc3-141">指定 Azure 儲存空間服務記錄的版本。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="b7fc3-142">預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="b7fc3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fc3-143">CommonParameters</span></span>
<span data-ttu-id="b7fc3-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fc3-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fc3-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b7fc3-146">INPUTS</span></span>

### <span data-ttu-id="b7fc3-147">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="b7fc3-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b7fc3-148">輸出</span><span class="sxs-lookup"><span data-stu-id="b7fc3-148">OUTPUTS</span></span>

### <span data-ttu-id="b7fc3-149">LoggingProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="b7fc3-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="b7fc3-150">筆記</span><span class="sxs-lookup"><span data-stu-id="b7fc3-150">NOTES</span></span>

## <span data-ttu-id="b7fc3-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7fc3-151">RELATED LINKS</span></span>

[<span data-ttu-id="b7fc3-152">AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b7fc3-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="b7fc3-153">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="b7fc3-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


