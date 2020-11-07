---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 821CB3E4-102E-440A-8C92-D1890899A6EE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 64924d579eebb826bc9c36468da1617370f48cf7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967476"
---
# <span data-ttu-id="32485-101">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="32485-101">Start-AzureService</span></span>

## <span data-ttu-id="32485-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32485-102">SYNOPSIS</span></span>
<span data-ttu-id="32485-103">在 Windows Azure 中啟動指定的託管服務。</span><span class="sxs-lookup"><span data-stu-id="32485-103">Starts the specified hosted service in Windows Azure.</span></span>

## <span data-ttu-id="32485-104">句法</span><span class="sxs-lookup"><span data-stu-id="32485-104">SYNTAX</span></span>

```
Start-AzureService [-ServiceName <String>] [-Slot <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="32485-105">說明</span><span class="sxs-lookup"><span data-stu-id="32485-105">DESCRIPTION</span></span>
<span data-ttu-id="32485-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32485-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="32485-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="32485-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="32485-108">如果服務處於停止狀態，則 **AzureService** Cmdlet 會在 Windows Azure 中啟動指定的託管服務。</span><span class="sxs-lookup"><span data-stu-id="32485-108">The **Start-AzureService** cmdlet starts the specified hosted service in Windows Azure, if the service is in the stopped state.</span></span>
<span data-ttu-id="32485-109">請注意， **Publish AzureServiceProject** Cmdlet 會自動嘗試啟動該服務。</span><span class="sxs-lookup"><span data-stu-id="32485-109">Note that the **Publish-AzureServiceProject** cmdlet automatically attempts to start the service.</span></span>

## <span data-ttu-id="32485-110">示例</span><span class="sxs-lookup"><span data-stu-id="32485-110">EXAMPLES</span></span>

## <span data-ttu-id="32485-111">參數</span><span class="sxs-lookup"><span data-stu-id="32485-111">PARAMETERS</span></span>

### <span data-ttu-id="32485-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32485-112">-PassThru</span></span>
<span data-ttu-id="32485-113">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="32485-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="32485-114">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="32485-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="32485-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="32485-115">-Profile</span></span>
<span data-ttu-id="32485-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="32485-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32485-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="32485-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32485-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="32485-118">-ServiceName</span></span>
<span data-ttu-id="32485-119">指定要啟動之託管服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="32485-119">Specifies the name of the hosted service to start.</span></span>
<span data-ttu-id="32485-120">如果沒有指定名稱，則 Cmdlet 會啟動目前的託管服務。</span><span class="sxs-lookup"><span data-stu-id="32485-120">If no name is specified, the cmdlet starts the current hosted service.</span></span>

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

### <span data-ttu-id="32485-121">-槽</span><span class="sxs-lookup"><span data-stu-id="32485-121">-Slot</span></span>
<span data-ttu-id="32485-122">指定要啟動服務的部署槽（暫存或生產）。</span><span class="sxs-lookup"><span data-stu-id="32485-122">Specifies the deployment slot in which to start the service, either Staging or Production.</span></span>

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

### <span data-ttu-id="32485-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32485-123">CommonParameters</span></span>
<span data-ttu-id="32485-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32485-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32485-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32485-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32485-126">輸入</span><span class="sxs-lookup"><span data-stu-id="32485-126">INPUTS</span></span>

## <span data-ttu-id="32485-127">輸出</span><span class="sxs-lookup"><span data-stu-id="32485-127">OUTPUTS</span></span>

## <span data-ttu-id="32485-128">筆記</span><span class="sxs-lookup"><span data-stu-id="32485-128">NOTES</span></span>

## <span data-ttu-id="32485-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="32485-129">RELATED LINKS</span></span>

[<span data-ttu-id="32485-130">移除-AzureService</span><span class="sxs-lookup"><span data-stu-id="32485-130">Remove-AzureService</span></span>](./Remove-AzureService.md)

[<span data-ttu-id="32485-131">開始-AzureService</span><span class="sxs-lookup"><span data-stu-id="32485-131">Start-AzureService</span></span>](./Start-AzureService.md)

[<span data-ttu-id="32485-132">停止 AzureService</span><span class="sxs-lookup"><span data-stu-id="32485-132">Stop-AzureService</span></span>](./Stop-AzureService.md)


