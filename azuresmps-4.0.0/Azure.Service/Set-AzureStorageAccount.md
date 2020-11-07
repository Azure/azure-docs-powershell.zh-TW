---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967296"
---
# <span data-ttu-id="7be6d-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7be6d-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="7be6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7be6d-102">SYNOPSIS</span></span>
<span data-ttu-id="7be6d-103">更新 Azure 訂閱中儲存空間帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="7be6d-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="7be6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7be6d-104">SYNTAX</span></span>

### <span data-ttu-id="7be6d-105">AccountType (預設) </span><span class="sxs-lookup"><span data-stu-id="7be6d-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7be6d-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="7be6d-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7be6d-107">說明</span><span class="sxs-lookup"><span data-stu-id="7be6d-107">DESCRIPTION</span></span>
<span data-ttu-id="7be6d-108">**AzureStorageAccount** Cmdlet 會更新目前訂閱中 Azure 儲存空間帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="7be6d-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="7be6d-109">可設定的屬性為： **Label** 、 **Description** 、 **Type** 及 **GeoReplicationEnabled** 。</span><span class="sxs-lookup"><span data-stu-id="7be6d-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="7be6d-110">示例</span><span class="sxs-lookup"><span data-stu-id="7be6d-110">EXAMPLES</span></span>

### <span data-ttu-id="7be6d-111">範例1：更新儲存空間帳戶的標籤</span><span class="sxs-lookup"><span data-stu-id="7be6d-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="7be6d-112">這個命令會更新名為 ContosoStorage01 的儲存空間帳戶的 **標籤** 和 **描述** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7be6d-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="7be6d-113">範例2：針對儲存空間帳戶啟用異地複製</span><span class="sxs-lookup"><span data-stu-id="7be6d-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="7be6d-114">這個命令會將 **GeoReplicationEnabled** 屬性設為名為 ContosoStorage01 的儲存帳戶 $False。</span><span class="sxs-lookup"><span data-stu-id="7be6d-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="7be6d-115">範例3：停用儲存空間帳戶的異地複製</span><span class="sxs-lookup"><span data-stu-id="7be6d-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="7be6d-116">這個命令會將 **GeoReplicationEnabled** 屬性設為名為 ContosoStorage01 的儲存帳戶 $True。</span><span class="sxs-lookup"><span data-stu-id="7be6d-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="7be6d-117">參數</span><span class="sxs-lookup"><span data-stu-id="7be6d-117">PARAMETERS</span></span>

### <span data-ttu-id="7be6d-118">-描述</span><span class="sxs-lookup"><span data-stu-id="7be6d-118">-Description</span></span>
<span data-ttu-id="7be6d-119">指定儲存空間帳戶的描述。</span><span class="sxs-lookup"><span data-stu-id="7be6d-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="7be6d-120">描述最多可以有1024個字元。</span><span class="sxs-lookup"><span data-stu-id="7be6d-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="7be6d-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="7be6d-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="7be6d-122">指定是否在啟用 geo 複製的情況下建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="7be6d-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be6d-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7be6d-123">-InformationAction</span></span>
<span data-ttu-id="7be6d-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="7be6d-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7be6d-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7be6d-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7be6d-126">持續</span><span class="sxs-lookup"><span data-stu-id="7be6d-126">Continue</span></span>
- <span data-ttu-id="7be6d-127">理會</span><span class="sxs-lookup"><span data-stu-id="7be6d-127">Ignore</span></span>
- <span data-ttu-id="7be6d-128">看</span><span class="sxs-lookup"><span data-stu-id="7be6d-128">Inquire</span></span>
- <span data-ttu-id="7be6d-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7be6d-129">SilentlyContinue</span></span>
- <span data-ttu-id="7be6d-130">停止</span><span class="sxs-lookup"><span data-stu-id="7be6d-130">Stop</span></span>
- <span data-ttu-id="7be6d-131">封存</span><span class="sxs-lookup"><span data-stu-id="7be6d-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be6d-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7be6d-132">-InformationVariable</span></span>
<span data-ttu-id="7be6d-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="7be6d-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be6d-134">-標籤</span><span class="sxs-lookup"><span data-stu-id="7be6d-134">-Label</span></span>
<span data-ttu-id="7be6d-135">指定儲存空間帳戶的標籤。</span><span class="sxs-lookup"><span data-stu-id="7be6d-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="7be6d-136">標籤的最大長度可能為100個字元。</span><span class="sxs-lookup"><span data-stu-id="7be6d-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="7be6d-137">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7be6d-137">-Profile</span></span>
<span data-ttu-id="7be6d-138">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7be6d-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7be6d-139">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7be6d-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be6d-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7be6d-140">-StorageAccountName</span></span>
<span data-ttu-id="7be6d-141">指定此 Cmdlet 修改的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7be6d-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be6d-142">-類型</span><span class="sxs-lookup"><span data-stu-id="7be6d-142">-Type</span></span>
<span data-ttu-id="7be6d-143">指定儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="7be6d-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="7be6d-144">有效值為：</span><span class="sxs-lookup"><span data-stu-id="7be6d-144">Valid values are:</span></span> 

- <span data-ttu-id="7be6d-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="7be6d-145">Standard_LRS</span></span>
- <span data-ttu-id="7be6d-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="7be6d-146">Standard_ZRS</span></span>
- <span data-ttu-id="7be6d-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="7be6d-147">Standard_GRS</span></span>
- <span data-ttu-id="7be6d-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="7be6d-148">Standard_RAGRS</span></span>
- <span data-ttu-id="7be6d-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="7be6d-149">Premium_LRS</span></span>

<span data-ttu-id="7be6d-150">如果未指定此參數，則會 Standard_GRS 預設值。</span><span class="sxs-lookup"><span data-stu-id="7be6d-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="7be6d-151">指定 *GeoReplicationEnabled* 參數的效果與在 *Type* 參數中指定 Standard_GRS 相同。</span><span class="sxs-lookup"><span data-stu-id="7be6d-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="7be6d-152">Standard_ZRS 或 Premium_LRS 帳戶不能變更為其他帳戶類型，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="7be6d-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7be6d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7be6d-153">CommonParameters</span></span>
<span data-ttu-id="7be6d-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7be6d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7be6d-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7be6d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7be6d-156">輸入</span><span class="sxs-lookup"><span data-stu-id="7be6d-156">INPUTS</span></span>

## <span data-ttu-id="7be6d-157">輸出</span><span class="sxs-lookup"><span data-stu-id="7be6d-157">OUTPUTS</span></span>

## <span data-ttu-id="7be6d-158">筆記</span><span class="sxs-lookup"><span data-stu-id="7be6d-158">NOTES</span></span>

## <span data-ttu-id="7be6d-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="7be6d-159">RELATED LINKS</span></span>

[<span data-ttu-id="7be6d-160">AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7be6d-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="7be6d-161">新-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7be6d-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="7be6d-162">移除-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7be6d-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


