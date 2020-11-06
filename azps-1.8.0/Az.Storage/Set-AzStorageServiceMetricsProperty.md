---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 8eaef595ff0b81485ebaf566b65b5c8374833bdd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614474"
---
# <span data-ttu-id="be26c-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="be26c-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="be26c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be26c-102">SYNOPSIS</span></span>
<span data-ttu-id="be26c-103">修改 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="be26c-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="be26c-104">句法</span><span class="sxs-lookup"><span data-stu-id="be26c-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be26c-105">說明</span><span class="sxs-lookup"><span data-stu-id="be26c-105">DESCRIPTION</span></span>
<span data-ttu-id="be26c-106">**AzStorageServiceMetricsProperty** Cmdlet 會修改 Azure 儲存空間服務的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="be26c-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="be26c-107">示例</span><span class="sxs-lookup"><span data-stu-id="be26c-107">EXAMPLES</span></span>

### <span data-ttu-id="be26c-108">範例1：修改 Blob 服務的公制屬性</span><span class="sxs-lookup"><span data-stu-id="be26c-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="be26c-109">這個命令會將 blob 儲存體的版本1.0 度量值修改為服務層級。</span><span class="sxs-lookup"><span data-stu-id="be26c-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="be26c-110">Azure 儲存服務規格會保留10天的專案。</span><span class="sxs-lookup"><span data-stu-id="be26c-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="be26c-111">由於這個命令會指定 *PassThru* 參數，因此命令會顯示已修改的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="be26c-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="be26c-112">參數</span><span class="sxs-lookup"><span data-stu-id="be26c-112">PARAMETERS</span></span>

### <span data-ttu-id="be26c-113">-內容</span><span class="sxs-lookup"><span data-stu-id="be26c-113">-Context</span></span>
<span data-ttu-id="be26c-114">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="be26c-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="be26c-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be26c-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="be26c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be26c-116">-DefaultProfile</span></span>
<span data-ttu-id="be26c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be26c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be26c-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="be26c-118">-MetricsLevel</span></span>
<span data-ttu-id="be26c-119">指定 Azure 儲存空間用來處理服務的指標等級。</span><span class="sxs-lookup"><span data-stu-id="be26c-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="be26c-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="be26c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be26c-121">所有</span><span class="sxs-lookup"><span data-stu-id="be26c-121">None</span></span>
- <span data-ttu-id="be26c-122">Services</span><span class="sxs-lookup"><span data-stu-id="be26c-122">Service</span></span>
- <span data-ttu-id="be26c-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="be26c-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be26c-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="be26c-124">-MetricsType</span></span>
<span data-ttu-id="be26c-125">指定公制類型。</span><span class="sxs-lookup"><span data-stu-id="be26c-125">Specifies a metrics type.</span></span>
<span data-ttu-id="be26c-126">此 cmldet 會將 Azure 儲存空間服務規格類型設定為此參數指定的值。</span><span class="sxs-lookup"><span data-stu-id="be26c-126">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="be26c-127">此參數可接受的值為： Hour 和 Minute。</span><span class="sxs-lookup"><span data-stu-id="be26c-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be26c-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be26c-128">-PassThru</span></span>
<span data-ttu-id="be26c-129">指示這個 Cmdlet 會傳回更新的公制屬性。</span><span class="sxs-lookup"><span data-stu-id="be26c-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="be26c-130">如果您沒有指定此參數，這個 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="be26c-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="be26c-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="be26c-131">-RetentionDays</span></span>
<span data-ttu-id="be26c-132">指定 Azure 存儲服務保留指標資訊的天數。</span><span class="sxs-lookup"><span data-stu-id="be26c-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="be26c-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="be26c-133">-ServiceType</span></span>
<span data-ttu-id="be26c-134">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="be26c-134">Specifies the storage service type.</span></span>
<span data-ttu-id="be26c-135">這個 Cmdlet 會修改此參數指定之服務類型的規格屬性。</span><span class="sxs-lookup"><span data-stu-id="be26c-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="be26c-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="be26c-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="be26c-137">Blob</span><span class="sxs-lookup"><span data-stu-id="be26c-137">Blob</span></span> 
- <span data-ttu-id="be26c-138">張</span><span class="sxs-lookup"><span data-stu-id="be26c-138">Table</span></span>
- <span data-ttu-id="be26c-139">序列</span><span class="sxs-lookup"><span data-stu-id="be26c-139">Queue</span></span>
- <span data-ttu-id="be26c-140">檔案目前不支援檔的值。</span><span class="sxs-lookup"><span data-stu-id="be26c-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="be26c-141">-版本</span><span class="sxs-lookup"><span data-stu-id="be26c-141">-Version</span></span>
<span data-ttu-id="be26c-142">指定 Azure 儲存空間規格的版本。</span><span class="sxs-lookup"><span data-stu-id="be26c-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="be26c-143">預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="be26c-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="be26c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be26c-144">CommonParameters</span></span>
<span data-ttu-id="be26c-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be26c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be26c-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be26c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be26c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="be26c-147">INPUTS</span></span>

### <span data-ttu-id="be26c-148">IStorageCoNtext 中的 [Common.]</span><span class="sxs-lookup"><span data-stu-id="be26c-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="be26c-149">輸出</span><span class="sxs-lookup"><span data-stu-id="be26c-149">OUTPUTS</span></span>

### <span data-ttu-id="be26c-150">MetricsProperties 中的 WindowsAzure。</span><span class="sxs-lookup"><span data-stu-id="be26c-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="be26c-151">筆記</span><span class="sxs-lookup"><span data-stu-id="be26c-151">NOTES</span></span>

## <span data-ttu-id="be26c-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="be26c-152">RELATED LINKS</span></span>

[<span data-ttu-id="be26c-153">AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="be26c-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="be26c-154">新-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="be26c-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


