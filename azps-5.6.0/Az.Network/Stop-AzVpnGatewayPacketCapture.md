---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: d61b12a5a46abbba95919bb747966caf14d61538
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901861"
---
# <span data-ttu-id="44220-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44220-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="44220-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44220-102">SYNOPSIS</span></span>
<span data-ttu-id="44220-103">停止 Vpn 閘道上的封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="44220-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="44220-104">語法</span><span class="sxs-lookup"><span data-stu-id="44220-104">SYNTAX</span></span>

### <span data-ttu-id="44220-105">By VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="44220-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44220-106">By VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="44220-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44220-107">By VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="44220-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44220-108">描述</span><span class="sxs-lookup"><span data-stu-id="44220-108">DESCRIPTION</span></span>
<span data-ttu-id="44220-109">停止 Vpn 閘道的封包捕獲作業，並上傳給儲存容器的 SasUrl 結果。</span><span class="sxs-lookup"><span data-stu-id="44220-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="44220-110">例子</span><span class="sxs-lookup"><span data-stu-id="44220-110">EXAMPLES</span></span>

### <span data-ttu-id="44220-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="44220-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
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

### <span data-ttu-id="44220-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="44220-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
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

## <span data-ttu-id="44220-113">參數</span><span class="sxs-lookup"><span data-stu-id="44220-113">PARAMETERS</span></span>

### <span data-ttu-id="44220-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44220-114">-AsJob</span></span>
<span data-ttu-id="44220-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="44220-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44220-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44220-116">-DefaultProfile</span></span>
<span data-ttu-id="44220-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44220-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44220-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44220-118">-InputObject</span></span>
<span data-ttu-id="44220-119">要開始封包捕獲的 Vpn 閘道物件。</span><span class="sxs-lookup"><span data-stu-id="44220-119">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44220-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="44220-120">-Name</span></span>
<span data-ttu-id="44220-121">要開始封包捕獲的 Vpn 閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="44220-121">The Vpn Gateway name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44220-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44220-122">-ResourceGroupName</span></span>
<span data-ttu-id="44220-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="44220-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44220-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44220-124">-ResourceId</span></span>
<span data-ttu-id="44220-125">VpnGateway 的 Azure 資源識別碼，其中要開始封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="44220-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44220-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="44220-126">-SasUrl</span></span>
<span data-ttu-id="44220-127">VPN 閘道上的 SAS URL 封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="44220-127">SAS URL packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44220-128">-確認</span><span class="sxs-lookup"><span data-stu-id="44220-128">-Confirm</span></span>
<span data-ttu-id="44220-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="44220-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44220-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44220-130">-WhatIf</span></span>
<span data-ttu-id="44220-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44220-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44220-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44220-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44220-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44220-133">CommonParameters</span></span>
<span data-ttu-id="44220-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44220-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44220-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44220-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44220-136">輸入</span><span class="sxs-lookup"><span data-stu-id="44220-136">INPUTS</span></span>

### <span data-ttu-id="44220-137">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="44220-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="44220-138">System.String</span><span class="sxs-lookup"><span data-stu-id="44220-138">System.String</span></span>

## <span data-ttu-id="44220-139">輸出</span><span class="sxs-lookup"><span data-stu-id="44220-139">OUTPUTS</span></span>

### <span data-ttu-id="44220-140">Microsoft.Azure.Commands.Network.models.PS VpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="44220-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="44220-141">筆記</span><span class="sxs-lookup"><span data-stu-id="44220-141">NOTES</span></span>

## <span data-ttu-id="44220-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="44220-142">RELATED LINKS</span></span>

[<span data-ttu-id="44220-143">Start-Az VpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="44220-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)