---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 715fc15fbafe2f0ba1b4c6782bed607f9878bd55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907454"
---
# <span data-ttu-id="5b3b7-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5b3b7-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="5b3b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5b3b7-102">SYNOPSIS</span></span>
<span data-ttu-id="5b3b7-103">修改 Azure 儲存體服務的計量屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="5b3b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="5b3b7-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b3b7-105">描述</span><span class="sxs-lookup"><span data-stu-id="5b3b7-105">DESCRIPTION</span></span>
<span data-ttu-id="5b3b7-106">**Set-AzStorageServiceMetricsProperty Cmdlet** 會修改 Azure 儲存體服務的計量屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="5b3b7-107">例子</span><span class="sxs-lookup"><span data-stu-id="5b3b7-107">EXAMPLES</span></span>

### <span data-ttu-id="5b3b7-108">範例 1：修改 Blob 服務的度量屬性</span><span class="sxs-lookup"><span data-stu-id="5b3b7-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="5b3b7-109">此命令將 Blob 儲存空間的版本 1.0 計量修改為服務層級。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="5b3b7-110">Azure 儲存體服務計量會保留專案 10 天。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="5b3b7-111">由於此命令會指定 *PassThru 參數* ，因此該命令會顯示已修改的度量屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="5b3b7-112">參數</span><span class="sxs-lookup"><span data-stu-id="5b3b7-112">PARAMETERS</span></span>

### <span data-ttu-id="5b3b7-113">-內容</span><span class="sxs-lookup"><span data-stu-id="5b3b7-113">-Context</span></span>
<span data-ttu-id="5b3b7-114">指定 Azure 儲存內容。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5b3b7-115">若要取得儲存內容，請使用 New-AzStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5b3b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b3b7-116">-DefaultProfile</span></span>
<span data-ttu-id="5b3b7-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b3b7-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="5b3b7-118">-MetricsLevel</span></span>
<span data-ttu-id="5b3b7-119">指定 Azure 儲存體用於服務的計量層級。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="5b3b7-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5b3b7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b3b7-121">沒有</span><span class="sxs-lookup"><span data-stu-id="5b3b7-121">None</span></span>
- <span data-ttu-id="5b3b7-122">服務</span><span class="sxs-lookup"><span data-stu-id="5b3b7-122">Service</span></span>
- <span data-ttu-id="5b3b7-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="5b3b7-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b3b7-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="5b3b7-124">-MetricsType</span></span>
<span data-ttu-id="5b3b7-125">指定度量類型。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-125">Specifies a metrics type.</span></span>
<span data-ttu-id="5b3b7-126">此 Cmdlet 將 Azure 儲存體服務計量類型設定為此參數指定的值。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="5b3b7-127">此參數可接受的值為：小時和分鐘。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="5b3b7-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b3b7-128">-PassThru</span></span>
<span data-ttu-id="5b3b7-129">表示此 Cmdlet 會返回更新的度量屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="5b3b7-130">如果您未指定此參數，此 Cmdlet 不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5b3b7-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="5b3b7-131">-RetentionDays</span></span>
<span data-ttu-id="5b3b7-132">指定 Azure 儲存體服務保留計量資訊的天數。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="5b3b7-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5b3b7-133">-ServiceType</span></span>
<span data-ttu-id="5b3b7-134">指定儲存服務類型。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-134">Specifies the storage service type.</span></span>
<span data-ttu-id="5b3b7-135">此 Cmdlet 會修改此參數指定之服務類型的計量屬性。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="5b3b7-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5b3b7-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b3b7-137">Blob</span><span class="sxs-lookup"><span data-stu-id="5b3b7-137">Blob</span></span> 
- <span data-ttu-id="5b3b7-138">表</span><span class="sxs-lookup"><span data-stu-id="5b3b7-138">Table</span></span>
- <span data-ttu-id="5b3b7-139">佇列</span><span class="sxs-lookup"><span data-stu-id="5b3b7-139">Queue</span></span>
- <span data-ttu-id="5b3b7-140">目前不支援檔案的值。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="5b3b7-141">-版本</span><span class="sxs-lookup"><span data-stu-id="5b3b7-141">-Version</span></span>
<span data-ttu-id="5b3b7-142">指定 Azure 儲存量值的版本。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="5b3b7-143">預設值為 1.0。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="5b3b7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b3b7-144">CommonParameters</span></span>
<span data-ttu-id="5b3b7-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b3b7-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5b3b7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b3b7-147">輸入</span><span class="sxs-lookup"><span data-stu-id="5b3b7-147">INPUTS</span></span>

### <span data-ttu-id="5b3b7-148">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5b3b7-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5b3b7-149">輸出</span><span class="sxs-lookup"><span data-stu-id="5b3b7-149">OUTPUTS</span></span>

### <span data-ttu-id="5b3b7-150">Microsoft.Azure.storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="5b3b7-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="5b3b7-151">筆記</span><span class="sxs-lookup"><span data-stu-id="5b3b7-151">NOTES</span></span>

## <span data-ttu-id="5b3b7-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b3b7-152">RELATED LINKS</span></span>

[<span data-ttu-id="5b3b7-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="5b3b7-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="5b3b7-154">New-AzStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="5b3b7-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


