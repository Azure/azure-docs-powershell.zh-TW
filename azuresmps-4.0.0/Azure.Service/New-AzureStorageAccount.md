---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967650"
---
# <span data-ttu-id="bf494-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf494-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="bf494-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf494-102">SYNOPSIS</span></span>
<span data-ttu-id="bf494-103">在 Azure 訂閱中建立新的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="bf494-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="bf494-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf494-104">SYNTAX</span></span>

### <span data-ttu-id="bf494-105">ParameterSetAffinityGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="bf494-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="bf494-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="bf494-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf494-107">說明</span><span class="sxs-lookup"><span data-stu-id="bf494-107">DESCRIPTION</span></span>
<span data-ttu-id="bf494-108">**新的-AzureStorageAccount** Cmdlet 會建立可提供 Azure 儲存服務存取權的帳戶。</span><span class="sxs-lookup"><span data-stu-id="bf494-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="bf494-109">儲存空間帳戶是儲存系統中的全域唯一資源。</span><span class="sxs-lookup"><span data-stu-id="bf494-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="bf494-110">[帳戶] 是 [Blob]、[佇列] 和 [資料表服務] 的父命名空間。</span><span class="sxs-lookup"><span data-stu-id="bf494-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="bf494-111">示例</span><span class="sxs-lookup"><span data-stu-id="bf494-111">EXAMPLES</span></span>

### <span data-ttu-id="bf494-112">範例1：為指定的地緣群組建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="bf494-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="bf494-113">這個命令會為指定的地緣群組建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="bf494-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="bf494-114">範例2：在指定位置建立儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="bf494-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="bf494-115">這個命令會在指定的位置建立儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="bf494-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="bf494-116">參數</span><span class="sxs-lookup"><span data-stu-id="bf494-116">PARAMETERS</span></span>

### <span data-ttu-id="bf494-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="bf494-117">-AffinityGroup</span></span>
<span data-ttu-id="bf494-118">指定目前訂閱中現有地緣群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf494-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="bf494-119">您可以指定 *Location* 或 *AffinityGroup* 參數，但不能同時指定兩者。</span><span class="sxs-lookup"><span data-stu-id="bf494-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf494-120">-描述</span><span class="sxs-lookup"><span data-stu-id="bf494-120">-Description</span></span>
<span data-ttu-id="bf494-121">指定儲存空間帳戶的描述。</span><span class="sxs-lookup"><span data-stu-id="bf494-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="bf494-122">描述最多可以為1024個字元。</span><span class="sxs-lookup"><span data-stu-id="bf494-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf494-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bf494-123">-InformationAction</span></span>
<span data-ttu-id="bf494-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="bf494-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf494-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bf494-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf494-126">持續</span><span class="sxs-lookup"><span data-stu-id="bf494-126">Continue</span></span>
- <span data-ttu-id="bf494-127">理會</span><span class="sxs-lookup"><span data-stu-id="bf494-127">Ignore</span></span>
- <span data-ttu-id="bf494-128">看</span><span class="sxs-lookup"><span data-stu-id="bf494-128">Inquire</span></span>
- <span data-ttu-id="bf494-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf494-129">SilentlyContinue</span></span>
- <span data-ttu-id="bf494-130">停止</span><span class="sxs-lookup"><span data-stu-id="bf494-130">Stop</span></span>
- <span data-ttu-id="bf494-131">封存</span><span class="sxs-lookup"><span data-stu-id="bf494-131">Suspend</span></span>

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

### <span data-ttu-id="bf494-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf494-132">-InformationVariable</span></span>
<span data-ttu-id="bf494-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="bf494-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf494-134">-標籤</span><span class="sxs-lookup"><span data-stu-id="bf494-134">-Label</span></span>
<span data-ttu-id="bf494-135">指定儲存空間帳戶的標籤。</span><span class="sxs-lookup"><span data-stu-id="bf494-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="bf494-136">標籤長度最多可為100個字元。</span><span class="sxs-lookup"><span data-stu-id="bf494-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf494-137">-位置</span><span class="sxs-lookup"><span data-stu-id="bf494-137">-Location</span></span>
<span data-ttu-id="bf494-138">指定建立儲存空間帳戶的 Azure 資料中心位置。</span><span class="sxs-lookup"><span data-stu-id="bf494-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="bf494-139">您可以包含 *Location* 或 *AffinityGroup* 參數，但不能同時包含兩者。</span><span class="sxs-lookup"><span data-stu-id="bf494-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf494-140">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bf494-140">-Profile</span></span>
<span data-ttu-id="bf494-141">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bf494-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf494-142">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bf494-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf494-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bf494-143">-StorageAccountName</span></span>
<span data-ttu-id="bf494-144">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf494-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="bf494-145">儲存空間帳戶名稱在 Azure 中必須是唯一的，而且長度必須介於3到24個字元，且只能使用小寫字母和數位。</span><span class="sxs-lookup"><span data-stu-id="bf494-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf494-146">-類型</span><span class="sxs-lookup"><span data-stu-id="bf494-146">-Type</span></span>
<span data-ttu-id="bf494-147">指定儲存空間帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="bf494-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="bf494-148">有效值為：</span><span class="sxs-lookup"><span data-stu-id="bf494-148">Valid values are:</span></span>

- <span data-ttu-id="bf494-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="bf494-149">Standard_LRS</span></span>
- <span data-ttu-id="bf494-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="bf494-150">Standard_ZRS</span></span>
- <span data-ttu-id="bf494-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="bf494-151">Standard_GRS</span></span>
- <span data-ttu-id="bf494-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="bf494-152">Standard_RAGRS</span></span>
- <span data-ttu-id="bf494-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="bf494-153">Premium_LRS</span></span>

<span data-ttu-id="bf494-154">如果未指定此參數，則會 Standard_GRS 預設值。</span><span class="sxs-lookup"><span data-stu-id="bf494-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="bf494-155">Standard_ZRS 或 Premium_LRS 帳戶不能變更為其他帳戶類型，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="bf494-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

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

### <span data-ttu-id="bf494-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf494-156">CommonParameters</span></span>
<span data-ttu-id="bf494-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf494-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf494-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf494-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf494-159">輸入</span><span class="sxs-lookup"><span data-stu-id="bf494-159">INPUTS</span></span>

## <span data-ttu-id="bf494-160">輸出</span><span class="sxs-lookup"><span data-stu-id="bf494-160">OUTPUTS</span></span>

## <span data-ttu-id="bf494-161">筆記</span><span class="sxs-lookup"><span data-stu-id="bf494-161">NOTES</span></span>

## <span data-ttu-id="bf494-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf494-162">RELATED LINKS</span></span>

[<span data-ttu-id="bf494-163">AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf494-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="bf494-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bf494-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


