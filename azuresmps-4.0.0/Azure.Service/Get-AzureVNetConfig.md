---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967734"
---
# <span data-ttu-id="9cc94-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="9cc94-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="9cc94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cc94-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc94-103">從目前的訂閱取得 Azure 虛擬網路配置。</span><span class="sxs-lookup"><span data-stu-id="9cc94-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="9cc94-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cc94-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9cc94-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cc94-105">DESCRIPTION</span></span>
<span data-ttu-id="9cc94-106">**AzureVNetConfig** Cmdlet 會檢索目前 Azure 訂閱的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="9cc94-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="9cc94-107">如果指定了 *ExportToFile* 參數，則會建立網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="9cc94-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="9cc94-108">示例</span><span class="sxs-lookup"><span data-stu-id="9cc94-108">EXAMPLES</span></span>

### <span data-ttu-id="9cc94-109">範例1：取得目前 Azure 訂閱的虛擬網路設定</span><span class="sxs-lookup"><span data-stu-id="9cc94-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="9cc94-110">這個命令會取得目前 Azure 訂閱的虛擬網路設定，並顯示它。</span><span class="sxs-lookup"><span data-stu-id="9cc94-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="9cc94-111">範例2：取得目前 Azure 訂閱的虛擬網路設定並將它儲存到本機檔案</span><span class="sxs-lookup"><span data-stu-id="9cc94-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="9cc94-112">這個命令會取得目前 Azure 訂閱的虛擬網路設定，然後將它儲存到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="9cc94-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="9cc94-113">參數</span><span class="sxs-lookup"><span data-stu-id="9cc94-113">PARAMETERS</span></span>

### <span data-ttu-id="9cc94-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="9cc94-114">-ExportToFile</span></span>
<span data-ttu-id="9cc94-115">指定要從 [設定] 中建立之網路設定檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="9cc94-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

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

### <span data-ttu-id="9cc94-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9cc94-116">-InformationAction</span></span>
<span data-ttu-id="9cc94-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9cc94-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9cc94-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9cc94-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9cc94-119">持續</span><span class="sxs-lookup"><span data-stu-id="9cc94-119">Continue</span></span>
- <span data-ttu-id="9cc94-120">理會</span><span class="sxs-lookup"><span data-stu-id="9cc94-120">Ignore</span></span>
- <span data-ttu-id="9cc94-121">看</span><span class="sxs-lookup"><span data-stu-id="9cc94-121">Inquire</span></span>
- <span data-ttu-id="9cc94-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9cc94-122">SilentlyContinue</span></span>
- <span data-ttu-id="9cc94-123">停止</span><span class="sxs-lookup"><span data-stu-id="9cc94-123">Stop</span></span>
- <span data-ttu-id="9cc94-124">封存</span><span class="sxs-lookup"><span data-stu-id="9cc94-124">Suspend</span></span>

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

### <span data-ttu-id="9cc94-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9cc94-125">-InformationVariable</span></span>
<span data-ttu-id="9cc94-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9cc94-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9cc94-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9cc94-127">-Profile</span></span>
<span data-ttu-id="9cc94-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9cc94-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cc94-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9cc94-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9cc94-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc94-130">CommonParameters</span></span>
<span data-ttu-id="9cc94-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cc94-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc94-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cc94-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc94-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9cc94-133">INPUTS</span></span>

## <span data-ttu-id="9cc94-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9cc94-134">OUTPUTS</span></span>

## <span data-ttu-id="9cc94-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9cc94-135">NOTES</span></span>

## <span data-ttu-id="9cc94-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cc94-136">RELATED LINKS</span></span>

[<span data-ttu-id="9cc94-137">AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="9cc94-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="9cc94-138">移除-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="9cc94-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="9cc94-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="9cc94-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


