---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 939A28A4-394A-4447-9EFA-8F2876D04DCD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b140c2c0efac81e361e2bab510cfeaf6210ef884
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967253"
---
# <span data-ttu-id="66b6a-101">Stop-AzureService</span><span class="sxs-lookup"><span data-stu-id="66b6a-101">Stop-AzureService</span></span>

## <span data-ttu-id="66b6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="66b6a-103">停止目前的託管服務。</span><span class="sxs-lookup"><span data-stu-id="66b6a-103">Stops the current hosted service.</span></span>

## <span data-ttu-id="66b6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="66b6a-104">SYNTAX</span></span>

```
Stop-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="66b6a-105">說明</span><span class="sxs-lookup"><span data-stu-id="66b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="66b6a-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66b6a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="66b6a-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="66b6a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="66b6a-108">**AzureService** Cmdlet 會在 Windows Azure 的指定槽中停止目前的託管服務。</span><span class="sxs-lookup"><span data-stu-id="66b6a-108">The **Stop-AzureService** cmdlet stops the current hosted service in the specified slot in Windows Azure.</span></span>
<span data-ttu-id="66b6a-109">如果未指定任何槽，則 Cmdlet 會停止生產槽中的服務。</span><span class="sxs-lookup"><span data-stu-id="66b6a-109">If no slot is specified, the cmdlet stops the service in the Production slot.</span></span>

## <span data-ttu-id="66b6a-110">示例</span><span class="sxs-lookup"><span data-stu-id="66b6a-110">EXAMPLES</span></span>

## <span data-ttu-id="66b6a-111">參數</span><span class="sxs-lookup"><span data-stu-id="66b6a-111">PARAMETERS</span></span>

### <span data-ttu-id="66b6a-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66b6a-112">-PassThru</span></span>
<span data-ttu-id="66b6a-113">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="66b6a-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66b6a-114">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="66b6a-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66b6a-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="66b6a-115">-Profile</span></span>
<span data-ttu-id="66b6a-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="66b6a-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66b6a-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="66b6a-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66b6a-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="66b6a-118">-ServiceName</span></span>
<span data-ttu-id="66b6a-119">指定要停止之託管服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="66b6a-119">Specifies the name of the hosted service to stop.</span></span>
<span data-ttu-id="66b6a-120">如果沒有指定名稱，則 Cmdlet 會停止目前的託管服務。</span><span class="sxs-lookup"><span data-stu-id="66b6a-120">If no name is specified, the cmdlet stops the current hosted service.</span></span>

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

### <span data-ttu-id="66b6a-121">-槽</span><span class="sxs-lookup"><span data-stu-id="66b6a-121">-Slot</span></span>
<span data-ttu-id="66b6a-122">指定主機服務（暫存或生產）的主機槽。</span><span class="sxs-lookup"><span data-stu-id="66b6a-122">Specifies the slot where the service is hosted, either Staging or Production.</span></span>
<span data-ttu-id="66b6a-123">如果未指定任何槽，則會假設為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="66b6a-123">If no slot is specified,  Production is assumed.</span></span>

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

### <span data-ttu-id="66b6a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b6a-124">CommonParameters</span></span>
<span data-ttu-id="66b6a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66b6a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b6a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66b6a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b6a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="66b6a-127">INPUTS</span></span>

## <span data-ttu-id="66b6a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="66b6a-128">OUTPUTS</span></span>

## <span data-ttu-id="66b6a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="66b6a-129">NOTES</span></span>

## <span data-ttu-id="66b6a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="66b6a-130">RELATED LINKS</span></span>

[<span data-ttu-id="66b6a-131">移除-AzureService</span><span class="sxs-lookup"><span data-stu-id="66b6a-131">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="66b6a-132">開始-AzureService</span><span class="sxs-lookup"><span data-stu-id="66b6a-132">Start-AzureService</span></span>](./Start-AzureService.md)


