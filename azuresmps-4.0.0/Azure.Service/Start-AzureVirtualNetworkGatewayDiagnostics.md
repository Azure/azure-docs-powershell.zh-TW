---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967218"
---
# <span data-ttu-id="8e0c5-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8e0c5-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="8e0c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="8e0c5-103">啟動虛擬網路閘道的診斷程式。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="8e0c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e0c5-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e0c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e0c5-105">DESCRIPTION</span></span>
<span data-ttu-id="8e0c5-106">**Start-AzureVirtualNetworkGatewayDiagnostics** Cmdlet 會為虛擬網路閘道啟動新的閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="8e0c5-107">一次只能執行一個閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="8e0c5-108">如果您在閘道診斷會話執行時執行這個 Cmdlet，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="8e0c5-109">示例</span><span class="sxs-lookup"><span data-stu-id="8e0c5-109">EXAMPLES</span></span>

## <span data-ttu-id="8e0c5-110">參數</span><span class="sxs-lookup"><span data-stu-id="8e0c5-110">PARAMETERS</span></span>

### <span data-ttu-id="8e0c5-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="8e0c5-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="8e0c5-112">指定捕獲持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0c5-113">-容器</span><span class="sxs-lookup"><span data-stu-id="8e0c5-113">-ContainerName</span></span>
<span data-ttu-id="8e0c5-114">指定 Azure 容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="8e0c5-115">這個 Cmdlet 會將結果儲存在此參數指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e0c5-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8e0c5-116">-GatewayId</span></span>
<span data-ttu-id="8e0c5-117">指定閘道的 ID。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-117">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0c5-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8e0c5-118">-Profile</span></span>
<span data-ttu-id="8e0c5-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8e0c5-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8e0c5-121">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="8e0c5-121">-StorageContext</span></span>
<span data-ttu-id="8e0c5-122">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="8e0c5-123">這個 Cmdlet 會使用此參數指定的儲存區內容來儲存結果。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e0c5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e0c5-124">CommonParameters</span></span>
<span data-ttu-id="8e0c5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e0c5-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e0c5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e0c5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8e0c5-127">INPUTS</span></span>

## <span data-ttu-id="8e0c5-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8e0c5-128">OUTPUTS</span></span>

## <span data-ttu-id="8e0c5-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8e0c5-129">NOTES</span></span>

## <span data-ttu-id="8e0c5-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e0c5-130">RELATED LINKS</span></span>

[<span data-ttu-id="8e0c5-131">AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8e0c5-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="8e0c5-132">停止 AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="8e0c5-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


