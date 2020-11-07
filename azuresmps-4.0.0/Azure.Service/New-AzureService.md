---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BB216903-B2BB-4948-AC28-408ED6C768F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6cae249f99282006ff8636e8d727485a223e2a1d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967345"
---
# <span data-ttu-id="391c1-101">New-AzureService</span><span class="sxs-lookup"><span data-stu-id="391c1-101">New-AzureService</span></span>

## <span data-ttu-id="391c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="391c1-102">SYNOPSIS</span></span>
<span data-ttu-id="391c1-103">建立 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="391c1-103">Creates an Azure service.</span></span>

## <span data-ttu-id="391c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="391c1-104">SYNTAX</span></span>

### <span data-ttu-id="391c1-105">ParameterSetAffinityGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="391c1-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureService [-ServiceName] <String> [-AffinityGroup] <String> [[-Label] <String>]
 [[-Description] <String>] [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="391c1-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="391c1-106">ParameterSetLocation</span></span>
```
New-AzureService [-ServiceName] <String> [-Location] <String> [[-Label] <String>] [[-Description] <String>]
 [[-ReverseDnsFqdn] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="391c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="391c1-107">DESCRIPTION</span></span>
<span data-ttu-id="391c1-108">**新的-AzureService** Cmdlet 會在目前的訂閱中建立新的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="391c1-108">The **New-AzureService** cmdlet creates a new Azure service in the current subscription.</span></span>

## <span data-ttu-id="391c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="391c1-109">EXAMPLES</span></span>

### <span data-ttu-id="391c1-110">範例1：建立服務</span><span class="sxs-lookup"><span data-stu-id="391c1-110">Example 1: Create a service</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -Label "MyTestService" -Location "South Central US"
```

<span data-ttu-id="391c1-111">這個命令會在南部中美位置建立名為 MySvc01 的新服務。</span><span class="sxs-lookup"><span data-stu-id="391c1-111">This command creates a new service named MySvc01 in the South Central US location.</span></span>

### <span data-ttu-id="391c1-112">範例2：在地緣群組中建立服務</span><span class="sxs-lookup"><span data-stu-id="391c1-112">Example 2: Create a service in an affinity group</span></span>
```
PS C:\> New-AzureService -ServiceName "MySvc01" -AffinityGroup NorthRegion
```

<span data-ttu-id="391c1-113">這個命令會使用 NorthRegion 關聯群組，建立一個名為 MySvc01 的新服務。</span><span class="sxs-lookup"><span data-stu-id="391c1-113">This command creates a new service named MySvc01 using the NorthRegion affinity group.</span></span>

## <span data-ttu-id="391c1-114">參數</span><span class="sxs-lookup"><span data-stu-id="391c1-114">PARAMETERS</span></span>

### <span data-ttu-id="391c1-115">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="391c1-115">-AffinityGroup</span></span>
<span data-ttu-id="391c1-116">指定與訂閱相關聯的地緣群組。</span><span class="sxs-lookup"><span data-stu-id="391c1-116">Specifies the affinity group associated with the subscription.</span></span>
<span data-ttu-id="391c1-117">如果您沒有指定 *Location* 參數，則需要地緣群組。</span><span class="sxs-lookup"><span data-stu-id="391c1-117">If you do not specify the *Location* parameter, an affinity group is required.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391c1-118">-描述</span><span class="sxs-lookup"><span data-stu-id="391c1-118">-Description</span></span>
<span data-ttu-id="391c1-119">指定服務的描述。</span><span class="sxs-lookup"><span data-stu-id="391c1-119">Specifies a description for the service.</span></span>
<span data-ttu-id="391c1-120">描述最多可以為1024個字元。</span><span class="sxs-lookup"><span data-stu-id="391c1-120">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391c1-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="391c1-121">-InformationAction</span></span>
<span data-ttu-id="391c1-122">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="391c1-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="391c1-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="391c1-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="391c1-124">持續</span><span class="sxs-lookup"><span data-stu-id="391c1-124">Continue</span></span>
- <span data-ttu-id="391c1-125">理會</span><span class="sxs-lookup"><span data-stu-id="391c1-125">Ignore</span></span>
- <span data-ttu-id="391c1-126">看</span><span class="sxs-lookup"><span data-stu-id="391c1-126">Inquire</span></span>
- <span data-ttu-id="391c1-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="391c1-127">SilentlyContinue</span></span>
- <span data-ttu-id="391c1-128">停止</span><span class="sxs-lookup"><span data-stu-id="391c1-128">Stop</span></span>
- <span data-ttu-id="391c1-129">封存</span><span class="sxs-lookup"><span data-stu-id="391c1-129">Suspend</span></span>

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

### <span data-ttu-id="391c1-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="391c1-130">-InformationVariable</span></span>
<span data-ttu-id="391c1-131">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="391c1-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="391c1-132">-標籤</span><span class="sxs-lookup"><span data-stu-id="391c1-132">-Label</span></span>
<span data-ttu-id="391c1-133">指定服務的標籤。</span><span class="sxs-lookup"><span data-stu-id="391c1-133">Specifies a label for the service.</span></span>
<span data-ttu-id="391c1-134">標籤長度最多可為100個字元。</span><span class="sxs-lookup"><span data-stu-id="391c1-134">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="391c1-135">-位置</span><span class="sxs-lookup"><span data-stu-id="391c1-135">-Location</span></span>
<span data-ttu-id="391c1-136">指定服務的位置。</span><span class="sxs-lookup"><span data-stu-id="391c1-136">Specifies the location for the service.</span></span>
<span data-ttu-id="391c1-137">如果沒有指定的地緣群組，則需要一個位置。</span><span class="sxs-lookup"><span data-stu-id="391c1-137">A location is required if there isn't a specified Affinity Group.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391c1-138">-設定檔</span><span class="sxs-lookup"><span data-stu-id="391c1-138">-Profile</span></span>
<span data-ttu-id="391c1-139">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="391c1-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="391c1-140">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="391c1-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="391c1-141">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="391c1-141">-ReverseDnsFqdn</span></span>
<span data-ttu-id="391c1-142">指定反向 DNS 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="391c1-142">Specifies the fully qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391c1-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="391c1-143">-ServiceName</span></span>
<span data-ttu-id="391c1-144">指定新服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="391c1-144">Specifies the name of the new service.</span></span>
<span data-ttu-id="391c1-145">該名稱在訂閱中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="391c1-145">The name must be unique to the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="391c1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="391c1-146">CommonParameters</span></span>
<span data-ttu-id="391c1-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="391c1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="391c1-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="391c1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="391c1-149">輸入</span><span class="sxs-lookup"><span data-stu-id="391c1-149">INPUTS</span></span>

## <span data-ttu-id="391c1-150">輸出</span><span class="sxs-lookup"><span data-stu-id="391c1-150">OUTPUTS</span></span>

## <span data-ttu-id="391c1-151">筆記</span><span class="sxs-lookup"><span data-stu-id="391c1-151">NOTES</span></span>

## <span data-ttu-id="391c1-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="391c1-152">RELATED LINKS</span></span>

[<span data-ttu-id="391c1-153">AzureService</span><span class="sxs-lookup"><span data-stu-id="391c1-153">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="391c1-154">Set-AzureService</span><span class="sxs-lookup"><span data-stu-id="391c1-154">Set-AzureService</span></span>](./Set-AzureService.md)


