---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966938"
---
# <span data-ttu-id="560f9-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="560f9-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="560f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="560f9-102">SYNOPSIS</span></span>
<span data-ttu-id="560f9-103">從目前的 Azure 訂閱刪除網路設定。</span><span class="sxs-lookup"><span data-stu-id="560f9-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="560f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="560f9-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="560f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="560f9-105">DESCRIPTION</span></span>
<span data-ttu-id="560f9-106">**AzureVNetConfig** Cmdlet 會從目前的 Azure 訂閱中移除所有虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="560f9-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="560f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="560f9-107">EXAMPLES</span></span>

### <span data-ttu-id="560f9-108">範例1：從目前的訂閱中移除虛擬網路設定</span><span class="sxs-lookup"><span data-stu-id="560f9-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="560f9-109">這個命令會從目前的訂閱中移除虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="560f9-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="560f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="560f9-110">PARAMETERS</span></span>

### <span data-ttu-id="560f9-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="560f9-111">-InformationAction</span></span>
<span data-ttu-id="560f9-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="560f9-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="560f9-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="560f9-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="560f9-114">持續</span><span class="sxs-lookup"><span data-stu-id="560f9-114">Continue</span></span>
- <span data-ttu-id="560f9-115">理會</span><span class="sxs-lookup"><span data-stu-id="560f9-115">Ignore</span></span>
- <span data-ttu-id="560f9-116">看</span><span class="sxs-lookup"><span data-stu-id="560f9-116">Inquire</span></span>
- <span data-ttu-id="560f9-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="560f9-117">SilentlyContinue</span></span>
- <span data-ttu-id="560f9-118">停止</span><span class="sxs-lookup"><span data-stu-id="560f9-118">Stop</span></span>
- <span data-ttu-id="560f9-119">封存</span><span class="sxs-lookup"><span data-stu-id="560f9-119">Suspend</span></span>

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

### <span data-ttu-id="560f9-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="560f9-120">-InformationVariable</span></span>
<span data-ttu-id="560f9-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="560f9-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="560f9-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="560f9-122">-Profile</span></span>
<span data-ttu-id="560f9-123">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="560f9-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="560f9-124">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="560f9-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="560f9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560f9-125">CommonParameters</span></span>
<span data-ttu-id="560f9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="560f9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560f9-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="560f9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560f9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="560f9-128">INPUTS</span></span>

## <span data-ttu-id="560f9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="560f9-129">OUTPUTS</span></span>

## <span data-ttu-id="560f9-130">筆記</span><span class="sxs-lookup"><span data-stu-id="560f9-130">NOTES</span></span>

## <span data-ttu-id="560f9-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="560f9-131">RELATED LINKS</span></span>

[<span data-ttu-id="560f9-132">AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="560f9-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="560f9-133">AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="560f9-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="560f9-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="560f9-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


