---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443548"
---
# <span data-ttu-id="bb380-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bb380-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="bb380-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb380-102">SYNOPSIS</span></span>
<span data-ttu-id="bb380-103">修改 Azure 儲存服務的記錄。</span><span class="sxs-lookup"><span data-stu-id="bb380-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="bb380-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb380-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb380-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb380-105">DESCRIPTION</span></span>
<span data-ttu-id="bb380-106">**AzureStorageServiceLoggingProperty** Cmdlet 會修改 Azure 儲存空間服務的記錄。</span><span class="sxs-lookup"><span data-stu-id="bb380-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="bb380-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb380-107">EXAMPLES</span></span>

### <span data-ttu-id="bb380-108">範例1：修改 Blob 服務的記錄摘要屬性</span><span class="sxs-lookup"><span data-stu-id="bb380-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="bb380-109">這個命令會修改 blob 儲存的版本1.0 記錄，以包含讀取和寫入操作。</span><span class="sxs-lookup"><span data-stu-id="bb380-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="bb380-110">Azure 儲存服務記錄會保留10天的專案。</span><span class="sxs-lookup"><span data-stu-id="bb380-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="bb380-111">由於這個命令會指定 *PassThru* 參數，因此命令會顯示已修改的記錄摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="bb380-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="bb380-112">參數</span><span class="sxs-lookup"><span data-stu-id="bb380-112">PARAMETERS</span></span>

### <span data-ttu-id="bb380-113">-內容</span><span class="sxs-lookup"><span data-stu-id="bb380-113">-Context</span></span>
<span data-ttu-id="bb380-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="bb380-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bb380-115">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb380-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bb380-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="bb380-116">-LoggingOperations</span></span>
<span data-ttu-id="bb380-117">指定 Azure 儲存服務作業的陣列。</span><span class="sxs-lookup"><span data-stu-id="bb380-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="bb380-118">Azure 儲存服務會記錄此參數指定的操作。</span><span class="sxs-lookup"><span data-stu-id="bb380-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="bb380-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bb380-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bb380-120">所有</span><span class="sxs-lookup"><span data-stu-id="bb380-120">None</span></span>
- <span data-ttu-id="bb380-121">查看</span><span class="sxs-lookup"><span data-stu-id="bb380-121">Read</span></span>
- <span data-ttu-id="bb380-122">撰寫</span><span class="sxs-lookup"><span data-stu-id="bb380-122">Write</span></span>
- <span data-ttu-id="bb380-123">Delete</span><span class="sxs-lookup"><span data-stu-id="bb380-123">Delete</span></span>
- <span data-ttu-id="bb380-124">同時</span><span class="sxs-lookup"><span data-stu-id="bb380-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb380-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb380-125">-PassThru</span></span>
<span data-ttu-id="bb380-126">表示此 Cmdlet 會傳回更新的記錄摘要屬性。</span><span class="sxs-lookup"><span data-stu-id="bb380-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="bb380-127">如果您沒有指定此參數，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bb380-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="bb380-128">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="bb380-128">-RetentionDays</span></span>
<span data-ttu-id="bb380-129">指定 Azure 儲存服務保留記錄資訊的天數。</span><span class="sxs-lookup"><span data-stu-id="bb380-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb380-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bb380-130">-ServiceType</span></span>
<span data-ttu-id="bb380-131">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="bb380-131">Specifies the storage service type.</span></span>
<span data-ttu-id="bb380-132">這個 Cmdlet 會修改此參數指定之服務類型的記錄摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="bb380-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="bb380-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bb380-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bb380-134">Blob</span><span class="sxs-lookup"><span data-stu-id="bb380-134">Blob</span></span> 
- <span data-ttu-id="bb380-135">張</span><span class="sxs-lookup"><span data-stu-id="bb380-135">Table</span></span>
- <span data-ttu-id="bb380-136">序列</span><span class="sxs-lookup"><span data-stu-id="bb380-136">Queue</span></span>
- <span data-ttu-id="bb380-137">檔案</span><span class="sxs-lookup"><span data-stu-id="bb380-137">File</span></span>

<span data-ttu-id="bb380-138">目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="bb380-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="bb380-139">-版本</span><span class="sxs-lookup"><span data-stu-id="bb380-139">-Version</span></span>
<span data-ttu-id="bb380-140">指定 Azure 儲存空間服務記錄的版本。</span><span class="sxs-lookup"><span data-stu-id="bb380-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="bb380-141">預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="bb380-141">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb380-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb380-142">CommonParameters</span></span>
<span data-ttu-id="bb380-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb380-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb380-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb380-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb380-145">輸入</span><span class="sxs-lookup"><span data-stu-id="bb380-145">INPUTS</span></span>

## <span data-ttu-id="bb380-146">輸出</span><span class="sxs-lookup"><span data-stu-id="bb380-146">OUTPUTS</span></span>

## <span data-ttu-id="bb380-147">筆記</span><span class="sxs-lookup"><span data-stu-id="bb380-147">NOTES</span></span>

## <span data-ttu-id="bb380-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb380-148">RELATED LINKS</span></span>

[<span data-ttu-id="bb380-149">AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bb380-149">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="bb380-150">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="bb380-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


