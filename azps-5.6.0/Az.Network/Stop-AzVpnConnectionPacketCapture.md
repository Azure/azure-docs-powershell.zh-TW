---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: d37bd9fa620b6da68c311399be811f639ea85aea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901862"
---
# <span data-ttu-id="23357-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23357-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="23357-102">簡介</span><span class="sxs-lookup"><span data-stu-id="23357-102">SYNOPSIS</span></span>
<span data-ttu-id="23357-103">在 Vpn 連接上停止封包捕獲作業</span><span class="sxs-lookup"><span data-stu-id="23357-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="23357-104">語法</span><span class="sxs-lookup"><span data-stu-id="23357-104">SYNTAX</span></span>

### <span data-ttu-id="23357-105">By VpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="23357-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23357-106">By VpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="23357-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23357-107">By VpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="23357-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23357-108">描述</span><span class="sxs-lookup"><span data-stu-id="23357-108">DESCRIPTION</span></span>
<span data-ttu-id="23357-109">停止 Vpn 連接上的封包捕獲作業，並上傳給儲存容器的 SasUrl 上的結果。</span><span class="sxs-lookup"><span data-stu-id="23357-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="23357-110">例子</span><span class="sxs-lookup"><span data-stu-id="23357-110">EXAMPLES</span></span>

### <span data-ttu-id="23357-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="23357-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="23357-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="23357-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="23357-113">參數</span><span class="sxs-lookup"><span data-stu-id="23357-113">PARAMETERS</span></span>

### <span data-ttu-id="23357-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23357-114">-AsJob</span></span>
<span data-ttu-id="23357-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="23357-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23357-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23357-116">-DefaultProfile</span></span>
<span data-ttu-id="23357-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="23357-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23357-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23357-118">-InputObject</span></span>
<span data-ttu-id="23357-119">要開始封包捕獲的 Vpn 連線物件。</span><span class="sxs-lookup"><span data-stu-id="23357-119">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23357-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="23357-120">-LinkConnectionName</span></span>
<span data-ttu-id="23357-121">SiteLinkConnection 的名稱。</span><span class="sxs-lookup"><span data-stu-id="23357-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="23357-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="23357-122">-Name</span></span>
<span data-ttu-id="23357-123">要開始封包捕獲的 Vpn 連接名稱。</span><span class="sxs-lookup"><span data-stu-id="23357-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23357-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="23357-124">-ParentResourceName</span></span>
<span data-ttu-id="23357-125">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="23357-125">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23357-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23357-126">-ResourceGroupName</span></span>
<span data-ttu-id="23357-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="23357-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23357-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23357-128">-ResourceId</span></span>
<span data-ttu-id="23357-129">要開始封包捕獲之 VpnConnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="23357-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23357-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="23357-130">-SasUrl</span></span>
<span data-ttu-id="23357-131">VPN 上停止封包捕獲的 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="23357-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="23357-132">-確認</span><span class="sxs-lookup"><span data-stu-id="23357-132">-Confirm</span></span>
<span data-ttu-id="23357-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="23357-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23357-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23357-134">-WhatIf</span></span>
<span data-ttu-id="23357-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23357-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23357-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23357-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23357-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23357-137">CommonParameters</span></span>
<span data-ttu-id="23357-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="23357-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23357-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23357-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23357-140">輸入</span><span class="sxs-lookup"><span data-stu-id="23357-140">INPUTS</span></span>

### <span data-ttu-id="23357-141">Microsoft.Azure.Commands.Network.models.PS VpnConnection</span><span class="sxs-lookup"><span data-stu-id="23357-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="23357-142">System.String</span><span class="sxs-lookup"><span data-stu-id="23357-142">System.String</span></span>

## <span data-ttu-id="23357-143">輸出</span><span class="sxs-lookup"><span data-stu-id="23357-143">OUTPUTS</span></span>

### <span data-ttu-id="23357-144">Microsoft.Azure.Commands.Network.models.PS VpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="23357-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="23357-145">筆記</span><span class="sxs-lookup"><span data-stu-id="23357-145">NOTES</span></span>

## <span data-ttu-id="23357-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="23357-146">RELATED LINKS</span></span>

[<span data-ttu-id="23357-147">Start-Az VpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="23357-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)