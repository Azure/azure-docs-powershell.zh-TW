---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 9ee9277ccbadf190605d8c9e05a1637011204219
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901885"
---
# <span data-ttu-id="30257-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30257-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="30257-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30257-102">SYNOPSIS</span></span>
<span data-ttu-id="30257-103">在虛擬網路閘道連接上停止封包捕獲作業</span><span class="sxs-lookup"><span data-stu-id="30257-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="30257-104">語法</span><span class="sxs-lookup"><span data-stu-id="30257-104">SYNTAX</span></span>

### <span data-ttu-id="30257-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="30257-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30257-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="30257-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30257-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="30257-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30257-108">描述</span><span class="sxs-lookup"><span data-stu-id="30257-108">DESCRIPTION</span></span>
<span data-ttu-id="30257-109">停止虛擬網路閘道連接上的封包捕獲作業，並且將結果上傳至給定 SasUrl 的儲存容器上。</span><span class="sxs-lookup"><span data-stu-id="30257-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="30257-110">例子</span><span class="sxs-lookup"><span data-stu-id="30257-110">EXAMPLES</span></span>

### <span data-ttu-id="30257-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="30257-111">Example 1</span></span>
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

### <span data-ttu-id="30257-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="30257-112">Example 2</span></span>
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

## <span data-ttu-id="30257-113">參數</span><span class="sxs-lookup"><span data-stu-id="30257-113">PARAMETERS</span></span>

### <span data-ttu-id="30257-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30257-114">-AsJob</span></span>
<span data-ttu-id="30257-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="30257-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="30257-116">-確認</span><span class="sxs-lookup"><span data-stu-id="30257-116">-Confirm</span></span>
<span data-ttu-id="30257-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="30257-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30257-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30257-118">-DefaultProfile</span></span>
<span data-ttu-id="30257-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30257-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30257-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30257-120">-InputObject</span></span>
<span data-ttu-id="30257-121">要開始封包捕獲的虛擬網路閘道連線物件。</span><span class="sxs-lookup"><span data-stu-id="30257-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="30257-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="30257-122">-Name</span></span>
<span data-ttu-id="30257-123">要開始封包捕獲的虛擬網路閘道連接名稱。</span><span class="sxs-lookup"><span data-stu-id="30257-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="30257-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30257-124">-ResourceGroupName</span></span>
<span data-ttu-id="30257-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="30257-125">The resource group name.</span></span>

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

### <span data-ttu-id="30257-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30257-126">-ResourceId</span></span>
<span data-ttu-id="30257-127">VirtualNetworkGatewayConnection 的 Azure 資源識別碼，其中要開始封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="30257-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="30257-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="30257-128">-SasUrl</span></span>
<span data-ttu-id="30257-129">用於在虛擬網路閘道上停止封包捕獲的 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="30257-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="30257-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30257-130">-WhatIf</span></span>
<span data-ttu-id="30257-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="30257-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30257-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30257-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30257-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30257-133">CommonParameters</span></span>
<span data-ttu-id="30257-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30257-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30257-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30257-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30257-136">輸入</span><span class="sxs-lookup"><span data-stu-id="30257-136">INPUTS</span></span>

### <span data-ttu-id="30257-137">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="30257-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="30257-138">System.String</span><span class="sxs-lookup"><span data-stu-id="30257-138">System.String</span></span>

## <span data-ttu-id="30257-139">輸出</span><span class="sxs-lookup"><span data-stu-id="30257-139">OUTPUTS</span></span>

### <span data-ttu-id="30257-140">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="30257-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="30257-141">筆記</span><span class="sxs-lookup"><span data-stu-id="30257-141">NOTES</span></span>

## <span data-ttu-id="30257-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="30257-142">RELATED LINKS</span></span>
[<span data-ttu-id="30257-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="30257-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)