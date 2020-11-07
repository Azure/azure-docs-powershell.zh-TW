---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967117"
---
# <span data-ttu-id="4336e-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4336e-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="4336e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4336e-102">SYNOPSIS</span></span>
<span data-ttu-id="4336e-103">取得 Azure 地緣群組物件。</span><span class="sxs-lookup"><span data-stu-id="4336e-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="4336e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4336e-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4336e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4336e-105">DESCRIPTION</span></span>
<span data-ttu-id="4336e-106">**AzureAffinityGroup** Cmdlet 會取得 Azure 地緣群組。</span><span class="sxs-lookup"><span data-stu-id="4336e-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="4336e-107">地緣群組物件包含地緣群組名稱、位置、標籤、描述，以及屬於地緣群組的儲存與託管服務。</span><span class="sxs-lookup"><span data-stu-id="4336e-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="4336e-108">示例</span><span class="sxs-lookup"><span data-stu-id="4336e-108">EXAMPLES</span></span>

### <span data-ttu-id="4336e-109">範例1：取得地緣群組的屬性</span><span class="sxs-lookup"><span data-stu-id="4336e-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="4336e-110">這個命令會取得名為 South01 的地緣群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="4336e-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="4336e-111">參數</span><span class="sxs-lookup"><span data-stu-id="4336e-111">PARAMETERS</span></span>

### <span data-ttu-id="4336e-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4336e-112">-InformationAction</span></span>
<span data-ttu-id="4336e-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="4336e-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4336e-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4336e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4336e-115">持續</span><span class="sxs-lookup"><span data-stu-id="4336e-115">Continue</span></span>
- <span data-ttu-id="4336e-116">理會</span><span class="sxs-lookup"><span data-stu-id="4336e-116">Ignore</span></span>
- <span data-ttu-id="4336e-117">看</span><span class="sxs-lookup"><span data-stu-id="4336e-117">Inquire</span></span>
- <span data-ttu-id="4336e-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4336e-118">SilentlyContinue</span></span>
- <span data-ttu-id="4336e-119">停止</span><span class="sxs-lookup"><span data-stu-id="4336e-119">Stop</span></span>
- <span data-ttu-id="4336e-120">封存</span><span class="sxs-lookup"><span data-stu-id="4336e-120">Suspend</span></span>

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

### <span data-ttu-id="4336e-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4336e-121">-InformationVariable</span></span>
<span data-ttu-id="4336e-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="4336e-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4336e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4336e-123">-Name</span></span>
<span data-ttu-id="4336e-124">指定此 Cmdlet 所取得之地緣群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4336e-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="4336e-125">透過管理入口網站建立之地緣群組的名稱通常是 Guid。</span><span class="sxs-lookup"><span data-stu-id="4336e-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="4336e-126">管理埠會顯示地緣群組標籤。</span><span class="sxs-lookup"><span data-stu-id="4336e-126">The Management Port shows the affinity group label.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4336e-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4336e-127">-Profile</span></span>
<span data-ttu-id="4336e-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4336e-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4336e-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4336e-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4336e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4336e-130">CommonParameters</span></span>
<span data-ttu-id="4336e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4336e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4336e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4336e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4336e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="4336e-133">INPUTS</span></span>

## <span data-ttu-id="4336e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4336e-134">OUTPUTS</span></span>

### <span data-ttu-id="4336e-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4336e-135">AffinityGroup</span></span>

## <span data-ttu-id="4336e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4336e-136">NOTES</span></span>

## <span data-ttu-id="4336e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="4336e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4336e-138">新-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4336e-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="4336e-139">移除-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4336e-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="4336e-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="4336e-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


