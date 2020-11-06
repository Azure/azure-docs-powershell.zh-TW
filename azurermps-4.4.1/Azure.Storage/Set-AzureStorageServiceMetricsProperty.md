---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454983"
---
# <span data-ttu-id="8a90d-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8a90d-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="8a90d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a90d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a90d-103">修改 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="8a90d-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a90d-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a90d-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="8a90d-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a90d-105">DESCRIPTION</span></span>
<span data-ttu-id="8a90d-106">**AzureStorageServiceMetricsProperty** Cmdlet 會修改 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="8a90d-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="8a90d-107">示例</span><span class="sxs-lookup"><span data-stu-id="8a90d-107">EXAMPLES</span></span>

### <span data-ttu-id="8a90d-108">範例1：修改 Blob 服務的公制屬性</span><span class="sxs-lookup"><span data-stu-id="8a90d-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="8a90d-109">這個命令會將 blob 儲存體的版本1.0 度量值修改為服務層級。</span><span class="sxs-lookup"><span data-stu-id="8a90d-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="8a90d-110">Azure 儲存服務規格會保留10天的專案。</span><span class="sxs-lookup"><span data-stu-id="8a90d-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="8a90d-111">由於這個命令會指定 *PassThru* 參數，因此命令會顯示已修改的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="8a90d-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="8a90d-112">參數</span><span class="sxs-lookup"><span data-stu-id="8a90d-112">PARAMETERS</span></span>

### <span data-ttu-id="8a90d-113">-內容</span><span class="sxs-lookup"><span data-stu-id="8a90d-113">-Context</span></span>
<span data-ttu-id="8a90d-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="8a90d-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8a90d-115">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a90d-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="8a90d-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="8a90d-116">-MetricsLevel</span></span>
<span data-ttu-id="8a90d-117">指定 Azure 儲存空間用來處理服務的指標等級。</span><span class="sxs-lookup"><span data-stu-id="8a90d-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="8a90d-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8a90d-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a90d-119">所有</span><span class="sxs-lookup"><span data-stu-id="8a90d-119">None</span></span>
- <span data-ttu-id="8a90d-120">Services</span><span class="sxs-lookup"><span data-stu-id="8a90d-120">Service</span></span>
- <span data-ttu-id="8a90d-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="8a90d-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a90d-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="8a90d-122">-MetricsType</span></span>
<span data-ttu-id="8a90d-123">指定公制類型。</span><span class="sxs-lookup"><span data-stu-id="8a90d-123">Specifies a metrics type.</span></span>
<span data-ttu-id="8a90d-124">此 cmldet 會將 Azure 儲存空間服務規格類型設定為此參數指定的值。</span><span class="sxs-lookup"><span data-stu-id="8a90d-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="8a90d-125">此參數可接受的值為： Hour 和 Minute。</span><span class="sxs-lookup"><span data-stu-id="8a90d-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a90d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a90d-126">-PassThru</span></span>
<span data-ttu-id="8a90d-127">指示這個 Cmdlet 會傳回更新的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="8a90d-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="8a90d-128">如果您沒有指定此參數，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8a90d-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="8a90d-129">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="8a90d-129">-RetentionDays</span></span>
<span data-ttu-id="8a90d-130">指定 Azure 存儲服務保留指標資訊的天數。</span><span class="sxs-lookup"><span data-stu-id="8a90d-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="8a90d-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="8a90d-131">-ServiceType</span></span>
<span data-ttu-id="8a90d-132">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="8a90d-132">Specifies the storage service type.</span></span>
<span data-ttu-id="8a90d-133">這個 Cmdlet 會修改此參數指定之服務類型的規格屬性。</span><span class="sxs-lookup"><span data-stu-id="8a90d-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="8a90d-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8a90d-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a90d-135">Blob</span><span class="sxs-lookup"><span data-stu-id="8a90d-135">Blob</span></span> 
- <span data-ttu-id="8a90d-136">張</span><span class="sxs-lookup"><span data-stu-id="8a90d-136">Table</span></span>
- <span data-ttu-id="8a90d-137">序列</span><span class="sxs-lookup"><span data-stu-id="8a90d-137">Queue</span></span>
- <span data-ttu-id="8a90d-138">檔案</span><span class="sxs-lookup"><span data-stu-id="8a90d-138">File</span></span>

<span data-ttu-id="8a90d-139">目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="8a90d-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="8a90d-140">-版本</span><span class="sxs-lookup"><span data-stu-id="8a90d-140">-Version</span></span>
<span data-ttu-id="8a90d-141">指定 Azure 儲存空間規格的版本。</span><span class="sxs-lookup"><span data-stu-id="8a90d-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="8a90d-142">預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="8a90d-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="8a90d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a90d-143">CommonParameters</span></span>
<span data-ttu-id="8a90d-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a90d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a90d-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a90d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a90d-146">輸入</span><span class="sxs-lookup"><span data-stu-id="8a90d-146">INPUTS</span></span>

### <span data-ttu-id="8a90d-147">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8a90d-147">IStorageContext</span></span>

<span data-ttu-id="8a90d-148">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="8a90d-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="8a90d-149">輸出</span><span class="sxs-lookup"><span data-stu-id="8a90d-149">OUTPUTS</span></span>

### <span data-ttu-id="8a90d-150">MetricsProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="8a90d-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="8a90d-151">筆記</span><span class="sxs-lookup"><span data-stu-id="8a90d-151">NOTES</span></span>

## <span data-ttu-id="8a90d-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a90d-152">RELATED LINKS</span></span>

[<span data-ttu-id="8a90d-153">AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="8a90d-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="8a90d-154">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8a90d-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


