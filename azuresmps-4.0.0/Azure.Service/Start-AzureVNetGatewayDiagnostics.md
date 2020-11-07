---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967472"
---
# <span data-ttu-id="1e917-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e917-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="1e917-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e917-102">SYNOPSIS</span></span>
<span data-ttu-id="1e917-103">為 VPN 閘道啟動閘道診斷程式。</span><span class="sxs-lookup"><span data-stu-id="1e917-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="1e917-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e917-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e917-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e917-105">DESCRIPTION</span></span>
<span data-ttu-id="1e917-106">**AzureVNetGatewayDiagnostics** Cmdlet 會針對虛擬私人網路絡 (VPN) 閘道，啟動新的閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="1e917-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="1e917-107">一次只能執行一個閘道診斷會話。</span><span class="sxs-lookup"><span data-stu-id="1e917-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="1e917-108">如果您在閘道診斷會話執行時執行這個 Cmdlet，這個 Cmdlet 會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="1e917-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="1e917-109">示例</span><span class="sxs-lookup"><span data-stu-id="1e917-109">EXAMPLES</span></span>

## <span data-ttu-id="1e917-110">參數</span><span class="sxs-lookup"><span data-stu-id="1e917-110">PARAMETERS</span></span>

### <span data-ttu-id="1e917-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="1e917-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="1e917-112">指定捕獲持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1e917-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e917-113">-容器</span><span class="sxs-lookup"><span data-stu-id="1e917-113">-ContainerName</span></span>
<span data-ttu-id="1e917-114">指定 Azure 容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e917-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="1e917-115">這個 Cmdlet 會將結果儲存在此參數指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="1e917-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e917-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1e917-116">-Profile</span></span>
<span data-ttu-id="1e917-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1e917-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1e917-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1e917-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1e917-119">-StorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="1e917-119">-StorageContext</span></span>
<span data-ttu-id="1e917-120">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="1e917-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1e917-121">這個 Cmdlet 會使用此參數指定的儲存區內容來儲存結果。</span><span class="sxs-lookup"><span data-stu-id="1e917-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e917-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="1e917-122">-VNetName</span></span>
<span data-ttu-id="1e917-123">指定包含此 Cmdlet 執行診斷之虛擬網路閘道的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="1e917-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="1e917-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e917-124">CommonParameters</span></span>
<span data-ttu-id="1e917-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e917-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e917-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e917-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e917-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1e917-127">INPUTS</span></span>

## <span data-ttu-id="1e917-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1e917-128">OUTPUTS</span></span>

## <span data-ttu-id="1e917-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1e917-129">NOTES</span></span>

## <span data-ttu-id="1e917-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e917-130">RELATED LINKS</span></span>

[<span data-ttu-id="1e917-131">AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e917-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="1e917-132">停止 AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1e917-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


