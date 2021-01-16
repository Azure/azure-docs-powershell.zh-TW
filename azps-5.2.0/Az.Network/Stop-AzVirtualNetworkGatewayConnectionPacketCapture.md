---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282423"
---
# <span data-ttu-id="2f128-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f128-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="2f128-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f128-102">SYNOPSIS</span></span>
<span data-ttu-id="2f128-103">在虛擬網路閘道連線時停止資料包捕獲作業</span><span class="sxs-lookup"><span data-stu-id="2f128-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="2f128-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f128-104">SYNTAX</span></span>

### <span data-ttu-id="2f128-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="2f128-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f128-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f128-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f128-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f128-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f128-108">說明</span><span class="sxs-lookup"><span data-stu-id="2f128-108">DESCRIPTION</span></span>
<span data-ttu-id="2f128-109">在虛擬網路閘道連線時停止 [資料包捕獲] 作業，並將在指定的儲存空間 SasUrl 容器上上傳結果。</span><span class="sxs-lookup"><span data-stu-id="2f128-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="2f128-110">示例</span><span class="sxs-lookup"><span data-stu-id="2f128-110">EXAMPLES</span></span>

### <span data-ttu-id="2f128-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2f128-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="2f128-112">範例2</span><span class="sxs-lookup"><span data-stu-id="2f128-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="2f128-113">參數</span><span class="sxs-lookup"><span data-stu-id="2f128-113">PARAMETERS</span></span>

### <span data-ttu-id="2f128-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f128-114">-AsJob</span></span>
<span data-ttu-id="2f128-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2f128-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f128-116">-確認</span><span class="sxs-lookup"><span data-stu-id="2f128-116">-Confirm</span></span>
<span data-ttu-id="2f128-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f128-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f128-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f128-118">-DefaultProfile</span></span>
<span data-ttu-id="2f128-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f128-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f128-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f128-120">-InputObject</span></span>
<span data-ttu-id="2f128-121">要開始建立資料包捕獲的虛擬網路閘道連線物件。</span><span class="sxs-lookup"><span data-stu-id="2f128-121">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f128-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f128-122">-Name</span></span>
<span data-ttu-id="2f128-123">要開始建立資料包捕獲的虛擬網路閘道連線名稱。</span><span class="sxs-lookup"><span data-stu-id="2f128-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f128-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f128-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f128-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f128-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f128-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f128-126">-ResourceId</span></span>
<span data-ttu-id="2f128-127">要開始進行資料包捕獲之 VirtualNetworkGatewayConnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f128-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f128-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="2f128-128">-SasUrl</span></span>
<span data-ttu-id="2f128-129">在虛擬網路閘道上停止資料包捕獲的 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="2f128-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="2f128-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f128-130">-WhatIf</span></span>
<span data-ttu-id="2f128-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f128-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f128-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f128-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f128-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f128-133">CommonParameters</span></span>
<span data-ttu-id="2f128-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f128-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f128-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2f128-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f128-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2f128-136">INPUTS</span></span>

### <span data-ttu-id="2f128-137">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f128-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="2f128-138">System.object</span><span class="sxs-lookup"><span data-stu-id="2f128-138">System.String</span></span>

## <span data-ttu-id="2f128-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2f128-139">OUTPUTS</span></span>

### <span data-ttu-id="2f128-140">PSVirtualNetworkGatewayPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2f128-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2f128-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2f128-141">NOTES</span></span>

## <span data-ttu-id="2f128-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f128-142">RELATED LINKS</span></span>
[<span data-ttu-id="2f128-143">開始-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f128-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)