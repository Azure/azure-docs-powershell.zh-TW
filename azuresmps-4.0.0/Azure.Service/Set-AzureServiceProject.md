---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967265"
---
# <span data-ttu-id="a184b-101">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a184b-101">Set-AzureServiceProject</span></span>

## <span data-ttu-id="a184b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a184b-102">SYNOPSIS</span></span>
<span data-ttu-id="a184b-103">為目前的服務設定預設位置、訂閱、槽及儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a184b-103">Sets default location, subscription, slot, and storage account for the current service.</span></span>

## <span data-ttu-id="a184b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a184b-104">SYNTAX</span></span>

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a184b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a184b-105">DESCRIPTION</span></span>
<span data-ttu-id="a184b-106">**AzureServiceProject** Cmdlet 會設定目前服務的部署位置、槽、儲存空間帳戶及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a184b-106">The **Set-AzureServiceProject** cmdlet sets the deployment location, slot, storage account, and subscription for the current service.</span></span>
<span data-ttu-id="a184b-107">每當服務發佈到雲端時，就會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="a184b-107">These values are used whenever the service is published to the cloud.</span></span>

## <span data-ttu-id="a184b-108">示例</span><span class="sxs-lookup"><span data-stu-id="a184b-108">EXAMPLES</span></span>

### <span data-ttu-id="a184b-109">範例1：基本設定</span><span class="sxs-lookup"><span data-stu-id="a184b-109">Example 1: Basic settings</span></span>
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

<span data-ttu-id="a184b-110">將服務的部署位置設定為北中美區域。</span><span class="sxs-lookup"><span data-stu-id="a184b-110">Sets the deployment location for the service to the North Central US region.</span></span>
<span data-ttu-id="a184b-111">將部署槽位設定為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="a184b-111">Sets the deployment slot to Production.</span></span> <span data-ttu-id="a184b-112">設定將用來將服務定義暫存至 myStorageAccount 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a184b-112">Sets the storage account that will be used to stage the service definition to myStorageAccount.</span></span>
<span data-ttu-id="a184b-113">設定將託管服務的訂閱進行 mySubscription。</span><span class="sxs-lookup"><span data-stu-id="a184b-113">Sets the subscription that will host the service to mySubscription.</span></span>
<span data-ttu-id="a184b-114">每當服務發佈到雲端時，系統會將它託管在資料中心的 [北部] 美國地區，它會更新部署槽，而且會使用指定的訂閱和儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a184b-114">Whenever the service is published to the cloud, it will be hosted in a data center in the North Central US region, it will update the deployment slot, and it will use the specified subscription and storage account.</span></span>

## <span data-ttu-id="a184b-115">參數</span><span class="sxs-lookup"><span data-stu-id="a184b-115">PARAMETERS</span></span>

### <span data-ttu-id="a184b-116">-位置</span><span class="sxs-lookup"><span data-stu-id="a184b-116">-Location</span></span>
<span data-ttu-id="a184b-117">將託管服務的地區。</span><span class="sxs-lookup"><span data-stu-id="a184b-117">The region in which the service will be hosted.</span></span>
<span data-ttu-id="a184b-118">每當服務發佈到雲端時，就會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="a184b-118">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="a184b-119">可能的值包括：亞洲、歐洲、美國、東亞、東、北部、北部、北美、美國、東南部、西歐、華南、東南部、西亞、西美、北美國、西歐、美國等。</span><span class="sxs-lookup"><span data-stu-id="a184b-119">Possible values are: Anywhere Asia, Anywhere Europe, Anywhere US, East Asia, East US, North Central US, North Europe, South Central US, Southeast Asia, West Europe, West US.</span></span>

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

### <span data-ttu-id="a184b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a184b-120">-PassThru</span></span>
<span data-ttu-id="a184b-121">表示此 Cmdlet 會傳回代表其操作專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a184b-121">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="a184b-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a184b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a184b-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a184b-123">-Profile</span></span>
<span data-ttu-id="a184b-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a184b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a184b-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a184b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a184b-126">-槽</span><span class="sxs-lookup"><span data-stu-id="a184b-126">-Slot</span></span>
<span data-ttu-id="a184b-127">要託管服務的槽 (生產或暫存) 。</span><span class="sxs-lookup"><span data-stu-id="a184b-127">The slot (production or staging) in which the service will be hosted.</span></span>
<span data-ttu-id="a184b-128">每當服務發佈到雲端時，就會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="a184b-128">This value is used whenever the service is published to the cloud.</span></span>
<span data-ttu-id="a184b-129">可能的值包括：生產、分段。</span><span class="sxs-lookup"><span data-stu-id="a184b-129">Possible values are: Production, Staging.</span></span>

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

### <span data-ttu-id="a184b-130">儲存空間</span><span class="sxs-lookup"><span data-stu-id="a184b-130">-Storage</span></span>
<span data-ttu-id="a184b-131">將服務套件上傳到雲端時要使用的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a184b-131">The storage account to be used when uploading the service package to the cloud.</span></span>
<span data-ttu-id="a184b-132">如果儲存帳戶不存在，則會在服務發佈到雲端時建立。</span><span class="sxs-lookup"><span data-stu-id="a184b-132">If the storage account doesn't exist, it will be created when the service is published to the cloud.</span></span>

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

### <span data-ttu-id="a184b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a184b-133">CommonParameters</span></span>
<span data-ttu-id="a184b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a184b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a184b-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a184b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a184b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a184b-136">INPUTS</span></span>

## <span data-ttu-id="a184b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a184b-137">OUTPUTS</span></span>

## <span data-ttu-id="a184b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="a184b-138">NOTES</span></span>
* <span data-ttu-id="a184b-139">節點開發人員、php 開發人員、python-開發人員</span><span class="sxs-lookup"><span data-stu-id="a184b-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="a184b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="a184b-140">RELATED LINKS</span></span>

[<span data-ttu-id="a184b-141">新-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a184b-141">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="a184b-142">發佈-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="a184b-142">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="a184b-143">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="a184b-143">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


