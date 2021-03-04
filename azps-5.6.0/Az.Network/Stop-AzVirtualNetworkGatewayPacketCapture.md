---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 2838d3d18aaa1cdf450eed184c5ebfe9a803c20a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901881"
---
# <span data-ttu-id="58cda-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58cda-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="58cda-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58cda-102">SYNOPSIS</span></span>
<span data-ttu-id="58cda-103">停止在虛擬網路閘道上的封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="58cda-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="58cda-104">語法</span><span class="sxs-lookup"><span data-stu-id="58cda-104">SYNTAX</span></span>

### <span data-ttu-id="58cda-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="58cda-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58cda-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="58cda-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58cda-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="58cda-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58cda-108">描述</span><span class="sxs-lookup"><span data-stu-id="58cda-108">DESCRIPTION</span></span>
<span data-ttu-id="58cda-109">停止在虛擬網路閘道上的封包捕獲作業，並上傳結果于提供之 SasUrl 的儲存容器上。</span><span class="sxs-lookup"><span data-stu-id="58cda-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="58cda-110">例子</span><span class="sxs-lookup"><span data-stu-id="58cda-110">EXAMPLES</span></span>

### <span data-ttu-id="58cda-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="58cda-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="58cda-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="58cda-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="58cda-113">參數</span><span class="sxs-lookup"><span data-stu-id="58cda-113">PARAMETERS</span></span>

### <span data-ttu-id="58cda-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58cda-114">-AsJob</span></span>
<span data-ttu-id="58cda-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58cda-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58cda-116">-確認</span><span class="sxs-lookup"><span data-stu-id="58cda-116">-Confirm</span></span>
<span data-ttu-id="58cda-117">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="58cda-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58cda-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58cda-118">-DefaultProfile</span></span>
<span data-ttu-id="58cda-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58cda-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58cda-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58cda-120">-InputObject</span></span>
<span data-ttu-id="58cda-121">要開始封包捕獲的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="58cda-121">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58cda-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="58cda-122">-Name</span></span>
<span data-ttu-id="58cda-123">要開始封包捕獲的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="58cda-123">The virtual network gateway name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58cda-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58cda-124">-ResourceGroupName</span></span>
<span data-ttu-id="58cda-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="58cda-125">The resource group name.</span></span>

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

### <span data-ttu-id="58cda-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58cda-126">-ResourceId</span></span>
<span data-ttu-id="58cda-127">VirtualNetworkGateway 的 Azure 資源識別碼，其中要開始封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="58cda-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="58cda-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="58cda-128">-SasUrl</span></span>
<span data-ttu-id="58cda-129">在虛擬網路閘道上捕獲 SAS URL 封包。</span><span class="sxs-lookup"><span data-stu-id="58cda-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="58cda-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58cda-130">-WhatIf</span></span>
<span data-ttu-id="58cda-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58cda-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58cda-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58cda-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58cda-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cda-133">CommonParameters</span></span>
<span data-ttu-id="58cda-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58cda-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58cda-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58cda-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cda-136">輸入</span><span class="sxs-lookup"><span data-stu-id="58cda-136">INPUTS</span></span>

### <span data-ttu-id="58cda-137">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="58cda-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="58cda-138">System.String</span><span class="sxs-lookup"><span data-stu-id="58cda-138">System.String</span></span>

## <span data-ttu-id="58cda-139">輸出</span><span class="sxs-lookup"><span data-stu-id="58cda-139">OUTPUTS</span></span>

### <span data-ttu-id="58cda-140">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="58cda-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="58cda-141">筆記</span><span class="sxs-lookup"><span data-stu-id="58cda-141">NOTES</span></span>

## <span data-ttu-id="58cda-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="58cda-142">RELATED LINKS</span></span>
[<span data-ttu-id="58cda-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="58cda-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
